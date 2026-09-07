## 2026-09-07T13:18Z — pass 002 — Gmail and Google Calendar native reuse assessment

Disposition: **Gmail 6/10 HOLD; Calendar 6/10 HOLD. No new-build recommendation.** Two provider/job assessments; completed Gmail supply research reused, not recreated.

### Steering and inventory carried forward

Read current shared Linear ledger before this pass. Voice's 2026-09-07 authenticated installed-app observation is attributed evidence, not an independent inspection here: Standard, Custom, Mhoo Finance (Local), WhatsApp NPM, Last contact NPM, Linear NPM, Codex OAuth. Installation does not establish account connection, native feature coverage or working sync. Linear/WhatsApp remain eligible for repair/extension assessment, never duplicate builds. Their usefulness clarification supersedes “health only.” Unknown deployed/native inventory means HOLD.

Expanded backlog preserved: LinkedIn, Indeed (reuse MHO-137), Facebook, Instagram, Google Business Profile, RSS, YouTube, TikTok, Higgsfield, X, Twilio and Mailchimp. Separate reading/analytics, publishing, recruiting, messaging and generation jobs and their costs/permissions. No new authority inferred.

### Job and score matrix

Score order: workflow utility / missing native capability / maintained licensed reuse / API-auth-sync reliability / simplicity.

| Candidate/job | Expected outcome and evidence | Scores | Disposition and gap class |
| --- | --- | --- | --- |
| Gmail relationship history | Existing authorized mailbox changes appear on the correct Twenty relationship records without duplicate messages or cross-Workspace visibility. [MHO-75](https://linear.app/mhoo/issue/MHO-75/supply-gmail-installed-plugin-and-official-mail-api-contract) is Done and links [prior packet PR29](https://github.com/mhoo-os/mhoo/pull/29); its scope excludes inbox reads and writes. Current committed native source has history pagination for additions, deletions and label changes. No live mailbox examined. | 2 / 0 / 1 / 1 / 2 = **6/10** | HOLD new integration. Native supply exists; setup/authorization versus broken behavior remains UNKNOWN without a failing journey/receipt. No missing feature demonstrated. |
| Google Calendar event context | Existing selected calendar events, changes and cancellations appear once on intended records; recurrence/timezone and reconnect preserve identity. Native source has token/page handling and an explicit 410 branch. No live events examined. | 2 / 0 / 1 / 1 / 2 = **6/10** | HOLD new integration. Native supply exists; deployed coverage, selected calendars and setup-versus-defect remain UNKNOWN. |

Utility derives from the owner's first-ten priorities. Gap=0 means no demonstrated need for duplicate source, not proof every user job works. Reuse=1 recognizes existing licensed source but does not approve extracting server code into an App. Reliability=1 reflects documented protocols without installed acceptance. Simplicity=2 applies to reuse planning, not an estimate of an unobserved repair.

### Exact native source and important correction

Inspected immutable commit **5f6cdd318b6a0d5db85b1a12f54e2aaffb65b035** via git show in /Users/mhoooo/projects/mhoo-os/mhoo-twenty-next, not dirty working-file contents. Source inventory is not deployed build evidence.

- [Gmail history service](https://github.com/mhoo-os/mhoo-twenty-next/blob/5f6cdd318b6a0d5db85b1a12f54e2aaffb65b035/packages/twenty-server/src/modules/messaging/message-import-manager/drivers/gmail/services/gmail-get-history.service.ts): paginates users.history.list and tracks historyId.
- [Calendar fetch service](https://github.com/mhoo-os/mhoo-twenty-next/blob/5f6cdd318b6a0d5db85b1a12f54e2aaffb65b035/packages/twenty-server/src/modules/calendar/calendar-event-import-manager/drivers/google-calendar/services/google-calendar-get-events.service.ts): connected-account OAuth client, syncToken/pageToken and explicit 410 handling. End-to-end recovery was not tested.
- [Calendar create service](https://github.com/mhoo-os/mhoo-twenty-next/blob/5f6cdd318b6a0d5db85b1a12f54e2aaffb65b035/packages/twenty-server/src/modules/calendar/calendar-event-creation-manager/drivers/google-calendar/services/google-calendar-create-event.service.ts): calls events.insert; sendUpdates depends on sendInvitations. This conflicts with treating pass001's older Twenty “cannot book meetings” documentation as complete current source inventory. It does NOT prove UI exposure, deployed availability or a public booking-page workflow. Cal.com remains HOLD, with its gap rationale qualified by this correction.
- [Exact repository LICENSE](https://github.com/mhoo-os/mhoo-twenty-next/blob/5f6cdd318b6a0d5db85b1a12f54e2aaffb65b035/LICENSE): server generally AGPLv3 with Twenty Application Exception, Enterprise-marked files commercial; named toolkit/App packages MIT. Inspected service headers have no Enterprise marker. Reusing native behavior does not justify relabeling server source MIT. Dependencies and any extraction need specific review.

### Official provider and directory evidence, checked 2026-09-07

[Zapier Gmail](https://zapier.com/apps/gmail/integrations) and [Zapier Calendar](https://zapier.com/apps/google-calendar/integrations) provide discovery directories, not proof an additional adapter is needed. Native source is the preferred reusable implementation for these jobs. Prior pass001's exact Pipedream PSAL1.0, Activepieces community MIT and Nango ELv2 license comparison is retained; no unrelated template adopted or unchanged license research repeated.

- [Gmail history contract](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.history/list): stale/invalid history IDs can return 404 and require full synchronization. [Gmail scopes](https://developers.google.com/workspace/gmail/api/auth/scopes): least privilege must match operation; read access can still involve restricted scopes and verification obligations. Actual client approval/scopes unverified. General Gmail sync guide retrieval timed out; the official method reference supplied the needed evidence.
- [Calendar incremental synchronization](https://developers.google.com/workspace/calendar/api/guides/sync): keep the same sync query across pages, persist final-page token, process deleted entries, and reset/reconcile on 410. Its code samples are Apache 2.0; prose CC BY 4.0 per page footer. No sample imported.
- [Calendar OAuth scopes](https://developers.google.com/workspace/calendar/api/auth): read-only event scope is distinct from write capabilities; actual configured grant not examined.
- [Twenty overview](https://docs.twenty.com/user-guide/calendar-emails/overview) documents native email/calendar sync. Documentation cadence is not an observed runtime service level.

### Gates, owner and next action

Security, permissions and native credential-custody acceptance: **UNKNOWN, therefore HOLD**, regardless of numeric total. Do not call provider endpoints to fill those gaps under this research authority. No paid automation or parallel vault is justified; no cost estimate for a new service is made.

Proposed planning path: existing native head should reuse existing source/runtime receipts, identify one concrete failing user journey if any, then classify missing configuration/grant, defect, or additional feature before scoping repair. For Gmail check mailbox identity, message/history pagination, reconnect and isolated visibility; for Calendar check selected-calendar coverage, recurring/cancelled events, timezone identity and 410 recovery. These are future acceptance questions, not test dispatches. Require exact deployed commit and authorized connection-state evidence; do not request tokens.

Primary issue for this pass: none; MHO-75 is historical evidence only. Implementation-owning repository: existing mhoo-twenty-next native capability; owning head 01a07aa7-944a-70c3-bf77-d51b9fc766f2, no new worker or acceptance assumed. Coordination stays with Connectors head 01a07aa6-6d60-71f0-92e8-87c7c1561d5c. Missing deployed/connection receipts belong with native head; cross-system authority remains mhoo, operations infrastructure. Clover remains with its retained owner.

Research base f744f91b861923e4cfb975ddab2499074cc1a524; instructions d60f3dcd3e72a741bc65ac340d1734aa6680b7d9 / local AGENTS.md, previously read and unchanged. Live origin default main remains d60f3dc. Initial local branch clean; retained worktrees unchanged. Existing operational ledger /Users/mhoooo/Documents/Codex/2026-09-06/mhoo-coordinator/checkpoint.json; shared Linear document remains canonical research coordination. No PR/push/merge. Authorized next step: append sanitized findings and hand off; no provider data, implementation, installs, sends, schedules or Dark Factory work. Reopen these jobs only on changed evidence; next priority is reuse Clover receipts, then selected Drive/Sheets assessment.
