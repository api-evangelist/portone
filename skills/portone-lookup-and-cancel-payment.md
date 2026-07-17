---
name: Look up and cancel a PortOne payment
description: Retrieve a payment by its merchant-assigned paymentId and issue a full or partial cancellation/refund, handling PortOne's amount-consistency rules.
api: openapi/portone-openapi.yml
operations: [getPayment, cancelPayment]
method: generated
generated: '2026-07-17'
---

# Look up and cancel a PortOne payment (V2)

Use the PortOne V2 REST API at `https://api.portone.io`.

## Auth
Send `Authorization: PortOne <API_SECRET>` (or `Authorization: Bearer <JWT>` from `POST /login/api-secret`). See `authentication/portone-authentication.yml`.

## Steps
1. **Look up the payment** — call `getPayment` with the merchant-assigned `paymentId`. Read `status` (READY, PAID, PARTIAL_CANCELLED, CANCELLED, VIRTUAL_ACCOUNT_ISSUED, FAILED). A missing id returns `PAYMENT_NOT_FOUND` (404).
2. **Cancel or refund** — call `cancelPayment` with `paymentId`. For a full cancel, omit the amount. For a partial refund, pass the `amount` (KRW minor units) plus any `taxFreeAmount`/`vatAmount` splits.
3. **Respect cancellable-amount rules** — if the amount exceeds the remaining balance you get `CANCEL_AMOUNT_EXCEEDS_CANCELLABLE_AMOUNT` (409); inconsistent tax splits give `SUM_OF_PARTS_EXCEEDS_CANCEL_AMOUNT` or `CANCELLABLE_AMOUNT_CONSISTENCY_BROKEN` (409). Re-read the payment with `getPayment` to recompute the cancellable balance.
4. **Idempotency** — `cancelPayment` on an already-cancelled payment returns `PAYMENT_ALREADY_CANCELLED` (409); treat as terminal, not a new failure.

## Error handling
Errors are `{ type, message }` with the HTTP status carried on the response (see `errors/portone-problem-types.yml`). A `PG_PROVIDER` (502) means the downstream PG rejected the cancel — inspect `pgCode`/`pgMessage`.

## Async
Cancellations may complete asynchronously; subscribe to `Transaction.CancelPending`, `Transaction.PartialCancelled`, and `Transaction.Cancelled` webhooks (`asyncapi/portone-webhooks.yml`) rather than assuming synchronous completion.
