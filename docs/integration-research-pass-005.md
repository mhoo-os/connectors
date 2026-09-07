## 2026-09-07T16:20Z — pass 005 — Plaid current-window ingestion

**Plaid 5/10 HOLD. One candidate assessed; LINE OA remains next scheduled candidate.** Existing [MHO-127](https://linear.app/mhoo/issue/MHO-127) is the demand and acceptance owner; no duplicate issue or worker.

Reused issue provenance: supplied files are owner-attested exports through ChatGPT Finance using Plaid, not proof of an MHOO production connection. Original CSV evidence and reconciliation limitations stay in the existing source inventory; this pass did not open transaction files, repeat counts or infer six-year coverage. MHO-127's surface/cursor/custody decision and MHO-183/227/228 dependencies remain unresolved here, not newly dispatched.

| Criterion | Score | Reason |
| --- | --- | --- |
| Workflow usefulness | 2 | Existing Finance demand for recent bank/card records reconciled against first-party statements. |
| Missing native capability | 1 | Durable native ingestion has not been accepted; current installed/native inventory insufficient to prove absence. |
| Maintained licensed reuse | 1 | Official MIT SDK available, but not a qualified native synchronization adapter. |
| API/auth/sync reliability | 1 | Documented change/cursor protocol; account eligibility, native custody and overlap proof missing. |
| Operating simplicity | 0 | Production access, cost, account consent, reconciliation and durable recovery are material work. |
| **Total** | **5/10** | **HOLD: security/permission/custody gates unknown; no implementation recommendation.** |

Expected job: authorized recent bank/card changes arrive once with account/source identity and corrections, while coverage remains explicitly unreconciled until statement overlap passes. Gap class: unaccepted integration surface/authority, not a demonstrated bug. Proposed next action is an existing-owner decision on exact surface and custody after reusing acceptance receipts; no live Link, account creation or synchronization authorized.

### Primary evidence checked 2026-09-07

[Transactions API](https://plaid.com/docs/api/products/transactions/) confirms up to 24 months, not six years. Two useful planning details: history request length must be set before Transactions initialization; changing account filtering creates a distinct cursor stream. On pagination mutation, restart the complete update loop from its initial cursor, not only the failed page. These constraints belong in a future bounded proof plan; do not remove/recreate an Item to change history under this research authority.

[Sync migration guide](https://plaid.com/docs/transactions/sync-migration/) provides existing-integration migration context. [Items API](https://plaid.com/docs/api/items/) is the supported reference used after the attempted /docs/api/tokens/ URL failed retrieval. No token/account endpoint called. Actual consent, revoke/reconnect, institution support and webhook authenticity implementation remain unproved.

[Pricing](https://plaid.com/pricing/) documents multiple billing models and product access, but no MHOO-specific Transactions rate or approved budget was established. A consumer-facing “free” statement or test allowance is not production entitlement. No purchase, sales outreach, account access or paid refresh requested.

Official source discovery follows [Plaid libraries](https://plaid.com/docs/api/libraries/): [plaid-node snapshot](https://github.com/plaid/plaid-node/tree/0b0f2efaf7ce49bc00e1f4f9b1985cd87d916034), observed commit date 2026-09-01; [exact MIT license](https://github.com/plaid/plaid-node/blob/0b0f2efaf7ce49bc00e1f4f9b1985cd87d916034/LICENSE). README identifies the official generated Node client and API version 2020-09-14. This is an SDK contract, not evidence that MHOO uses that revision or that dependencies, tenancy, retries or runtime acceptance pass. No SDK copied, installed or executed. Prior alternative-runtime license research not repeated; no Nango/runtime selection.

### Custody and limits

Primary issue MHO-127; implementation repository/worker **not accepted for this surface**. Default proposal remains owning native App in mhoo-twenty-next under existing head01a07aa7-944a-70c3-bf77-d51b9fc766f2, with Twenty retaining identity/Connections/permissions. Finance consumes authorized records, not a new parallel credential vault. Native head/issue owner must resolve exact token, cursor and webhook ownership; client authority/retention and statement overlap remain with existing issue dependencies. No new assignment inferred.

Research custody: Connectors head01a07aa6-6d60-71f0-92e8-87c7c1561d5c. Base98ca0435329a4ce1f5b0a28a3460066d9ac2b2d5; initially clean local research branch, instructions retained from d60f3dcd3e72a741bc65ac340d1734aa6680b7d9 / AGENTS.md. Prior origin/main/worktree receipts reused; no upstream implementation or ownership change proposed. Existing operational checkpoint /Users/mhoooo/Documents/Codex/2026-09-06/mhoo-coordinator/checkpoint.json and shared research document70320781-1678-4a87-a4ed-b5569fefb3e1 remain authoritative coordination pointers.

No provider data calls, live files, credentials, implementation, deployment, installs, new issues/workers, schedule changes or Dark Factory revival. Local unpublished documentation/no PR. Next: retain findings; do not repeat Plaid without changed evidence. Next scheduled pass assesses LINE OA using prior work before new research.
