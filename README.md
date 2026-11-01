# Western Alliance Bancorporation

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Western Alliance Bancorporation (NYSE: WAL) is the parent of Western Alliance Bank, a top-performing US commercial bank. Its WAB API Developer Portal (developer.westernalliancebank.com, built on Salesforce Experience Cloud with MuleSoft Anypoint API Community Manager) publishes treasury-management APIs on the api-connect.westernalliancebank.com gateway in six families - Informational (balances, intraday, prior-day and date-range transactions, statements, check images, stop payments), Transactional (book transfer, wires, intrabank transfer, ACH beta), Utility (token), Embedded Finance, Digital Assets (TassatPay beta) and Corporate Trust. Access requires Treasury Management enrollment; the bank issues a Client ID / Client Secret exchanged for a time-limited bearer token, and the intrabank transfer surface pushes ISO 20022-coded status webhooks.

**Areas:** Banking · Financial Services · Treasury Management · Payments · Account · Transaction · Wires · ACH · Digital Assets · Webhook

## Western Alliance Bancorporation on APIs.io

Everything profiled for Western Alliance Bancorporation is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/western-alliance-bancorporation/](https://apis.io/providers/western-alliance-bancorporation/)** — or go straight to one of the APIs or properties below.

### APIs (26)

- [Western Alliance Bank Check Image API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-check-image-api/) — Retrieves the image of a paid check by account, check date, check number, trace number and amount. Family: Informational APIs on the WAB API Developer…
- [Western Alliance Bank Stop Payments API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-stop-payments-api/) — Places a stop-payment order on a check (or range) and looks up existing stop payments on an account. Family: Informational APIs on the WAB API Developer…
- [Western Alliance Bank Book Transfer API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-book-transfer-api/) — Moves funds between two Western Alliance accounts held by the same client (book transfer). Family: Transactional APIs on the WAB API Developer Portal; 2…
- [Western Alliance Bank Intrabank Transfer API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-intrabank-transfer-api/) — Initiates an intra-bank transfer between two Western Alliance Bank accounts and searches intra-bank transfers as originator or beneficiary. The transfer…
- [Western Alliance Bank API (Treasury Management)](https://apis.io/apis/western-alliance-bancorporation/wab-treasury-management-api/) — Western Alliance Bank's commercial open-banking API lets approved business clients interact directly with WAB systems to access balance and transaction…
- [Western Alliance Bancorporation ACH Request API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-ach-request-api/) — The ACH Request API from Western Alliance Bancorporation — 1 operation(s) for ach request.
- [Western Alliance Bancorporation Balance API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-balance-api/) — The Balance API from Western Alliance Bancorporation — 1 operation(s) for balance.
- [Western Alliance Bancorporation Client Data API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-client-data-api/) — The Client Data API from Western Alliance Bancorporation — 1 operation(s) for client data.
- [Western Alliance Bancorporation Date Range Transaction History API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-date-range-transaction-history-api/) — The Date Range Transaction History API from Western Alliance Bancorporation — 1 operation(s) for date range transaction history.
- [Western Alliance Bancorporation Deposite API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-deposite-api/) — The Deposite API from Western Alliance Bancorporation — 2 operation(s) for deposite.
- [Western Alliance Bancorporation Get Balance API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-get-balance-api/) — The Get Balance API from Western Alliance Bancorporation — 2 operation(s) for get balance.
- [Western Alliance Bancorporation Get Bank Statement API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-get-bank-statement-api-api/) — The Get Bank Statement API API from Western Alliance Bancorporation — 1 operation(s) for get bank statement api.
- [Western Alliance Bancorporation Get Tassat Login Token API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-get-tassat-login-token-api/) — The Get Tassat Login Token API from Western Alliance Bancorporation — 1 operation(s) for get tassat login token.
- [Western Alliance Bancorporation Get Token API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-get-token-api/) — The Get Token API from Western Alliance Bancorporation — 1 operation(s) for get token.
- [Western Alliance Bancorporation Get User Token API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-get-user-token-api/) — The Get User Token API from Western Alliance Bancorporation — 1 operation(s) for get user token.
- [Western Alliance Bancorporation Get WAB Token API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-get-wab-token-api/) — The Get WAB Token API from Western Alliance Bancorporation — 1 operation(s) for get wab token.
- [Western Alliance Bancorporation Health Check API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-health-check-api/) — The Health Check API from Western Alliance Bancorporation — 12 operation(s) for health check.
- [Western Alliance Bancorporation Intrabank Search API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-intrabank-search-api/) — On-demand lookup of intra-bank transfers; a fallback when the webhook is missed, not a replacement for it.
- [Western Alliance Bancorporation Redeem API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-redeem-api/) — The Redeem API from Western Alliance Bancorporation — 2 operation(s) for redeem.
- [Western Alliance Bancorporation Send API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-send-api/) — The Send API from Western Alliance Bancorporation — 2 operation(s) for send.
- [Western Alliance Bancorporation Transaction History Intraday API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-transaction-history-intraday-api/) — The Transaction History Intraday API from Western Alliance Bancorporation — 2 operation(s) for transaction history intraday.
- [Western Alliance Bancorporation Transaction History Priorday API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-transaction-history-priorday-api/) — The Transaction History Priorday API from Western Alliance Bancorporation — 2 operation(s) for transaction history priorday.
- [Western Alliance Bancorporation Transactions API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-transactions-api/) — The Transactions API from Western Alliance Bancorporation — 1 operation(s) for transactions.
- [Western Alliance Bancorporation Wallet balance API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-wallet-balance-api/) — The Wallet balance API from Western Alliance Bancorporation — 1 operation(s) for wallet balance.
- [Western Alliance Bancorporation Wallet Names API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-wallet-names-api/) — The Wallet Names API from Western Alliance Bancorporation — 1 operation(s) for wallet names.
- [Western Alliance Bancorporation Wires Request API](https://apis.io/apis/western-alliance-bancorporation/western-alliance-bancorporation-wires-request-api-api/) — The Wires Request API API from Western Alliance Bancorporation — 1 operation(s) for wires request api.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Western Alliance Bancorporation Webhooks](https://apis.io/asyncapis/western-alliance-bancorporation/western-alliance-bancorporation-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [wab-treasury-apis](https://apis.io/servers/western-alliance-bancorporation/wab-treasury-apis/)

#### Collections (15)

Postman and Open Collection request collections.

- [ACH EAPI | Beta](https://apis.io/collections/western-alliance-bancorporation/postman-western-alliance-bancorporation-ach-eapi-beta/)
- [All Account Balance API](https://apis.io/collections/western-alliance-bancorporation/postman-western-alliance-bancorporation-all-account-balance-api/)
- [All Account Intraday API](https://apis.io/collections/western-alliance-bancorporation/postman-western-alliance-bancorporation-all-account-intraday-api/)
- [All Account Priorday API](https://apis.io/collections/western-alliance-bancorporation/postman-western-alliance-bancorporation-all-account-priorday-api/)
- [Bank Statement API](https://apis.io/collections/western-alliance-bancorporation/postman-western-alliance-bancorporation-bank-statement-api/)
- [Book Transfer API](https://apis.io/collections/western-alliance-bancorporation/postman-western-alliance-bancorporation-book-transfer-api/)
- [Check image API](https://apis.io/collections/western-alliance-bancorporation/postman-western-alliance-bancorporation-check-image-api/)
- [Date Range Transactions API](https://apis.io/collections/western-alliance-bancorporation/postman-western-alliance-bancorporation-date-range-transactions-api/)
- [Single Account Balance API](https://apis.io/collections/western-alliance-bancorporation/postman-western-alliance-bancorporation-single-account-balance-api/)
- [Single Account Intraday API](https://apis.io/collections/western-alliance-bancorporation/postman-western-alliance-bancorporation-single-account-intraday-api/)
- [Single Account Priorday API](https://apis.io/collections/western-alliance-bancorporation/postman-western-alliance-bancorporation-single-account-priorday-api/)
- [Stop Payments API](https://apis.io/collections/western-alliance-bancorporation/postman-western-alliance-bancorporation-stop-payments-api/)
- [TassatPay EAPI | Beta](https://apis.io/collections/western-alliance-bancorporation/postman-western-alliance-bancorporation-tassatpay-eapi-beta/)
- [Token API](https://apis.io/collections/western-alliance-bancorporation/postman-western-alliance-bancorporation-token-api/)
- [Wires Request API](https://apis.io/collections/western-alliance-bancorporation/postman-western-alliance-bancorporation-wires-request-api/)

#### Overlays (16)

OpenAPI overlays, including conversational phrasing for each operation.

- [Western Alliance Bancorporation Ach Eapi Beta Overlay](https://apis.io/overlays/western-alliance-bancorporation/western-alliance-bancorporation-ach-eapi-beta-overlay/)
- [Western Alliance Bancorporation All Account Balance Api Overlay](https://apis.io/overlays/western-alliance-bancorporation/western-alliance-bancorporation-all-account-balance-api-overlay/)
- [Western Alliance Bancorporation All Account Intraday Api Overlay](https://apis.io/overlays/western-alliance-bancorporation/western-alliance-bancorporation-all-account-intraday-api-overlay/)
- [Western Alliance Bancorporation All Account Priorday Api Overlay](https://apis.io/overlays/western-alliance-bancorporation/western-alliance-bancorporation-all-account-priorday-api-overlay/)
- [Western Alliance Bancorporation Bank Statement Api Overlay](https://apis.io/overlays/western-alliance-bancorporation/western-alliance-bancorporation-bank-statement-api-overlay/)
- [Western Alliance Bancorporation Book Transfer Api Overlay](https://apis.io/overlays/western-alliance-bancorporation/western-alliance-bancorporation-book-transfer-api-overlay/)
- [Western Alliance Bancorporation Check Image Api Overlay](https://apis.io/overlays/western-alliance-bancorporation/western-alliance-bancorporation-check-image-api-overlay/)
- [Western Alliance Bancorporation Date Range Transactions Api Overlay](https://apis.io/overlays/western-alliance-bancorporation/western-alliance-bancorporation-date-range-transactions-api-overlay/)
- [Western Alliance Bancorporation Intrabank Transfer Api Overlay](https://apis.io/overlays/western-alliance-bancorporation/western-alliance-bancorporation-intrabank-transfer-api-overlay/)
- [Western Alliance Bancorporation Single Account Balance Api Overlay](https://apis.io/overlays/western-alliance-bancorporation/western-alliance-bancorporation-single-account-balance-api-overlay/)
- [Western Alliance Bancorporation Single Account Intraday Api Overlay](https://apis.io/overlays/western-alliance-bancorporation/western-alliance-bancorporation-single-account-intraday-api-overlay/)
- [Western Alliance Bancorporation Single Account Priorday Api Overlay](https://apis.io/overlays/western-alliance-bancorporation/western-alliance-bancorporation-single-account-priorday-api-overlay/)
- [Western Alliance Bancorporation Stop Payments Api Overlay](https://apis.io/overlays/western-alliance-bancorporation/western-alliance-bancorporation-stop-payments-api-overlay/)
- [Western Alliance Bancorporation Tassatpay Eapi Beta Overlay](https://apis.io/overlays/western-alliance-bancorporation/western-alliance-bancorporation-tassatpay-eapi-beta-overlay/)
- [Western Alliance Bancorporation Token Api Overlay](https://apis.io/overlays/western-alliance-bancorporation/western-alliance-bancorporation-token-api-overlay/)
- [Western Alliance Bancorporation Wires Request Api Overlay](https://apis.io/overlays/western-alliance-bancorporation/western-alliance-bancorporation-wires-request-api-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Western Alliance Bancorporation Authentication](https://apis.io/security/western-alliance-bancorporation/western-alliance-bancorporation-authentication/)
- [Western Alliance Bancorporation Domain Security](https://apis.io/security/western-alliance-bancorporation/western-alliance-bancorporation-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Western Alliance Bancorporation Plans Pricing](https://apis.io/plans/western-alliance-bancorporation/western-alliance-bancorporation-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Western Alliance Bancorporation Rate Limits](https://apis.io/rate-limits/western-alliance-bancorporation/western-alliance-bancorporation-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Western Alliance Bancorporation Finops](https://apis.io/finops/western-alliance-bancorporation/western-alliance-bancorporation-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.westernalliancebancorporation.com)
- [Documentation](https://developer.westernalliancebank.com/s/get-token-tutorial)
- [Getting started](https://developer.westernalliancebank.com/s/getting-started)
- [API reference](https://developer.westernalliancebank.com/s/apis)
- [Pricing](https://www.westernalliancebancorporation.com/sites/default/files/2025-05/api-services-terms-conditions.pdf)
- [Sign up](https://developer.westernalliancebank.com/s/login/SelfRegister)
- [Support](https://developer.westernalliancebank.com/s/forums)
- [Blog](https://developer.westernalliancebank.com/s/blog)
- [Terms of service](https://www.westernalliancebancorporation.com/sites/default/files/2025-05/api-services-terms-conditions.pdf)
- [Privacy policy](https://www.westernalliancebancorporation.com/privacy-legal-home/privacy-policy)
- [GitHub](https://github.com/westernalliancebank)
- [Status](https://developer.westernalliancebank.com/s/incident)

## API Evangelist rating

**Kin Score 46.1** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 70.5 |
| Contract quality | 21.0 |
| Contract governance | 18.2 |
| Operational transparency | 26.3 |
| Developer ergonomics | 70.8 |
| Access clarity | 65.8 |

**Agent readiness 48.8** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | served (partial credit) |
| Idempotency | documented (partial credit) |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | — |

**Regulatory alignment 30.7** — Banking & Open Finance

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/western-alliance-bancorporation/](https://apis.io/providers/western-alliance-bancorporation/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Western Alliance Bancorporation: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/western-alliance-bancorporation/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
