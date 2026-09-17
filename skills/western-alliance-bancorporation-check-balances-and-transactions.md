---
generated: '2026-09-17'
method: generated
name: Check balances and pull transaction history
description: Authenticate, read balances for one or all entitled accounts, and page through intraday, prior-day or date-range transaction history with filters.
api: openapi/western-alliance-bancorporation-all-account-balance-api-openapi.yml
operations: [getToken, getBalance, getIntradayTransactions, getPriordayTransactions, getDateRangeTransactions]
source: >-
  Grounded in the Informational API Postman collections on the WAB API Developer Portal
  (https://developer.westernalliancebank.com/s/postman-collection) and the portal's Get Balance tutorial page;
  operationIds verified in openapi/western-alliance-bancorporation-{all,single}-account-*-openapi.yml and
  openapi/western-alliance-bancorporation-date-range-transactions-api-openapi.yml.
---

# Check balances and pull transaction history

Read-only flow across the Informational family. Every call carries `Authorization: Bearer` and an
`X-Correlation-ID` GUID.

## Auth
- `getToken` with `appClientId` / `appClientSecret` headers and `Scope=Informational`.

## Steps
1. **All-account balance** - `getBalance` (`GET /info-multi-acc-balance-eapi/api/v1/dp/accounts/balance`), or
   the single-account variant `GET /info-single-acc-balance-eapi/api/v1dp/accounts/{AccountNumber}/balance`
   (path carried verbatim from the collection, which omits the slash before `dp`).
2. **Today's activity** - `getIntradayTransactions`
   (`GET /info-multi-acc-intraday-eapi/api/v1/dp/accounts/transactions/intraday` or the single-account form).
   Optional filters: `FilterType`, `CheckNumber`, `Amount`, `TransactionCode`, `TimeDepositId`.
3. **Posted history** - `getPriordayTransactions` (`.../dp/accounts/transactions/priorDay`). Filters:
   `TransactionDate` (yyyy-MM-dd, defaults to last business day), `CheckOrSerialNumber`, `TransactionAmount`,
   `TransactionCode`, `TransactionCodeList` (max 10), `TransactionFilterType`, `ReturnExtended`.
4. **Date window** - `getDateRangeTransactions`
   (`GET /info-dt-rng-trns-eapi/api/v1/dp/accounts/{AccountNumber}/AccountTransactions`) with `BeginDate`,
   `EndDate` and the same filter set.
5. **Paginate** - send the `X-Next-Page-Key` header from the previous response on every history call until none
   is returned.

## Errors
- Only the intrabank surface publishes an error index; expect the same `{errors:[...]}` envelope here
  (`errors/western-alliance-bancorporation-problem-types.yml`). No rate-limit headers are documented.

## Notes
- Balances and history are separate products on the Setup Form; a token scoped to one product may not reach another.
