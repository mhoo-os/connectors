## 2026-09-08 08:27 Bangkok — pass 014 — Twilio and Mailchimp

**Twilio SMS status evidence 5/10 HOLD; Mailchimp audience suppression evidence 4/10 HOLD.** Jobs: explain an existing SMS delivery failure; show whether a contact opted out before an operator considers marketing. Exact demand/account unknown. Voice calls, WhatsApp replacement, contact writes and campaign sending are separate jobs, not authorized effects.

Scores utility/native gap/maintained licensed reuse/API-auth-sync/simplicity: Twilio 1/1/1/1/1=5; Mailchimp 1/1/0/1/1=4. Current native inventory, security, credential custody and exact account permissions unpassed; no new-build recommendation.

### Reused new native receipt

Shared ledger now attributes native Settings receipt: WhatsApp UUID a2c8ca18-0830-46dd-bd4a-6b49dde06e66 is @pixelinfinito/twenty-app-whatsapp0.1.2, eight objects/32 functions, with whatsappMessages status/timestamps/errors and wa-status-processor declared. Source/tarball equality, license and behavior remain unproved. Existing-message status is already structurally represented; do not create a duplicate model or infer missing functionality. Native head retains source/provenance follow-up. MHO-267/PR41 remains independently owned; this research does not take over either lane.

### Twilio

[Status callbacks](https://www.twilio.com/docs/messaging/guides/track-outbound-message-status) can arrive out of order and parameters evolve. Future source acceptance must preserve Message SID/channel, original status/error and observation time, validate signatures against the actual request, and avoid regressing state from late callbacks. This is protocol evidence, not a live message or delivery receipt.

[Official Node SDK](https://github.com/twilio/twilio-node/tree/c8a4c27de84ec3838726da878cb9ca04a438ec59), latest observed2026-08-12, has pinned MIT LICENSE. Exact adapter/dependencies not audited. Account/subaccount binding and read-limited credential route remain unresolved; no keys created.

[US SMS pricing](https://www.twilio.com/en-us/sms/pricing/us) charges by segment with carrier fees, number rental and applicable onboarding charges; failed messages can also incur a processing fee. This is US-only discovery, not a quote for MHOO's unknown destination. Country/sender approval, consent, volume and budget must be established for any future send work. Voice pricing/recording permissions not qualified.

### Mailchimp

[Audience webhook guide](https://mailchimp.com/developer/marketing/guides/sync-audience-data-webhooks/) now documents optional HMAC-SHA256 signatures over timestamp plus raw body, X-Mailchimp-Signature and a five-minute freshness check, using a one-time signing secret. Do not rely on older claims that audience webhooks cannot be signed. Guide says callbacks time out after10seconds and retry over75minutes; deliveries may still be dropped/disabled. Signed availability on an actual account and reconciliation remain unproved. Never infer renewed consent from a stale contact import.

[Fundamentals](https://mailchimp.com/developer/marketing/docs/fundamentals/) recommends OAuth for others' accounts; access follows authorizing-user role, token revokes if user removed, and API limits include10 concurrent connections. A read-only job is not proof of a read-only token. [Marketing pricing](https://mailchimp.com/pricing/marketing/) requires the actual contact/send/feature selection before quoting cost; account tier and report access unverified.

[Official Node library](https://github.com/mailchimp/mailchimp-marketing-node/tree/7c1edd292e2d4732a0ea209de6b6dd38f968bf9d) latest observed commit2022-11-02; LICENSE is a custom Mailchimp Client Library License Agreement, not MIT. Maintenance and license-use gate unqualified. Keep audience identity, subscription source/time and unsubscribe state distinct from Twenty contact identity. Reporting and campaign creation/sending need separate assessment.

### Custody and next step

Primary issue none for these candidates; implementation-owning repo/head/worker unassigned. Default earned App-local scope routes to mhoo-twenty-next/native head01a07aa7-944a-70c3-bf77-d51b9fc766f2 for acceptance. Research head01a07aa6-6d60-71f0-92e8-87c7c1561d5c owns missing job/account/budget decisions. Twenty owns identity/Connections/permissions; existing Clover worker unchanged.

Basef602b0e20db13fc6de50fdd9831f8d9139e6242c initially clean. Shared ledger read first. User-supplied replacement AGENTS instructions adopted this turn including standing browser-auth authority; committed repository authority receipt remains d60f3dcd3e72a741bc65ac340d1734aa6680b7d9, not proof the new supplied text was committed. Prior origin/default/worktree receipts reused. Existing reading paths /Users/mhoooo/Documents/Codex/MHOO-DESK-SETUP.md and /Users/mhoooo/Documents/Codex/2026-09-06/mhoo-coordinator/checkpoint.json retained. No login needed.

Local unpublished documentation/no PR. No provider data, credentials, installation, code, sends, contact writes, webhook creation, fees, new issues/workers or schedule changes. Next authorized action append findings/send head; expanded candidate pass complete. Subsequent research should follow changed owner evidence or a concrete unqualified job, avoiding repeated unchanged HOLD probes.
