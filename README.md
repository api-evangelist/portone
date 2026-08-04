# PortOne (portone)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

PortOne (formerly Iamport) is a Korea-based payment orchestration platform that lets online businesses integrate one API to reach 100+ Korean and global payment methods and PSPs. The V2 REST API (`api.portone.io`) covers payments, billing keys, scheduled/recurring payments, identity verification, cash receipts, B2B tax invoices, and partner settlement, with the legacy V1 API still served at `api.iamport.kr`.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/portone/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/portone/refs/heads/main/apis.yml)

## Tags

- Payments
- Payment Orchestration
- Fintech
- Korea
- Billing
- Identity Verification

## Timestamps

- **Created:** 2026-07-17
- **Modified:** 2026-07-17

## APIs

### PortOne Payments API (V2)

Core payment lifecycle over api.portone.io — single/bulk payment lookup, manual (keyed) payments, capture, cancellation, escrow, virtual-account close, and cash-receipt issuance, keyed by merchant-supplied paymentId.

- **Human URL:** [https://developers.portone.io/api/rest-v2/payment](https://developers.portone.io/api/rest-v2/payment)
- **Base URL:** `https://api.portone.io`

#### Tags

- Payments
- Cancellation
- Escrow
- Virtual Account

#### Properties

- [Documentation](https://developers.portone.io/api/rest-v2/payment)
- [API Reference](https://developers.portone.io/api/rest-v2)
- [OpenAPI](openapi/portone-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/portone.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### PortOne Billing Keys API (V2)

Issue, look up, and delete billing keys and charge non-authenticated (card-on-file) payments with them for subscriptions and recurring billing.

- **Human URL:** [https://developers.portone.io/api/rest-v2/payment.billingKey](https://developers.portone.io/api/rest-v2/payment.billingKey)
- **Base URL:** `https://api.portone.io`

#### Tags

- Billing
- Recurring
- Tokenization

#### Properties

- [Documentation](https://developers.portone.io/api/rest-v2/payment.billingKey)
- [OpenAPI](openapi/portone-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/portone.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### PortOne Payment Schedule API (V2)

Reserve future billing-key charges and query or revoke scheduled payments for subscription and installment workflows.

- **Human URL:** [https://developers.portone.io/api/rest-v2/paymentSchedule](https://developers.portone.io/api/rest-v2/paymentSchedule)
- **Base URL:** `https://api.portone.io`

#### Tags

- Scheduling
- Recurring
- Reservations

#### Properties

- [Documentation](https://developers.portone.io/api/rest-v2/paymentSchedule)
- [OpenAPI](openapi/portone-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### PortOne Identity Verification API (V2)

Korean identity verification (bon-in injung / 본인인증) — send and confirm verification, and retrieve verified holder data via carrier and credit-authority channels.

- **Human URL:** [https://developers.portone.io/api/rest-v2/identityVerification](https://developers.portone.io/api/rest-v2/identityVerification)
- **Base URL:** `https://api.portone.io`

#### Tags

- Identity Verification
- KYC
- Bon-in Injung

#### Properties

- [Documentation](https://developers.portone.io/api/rest-v2/identityVerification)
- [OpenAPI](openapi/portone-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### PortOne Cash Receipts API (V2)

Issue, cancel, and look up Korean cash receipts (hyeongeum yeongsujeung / 현금영수증) required for tax-deductible cash and transfer settlements.

- **Human URL:** [https://developers.portone.io/api/rest-v2/cashReceipt](https://developers.portone.io/api/rest-v2/cashReceipt)
- **Base URL:** `https://api.portone.io`

#### Tags

- Cash Receipt
- Tax
- Hyeongeum Yeongsujeung

#### Properties

- [Documentation](https://developers.portone.io/api/rest-v2/cashReceipt)
- [OpenAPI](openapi/portone-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### PortOne B2B Tax Invoice API (V2)

Electronic tax invoice (segyegyesanseo / 세금계산서) issuance, cancellation, bulk operations, counterparty (member company) lookup, and NTS reporting for B2B settlement.

- **Human URL:** [https://developers.portone.io/api/rest-v2/b2b](https://developers.portone.io/api/rest-v2/b2b)
- **Base URL:** `https://api.portone.io`

#### Tags

- B2B
- Tax Invoice
- Segyegyesanseo

#### Properties

- [Documentation](https://developers.portone.io/api/rest-v2/b2b)
- [OpenAPI](openapi/portone-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### PortOne Platform Partner Settlement API (V2)

Marketplace/platform settlement engine — manage partners, contracts, policies, transfers, order-sheets, and payouts for splitting funds across sellers.

- **Human URL:** [https://developers.portone.io/api/rest-v2/platform](https://developers.portone.io/api/rest-v2/platform)
- **Base URL:** `https://api.portone.io`

#### Tags

- Platform
- Settlement
- Marketplace

#### Properties

- [Documentation](https://developers.portone.io/api/rest-v2/platform)
- [OpenAPI](openapi/portone-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### PortOne Payment Sessions & Checkout API (V2)

Create and manage server-side payment sessions and checkout profiles that back PortOne's hosted/SDK checkout experience.

- **Human URL:** [https://developers.portone.io/api/rest-v2/paymentSession](https://developers.portone.io/api/rest-v2/paymentSession)
- **Base URL:** `https://api.portone.io`

#### Tags

- Checkout
- Sessions
- Hosted Payment

#### Properties

- [Documentation](https://developers.portone.io/api/rest-v2/paymentSession)
- [OpenAPI](openapi/portone-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### PortOne Payment Reconciliation API (V2)

Retrieve payment reconciliation rounds and line items for matching PortOne transaction records against PSP settlement statements.

- **Human URL:** [https://developers.portone.io/api/rest-v2](https://developers.portone.io/api/rest-v2)
- **Base URL:** `https://api.portone.io`

#### Tags

- Reconciliation
- Reporting
- Ledger

#### Properties

- [API Reference](https://developers.portone.io/api/rest-v2)
- [OpenAPI](openapi/portone-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### PortOne REST API (V1, legacy Iamport)

Legacy V1 (Iamport) REST API on api.iamport.kr — token-authenticated (POST /users/getToken with imp_key/imp_secret) payment lookup, cancellation, non-authenticated and scheduled payments, virtual accounts, and identity verification. Maintained for existing integrations; new integrations are directed to V2.

- **Human URL:** [https://developers.portone.io/api/rest-v1](https://developers.portone.io/api/rest-v1)
- **Base URL:** `https://api.iamport.kr`

#### Tags

- Payments
- Legacy
- Iamport

#### Properties

- [Documentation](https://developers.portone.io/api/rest-v1)
- [API Reference](https://developers.portone.io/api/rest-v1/payment)

## Common Properties

- [Agentic Access](agentic-access/portone-agentic-access.yml)
- [Trust Center](security/portone-trust-center.yml)
- [Vulnerability Disclosure](security/portone-vulnerability-disclosure.yml)
- [Domain Security](security/portone-domain-security.yml)
- [Authentication](authentication/portone-authentication.yml)
- [GitHub Organization](https://github.com/portone-io)
- [LinkedIn](https://www.linkedin.com/company/portoneglobal)
- [Website](https://portone.io/)
- [Documentation](https://developers.portone.io/)
- [Plans](plans/portone-plans-pricing.yml)
- [Rate Limits](rate-limits/portone-rate-limits.yml)
- [Fin Ops](finops/portone-finops.yml)
- [Blog](https://developers.portone.io/opi/ko/support/release-note)

## Notes

- **Rebrand:** PortOne is the rebrand of **Iamport** (아임포트). The legacy V1 API is still served under the `api.iamport.kr` host and the original GitHub org is [github.com/iamport](https://github.com/iamport); current repos live at [github.com/portone-io](https://github.com/portone-io).
- **Authentication (V2):** `Authorization: PortOne <API_SECRET>` (custom scheme keyword `PortOne`, not `Bearer`), or a short-lived JWT via `Authorization: Bearer <accessToken>`.
- **Authentication (V1):** two-step token exchange — `POST /users/getToken` with `imp_key` + `imp_secret`.
- **Async model:** payment status changes are delivered via HTTP **webhooks** (outbound POST, with a resend-webhook operation), not WebSocket or SSE.
- **Agent tooling:** PortOne publishes an official MCP server ([github.com/portone-io/mcp-server](https://github.com/portone-io/mcp-server)) and server SDKs ([github.com/portone-io/server-sdk](https://github.com/portone-io/server-sdk)).
- **Currency:** KRW for Korea settlement; multi-currency supported through global PSPs.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
