# Resume without duplicates

Keep a private checkpoint of the last verified stage: connected, inbox verified, email submitted, verified, consent complete, onboarding, signed in. Store no message body, authentication link, code, cookie, credential, or browser/session metadata. Reinspect current state when resuming; the checkpoint is evidence to investigate, not proof of the present state.

- **Connection missing or revoked:** Ask the owner to connect through the supported authorization UI. Continue only after a harmless inbox read succeeds. Never retrieve tokens from files or substitute another user's mailbox.
- **Creation timed out:** List/get first. Reuse the same stable client identifier for the same logical inbox. If reconciliation cannot establish whether the inbox exists, report uncertainty and stop before a new creation.
- **Email delayed:** Refresh only the intended mailbox at a reasonable interval within the interactive task. Check the exact submitted address. Avoid repeated resend clicks; after a short delivery wait and one user-approved resend, report persistent delivery failure. Do not rotate addresses to evade a service restriction.
- **Link expired or already used:** Inspect the current browser and mailbox first. If needed, request one fresh verification email through the current signup UI. Correlate it to that request. Never retry old links indefinitely.
- **Duplicate/existing account:** Ask whether the user intends to sign in or recover the account. Do not silently create another inbox or change the account identity.
- **CAPTCHA, access denial, unsupported region, or provider rejection:** Stop at the specific blocker. Use a supported user handoff where appropriate. Do not spoof eligibility, cycle proxies, or attempt stealth automation.
- **Unexpected terms or charges:** Present the changed requirement and its link or amount. Await user direction; authorization for free signup does not cover a purchase.
- **Unknown identity, phone, or age requirement:** Ask the user for the required truthful information or hand off. Never fabricate it or use somebody else's identity.
- **Training toggle absent:** Do not claim it is off. Explain that the preference could not be verified and use official settings/help if available.
- **Browser closes or navigation changes:** Reopen the official site and inspect. Do not replay the whole flow blindly.

Stop safely with the verified stage, exact blocker, and smallest next action. Avoid exposing authentication URLs or unnecessary account identifiers in the report.
