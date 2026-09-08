# Integration research ledger

Latest: [pass 013 — Higgsfield and X](integration-research-pass-013.md).

Latest: [pass 012 — YouTube and TikTok performance](integration-research-pass-012.md).

Latest: [pass 011 — selected RSS/Atom monitoring](integration-research-pass-011.md).

Latest: [pass 010 — Google Business Profile reviews](integration-research-pass-010.md).

Latest: [pass 009 — Facebook/Instagram analytics gates](integration-research-pass-009.md).

Latest: [pass 008 — LinkedIn/Indeed recruiting access](integration-research-pass-008.md).

Latest: [pass 007 — existing WhatsApp app assessment](integration-research-pass-007.md).

Latest: [pass 006 — LINE OA incoming context](integration-research-pass-006.md).

Latest: [pass 005 — Plaid existing-demand assessment](integration-research-pass-005.md).

Latest: [pass 004 — existing Linear usefulness and GitHub evidence](integration-research-pass-004.md).

Latest: [pass 003 — Drive/Sheets and Clover receipt reuse](integration-research-pass-003.md).

Latest: [pass 002 — Gmail/Calendar native reuse and owner corrections](integration-research-pass-002.md). This qualifies pass 001's calendar gap claim; historical findings below are retained.

## 2026-09-07 — pass 001 — Cal.com booking evidence

**Decision: HOLD, 5/10. One candidate researched. No implementation recommendation.**
Potential use: preserve a prospect's booked, cancelled or rescheduled appointment against a Twenty opportunity, reducing manual follow-up. This is a hypothesis for MHOO sales/onboarding, not confirmed demand or an existing Cal.com account.

### Scope, custody and provenance

- Primary issue: none; parent research dispatch 01a078c0-dfad-7d83-bf3a-56510787d107 to task 01a07bcc-2cdc-7101-998a-ad21cb1c59ea.
- Research owner: Connectors head 01a07aa6-6d60-71f0-92e8-87c7c1561d5c; coordination capped at Astra Low. Retained implementation worker: none for this candidate. Clover workers unchanged.
- Implementation owner: unassigned; owning native Twenty App in mhoo-twenty-next is the default proposal, subject to its head accepting demand/scope. No shared adapter earned here.
- Source base/head and authoritative AGENTS: d60f3dcd3e72a741bc65ac340d1734aa6680b7d9, read from this worktree's AGENTS.md; [merged instructions PR9](https://github.com/mhoo-os/connectors/pull/9). Origin git@github-mhoo:mhoo-os/connectors.git; live remote HEAD main at that same commit. Initial worktree clean/detached.
- Reading path: AGENTS.md → /Users/mhoooo/Documents/Codex/MHOO-DESK-SETUP.md → relevant coordinator checkpoint/registry entries → repository README, docs and boundary notes → existing head and research document.
- Existing operational ledger: /Users/mhoooo/Documents/Codex/2026-09-06/mhoo-coordinator/checkpoint.json.
- [Shared research document](https://linear.app/mhoo/document/connectors-integration-research-ledger-93c38f19fb03) read before publishing; prior supply inventory preserved. Completed MHO-75/86/96/105/137 not repeated. MHO-127 and historical MHO-195 not reassigned. No open/new GitHub issue found in repository issue listing.
- Other worktrees: main and retained desk-setup branch at d60f3dc; finance-context detached at 04fa1dc is older inventory, not declared safe to delete. No branches reset or deleted.
- Authorized next step: preserve this documentation and send to existing head. No candidate implementation, provider account/API calls, installs, payments, credentials, runtime, schedule or Dark Factory revival.

### Scores (0–2 each)

| Criterion | Score | Evidence and limit |
| --- | --- | --- |
| Concrete MHOO usefulness | 1 | Plausible onboarding/sales follow-up; no accepted user demand or measured manual burden. |
| Gap versus native Twenty/installed apps | 1 | [Twenty booking documentation](https://docs.twenty.com/user-guide/calendar-emails/how-tos/can-i-book-meetings-from-twenty) says calendar sync does not create meetings. [Calendar capability](https://docs.twenty.com/user-guide/calendar-emails/capabilities/calendar) already covers event context. Booking lifecycle may add value, but adding a booking link may suffice. No Cal.com tool appeared in current task tool metadata; this does not establish Workspace installation inventory. |
| Maintained, suitably licensed reusable source | 1 | Activepieces community path has MIT coverage and recent change, but piece-level security gaps; other source licenses have restrictions. |
| API/auth/sync reliability | 1 | Official scoped OAuth, signed webhooks and cursor pagination exist; replay, tenant isolation, version compatibility and deletion coverage unproved. |
| Low implementation/operating burden | 1 | Narrow App-local read projection could be small; OAuth acceptance, webhook receiver and reconciliation add burden. Need to prove that existing calendar sync plus booking link is insufficient. |
| **Total** | **5/10** | **HOLD; mandatory security, permission and custody gates unresolved.** |

### Directory and source comparison

[Zapier Cal.com directory](https://zapier.com/apps/calcom/integrations) establishes a scheduling/booking integration and CRM pairings; it is discovery evidence only, not reusable code, MHOO demand, security or license acceptance.

Official GitHub snapshots observed on 2026-09-07:

| Source | Exact snapshot and inspected path | Finding |
| --- | --- | --- |
| Pipedream | [Cal.com app](https://github.com/PipedreamHQ/pipedream/blob/7102eebbfce8476b4e3d6d3fc7473ea16cb4f0f8/components/cal_com/cal_com.app.mjs), [license](https://github.com/PipedreamHQ/pipedream/blob/7102eebbfce8476b4e3d6d3fc7473ea16cb4f0f8/LICENSE) | Pipedream Source Available License 1.0 includes commercial-use restrictions; no permissive reuse accepted. Package has no license declaration; components/LICENSE returned 404. App uses API-key auth, retries and booking API version 2026-02-25. List method does not itself drain pages. |
| Activepieces | [piece](https://github.com/activepieces/activepieces/blob/0f2afd840e865601d222fab5e2a8bb53fe0f5064/packages/pieces/community/cal-com/src/index.ts), [webhook helper](https://github.com/activepieces/activepieces/blob/0f2afd840e865601d222fab5e2a8bb53fe0f5064/packages/pieces/community/cal-com/src/lib/triggers/register-webhook.ts), [license](https://github.com/activepieces/activepieces/blob/0f2afd840e865601d222fab5e2a8bb53fe0f5064/LICENSE) | MIT Expat applies to community source, subject to third-party terms; enterprise paths excluded. API-key trigger piece; no actions. Inspected helper registers/deletes webhooks, supplies no signing secret and returns payload body without piece-level verification. Framework-wide guarantees not audited, so this is a reuse gate, not a claim of an exploitable service. Last path change 71d407e5c8910e6596f6c7da8157ce131fb9c85b, 2026-08-21. |
| Nango | [booking sync](https://github.com/NangoHQ/integration-templates/blob/1efbe17acea944b505ac50b3453862788b5c4b5b/integrations/cal-com-v2/syncs/bookings.ts), [license](https://github.com/NangoHQ/integration-templates/blob/1efbe17acea944b505ac50b3453862788b5c4b5b/LICENSE) | Elastic License 2.0, not MIT; hosted/managed-service restriction needs use-specific review. Sync uses current 2026-05-01 cursor API, UID, update timestamps and checkpoints. Numerous actions/tests listed; not executed. It depends on Nango proxy/storage; adopting that runtime/custody is not authorized. Last path change 91ecf3e04fb0523ec534d175e70c40244dc1bde3, 2026-08-23. |

Recent path changes establish activity, not support quality. Stars were not used. Licenses above apply to inspected source scopes, not blanket approval of dependencies or Cal.com server distribution; no server code proposed.

### Provider evidence and unresolved gates

- [API v2 introduction](https://cal.com/docs/api-reference/v2/introduction): OAuth/API keys; legacy Platform offering is deprecated/maintenance-only. API-key default documented at 120 requests/minute; actual account entitlement unverified.
- [OAuth](https://cal.com/docs/api-reference/v2/oauth): scoped access is documented; webhook read/write permissions are distinct. Scope/account/organization mapping, refresh/revoke behavior and Twenty Connection support must be accepted for the concrete flow. No OAuth client created.
- [Get bookings](https://cal.com/docs/api-reference/v2/bookings/get-all-bookings): currently requires 2026-05-01, cursor/nextCursor/hasMore, and supports updated-time filters. Pipedream's 2026-02-25 differs; this proves version drift to review, not an observed failure of its pinned API.
- [Webhook authenticity](https://cal.com/help/webhooks): HMAC-SHA256 over payload and X-Cal-Signature-256. Require raw-body verification, tenant-bound subscription, duplicate/replay handling and reconciliation. Delivery retry guarantees and deletion/tombstone completeness were not established.
- Credential custody: NOT PASSED. Future secrets must remain in accepted Twenty Connections; Nango/Pipedream hosted custody is not inferred. Native user/App/Workspace denial and revocation tests are missing.
- Security/permission: NOT PASSED. Inspect signed receiver, minimum scope, cancellation/reschedule identity, timestamps and personal-data retention before any implementation dispatch.
- License gate: MIT source candidate identified; dependencies and intended reuse still need bounded review. Pipedream/Nango are not approved source drops.
- Blocker owners: demand and installation gap → native repo head/product owner; custody and permission proof → native repo head; any cross-system authority decision → mhoo architecture head; deployment → infrastructure only if later authorized.

### Next pass and validation

Do not repeat unchanged Cal.com research hourly. Reopen only for accepted demand, new source/API/license evidence or a concrete gate answer. First decision is whether booking lifecycle evidence adds enough beyond a booking link and existing Twenty calendar sync. No issue should be created from this hypothesis.

Documentation checks: git diff --check and staged diff review; primary URLs/source claims reviewed. No test tooling exists in this repository, and no runtime tests were invented. Research PR: none. This pass is local documentation, not merged/default-branch capability. Shared Linear publication is a research record only.

Repo-head steering received after this pass: next passes follow the existing Linear priority table (Gmail, Calendar, Clover, selected Drive files, controlled Sheets bridge, Linear, GitHub, conditional Plaid, LINE OA audit, conditional WhatsApp). Reuse completed receipts; at most two per pass. Cal.com is retained history, not promoted above that worklist.
