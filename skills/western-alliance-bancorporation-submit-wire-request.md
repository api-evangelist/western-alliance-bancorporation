---
generated: '2026-09-17'
method: generated
name: Submit a wire transfer request
description: Authenticate and submit a Fedwire-style wire transfer request from a virtual account, then verify posting through the transaction history APIs.
api: openapi/western-alliance-bancorporation-wires-request-api-openapi.yml
operations: [getToken, healthcheck, wiresRequestAPI, getPriordayTransactions]
source: >-
  Grounded in the Wires Request API Postman collection
  (https://developer.westernalliancebank.com/sfsites/c/cms/delivery/media/MCJUIZSAE2RBGVPGZKSFAQABOWGM);
  operationIds verified in openapi/western-alliance-bancorporation-wires-request-api-openapi.yml.
---

# Submit a wire transfer request

## Auth
- `getToken` with `appClientId` / `appClientSecret`; bearer on every call. Funds-transfer servers need the WAB
  Client Certificate.

## Idempotency
- None documented for wires. The body carries a `WireConfirmationNumber`; whether the gateway rejects a repeat is
  not published - do not retry a timed-out PUT without checking history first.

## Steps
1. **Liveness** - `healthcheck` (`GET /trnsct-wires-rqst-eapi/api/v1/healthcheck`, `X-Dependent-Ping: false`).
2. **Submit** - `wiresRequestAPI` (`PUT /trnsct-wires-rqst-eapi/api/v1/wires/transferRequest`) with
   `SystemIdentifier`, `WireConfirmationNumber`, `MethodOfPayment` (`FED`), `ProcessingDate` (yyyyMMdd),
   `Amount` (17-char zero-padded cents), `Currency`, `VirtualAccountNumber` / `VirtualAccountName` / address lines
   and the originator / beneficiary block exactly as in the collection example.
3. **Verify** - next business day, `getPriordayTransactions` on the debited account.

## Errors
- Not published for wires; the shared envelope is `{errors:[{code,message,additionalInfo}]}`.

## Notes
- No cancel / recall operation is published; a wire recall is a bank operations process, not an API call
  (`conventions/western-alliance-bancorporation-conventions.yml` reversibility block).
