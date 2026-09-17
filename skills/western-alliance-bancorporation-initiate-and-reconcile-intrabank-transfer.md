---
generated: '2026-09-17'
method: generated
name: Initiate and reconcile an intrabank transfer
description: Move funds between two Western Alliance Bank accounts, capture the Payment Message Reference, confirm via the webhook (or Search API fallback), and reconcile against intraday and prior-day history.
api: openapi/western-alliance-bancorporation-intrabank-transfer-api-openapi.yml
operations: [getToken, initiateIntraBankTransfer, searchIntraBankTransfers, getIntradayTransactions, getPriordayTransactions]
source: >-
  Mirrors the "Core Workflow" in the provider's Intrabank Transfer API User Guide
  (https://developer.westernalliancebank.com/sfsites/c/cms/delivery/media/MC2GPNZ5A6AFBB7FPCQ6YISYCQY4);
  operationIds verified in openapi/western-alliance-bancorporation-intrabank-transfer-api-openapi.yml,
  openapi/western-alliance-bancorporation-token-api-openapi.yml and the single-account intraday / priorday specs.
---

# Initiate and reconcile an intrabank transfer

The webhook is the primary confirmation; Search, Intraday and Prior Day are reconciliation tools. Always log the
`PaymentMessageReference` - it is the one identifier that appears in every surface.

## Auth
- `getToken` (`GET /entitlements-get-token-eapi/api/v1/token?Scope=Informational`) with headers `appClientId`,
  `appClientSecret`, `X-Correlation-ID` (GUID). Use the returned bearer on every call; tokens expire after an
  unpublished period. See `authentication/western-alliance-bancorporation-authentication.yml`.
- Servers initiating transfers must carry the WAB-issued Client Certificate (API Services Terms 6(c)(ii)).

## Idempotency
- Choose a unique client `PaymentId` per transfer. A repeat returns `409 Duplicate`; do NOT retry blindly - look the
  transfer up instead (step 4). Coverage is partial: only this operation has a replay guard
  (`conventions/western-alliance-bancorporation-conventions.yml`).

## Steps
1. **Initiate** - `initiateIntraBankTransfer` (`POST /trnsct-ibt-eapi/api/v1/transactions/intraBankTransfer`) with
   `SystemIdentifier`, `PaymentId`, `ProcessingDate` (yyyyMMdd), `Amount` (zero-padded cents, "0124" = $1.24),
   `Currency`, `OriginatorAccountId`, `BeneficiaryAccountId`, `BeneficiaryName`, `RemittanceInformation`.
   Read `Status` / `StatusCode`: `W02` Accepted means format-valid only; `W21` (HTTP 200!) is a rejection.
   Persist `PaymentMessageReference`.
2. **Confirm** - wait for the webhook (`asyncapi/western-alliance-bancorporation-webhooks.yml`): `StatusCode`
   `ACSC` = executed, `RJCT` = rejected with `FundTransferReasonCode` (e.g. `MS01`).
3. **Same-day check (optional)** - `getIntradayTransactions` on the originating account; the reference appears in
   `AdditionalInformation` as `TRN-<PaymentMessageReference>`.
4. **Fallback lookup** - if no webhook arrives, `searchIntraBankTransfers`
   (`POST /trnsct-ibt-eapi/api/v2/transactions/intraBankSearch?page=1`) with `Type` Originator or Beneficiary and
   exactly ONE of `PaymentId`, `PaymentMessageReference` or `ValueDate`.
5. **Next-day reconciliation** - `getPriordayTransactions`; the posted record's `TransactionControlNumber` is
   `000` + `PaymentMessageReference`.

## Errors
- `400 Rejected / Processing Date is Invalid`, `400 Cancelled while in Processing` (resubmit with a NEW PaymentId),
  `403 Not authorized for Intra Bank transaction`, `409 Duplicate`. Envelope: `{errors:[{code,message,additionalInfo}]}`.
  See `errors/western-alliance-bancorporation-problem-types.yml`.

## Notes
- No client-side cancel or reversal exists; treat the transfer as irreversible once accepted.
- Rehearse in the Client UAT Environment (`api-connect.westernalliancebanktest.com`) with fake data only.
