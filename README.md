# PortOne (portone)

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
