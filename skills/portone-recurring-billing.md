---
name: Charge a customer on file with a PortOne billing key
description: Issue a billing key, charge it immediately for card-on-file payments, and reserve future recurring charges with the payment scheduler.
api: openapi/portone-openapi.yml
operations: [issueBillingKey, payWithBillingKey, createPaymentSchedule, deleteBillingKey]
method: generated
generated: '2026-07-17'
---

# Recurring / card-on-file billing with PortOne (V2)

Base URL `https://api.portone.io`. Auth: `Authorization: PortOne <API_SECRET>`.

## Steps
1. **Issue a billing key** — call `issueBillingKey` with the customer's payment method and the `channelKey` of the PG channel to route through. On success you receive a `billingKey`. (The hosted UI path uses `@portone/browser-sdk`; the server path uses this operation.)
2. **Charge immediately** — call `payWithBillingKey` with a merchant-assigned `paymentId`, the `billingKey`, `orderName`, and `amount` (KRW minor units). Because `paymentId` is client-assigned, retrying the same id is idempotent — a duplicate returns `ALREADY_PAID` / `ALREADY_PAID_OR_WAITING` (409); treat as success.
3. **Reserve future charges** — call `createPaymentSchedule` with the `billingKey` and a future `timeToPay` to schedule recurring/installment charges. Query with `getPaymentSchedules`; revoke with `revokePaymentSchedules`.
4. **Retire a token** — call `deleteBillingKey` when the customer removes the payment method. A deleted key returns `BILLING_KEY_NOT_FOUND` (404) on reuse.

## Events
Subscribe to `BillingKey.Issued`, `BillingKey.Updated`, `BillingKey.Failed`, `BillingKey.Deleted`, and `Transaction.Paid` webhooks to keep your ledger in sync (`asyncapi/portone-webhooks.yml`). Verify signatures with the Standard Webhooks helper in `@portone/server-sdk`.

## Errors
`{ type, message }` envelope; see `errors/portone-problem-types.yml`. Downstream declines surface as `PG_PROVIDER` (502) with `pgCode`/`pgMessage` passthrough (`errors/portone-decline-codes.yml`).
