---
name: Run Korean identity verification with PortOne
description: Send, confirm, and retrieve a Korean bon-in-injung (본인인증) identity verification via carrier/credit-authority channels.
api: openapi/portone-openapi.yml
operations: [sendIdentityVerification, confirmIdentityVerification, resendIdentityVerification, getIdentityVerification]
method: generated
generated: '2026-07-17'
---

# Korean identity verification (본인인증) with PortOne (V2)

Base URL `https://api.portone.io`. Auth: `Authorization: PortOne <API_SECRET>`.

## Steps
1. **Send the verification** — call `sendIdentityVerification` with a merchant-assigned `identityVerificationId`, the `channelKey` of a configured identity-verification channel, and the holder's name/phone/carrier details. This dispatches the OTP/authentication challenge.
2. **Confirm** — call `confirmIdentityVerification` with the same `identityVerificationId` and the OTP the user received. On success the record moves to a verified state; confirming an already-verified record returns `IDENTITY_VERIFICATION_ALREADY_VERIFIED` (409).
3. **Resend if needed** — call `resendIdentityVerification` to re-dispatch the challenge. Excess attempts return `MAX_TRANSACTION_COUNT_REACHED` (400).
4. **Read verified data** — call `getIdentityVerification` with the `identityVerificationId` to retrieve the verified holder information. A missing id returns `IDENTITY_VERIFICATION_NOT_FOUND` (404).

## Notes
- `identityVerificationId` is client-assigned, so retries are idempotent against the same record.
- Errors use the `{ type, message }` envelope (`errors/portone-problem-types.yml`); PIPA/personal-data handling applies to the returned holder fields.
