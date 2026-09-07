## 2026-09-07T14:19Z — pass 003 — selected Drive evidence and Sheets import

**Drive 6/10 HOLD; Sheets 6/10 HOLD. Two new candidate/job assessments.** No implementation recommendation; native/installed capability and custody gates remain unknown.

### Reuse and ownership

Read the shared research ledger before this pass; preserve all prior priorities, installed Linear/WhatsApp correction and extension assessment authority. Reused [MHO-266](https://linear.app/mhoo/issue/MHO-266/standalone-clover-app-multi-merchant-records-historical-import-and) current issue receipt (updated 13:37Z): existing Clover worker 01a073d5-22c3-7123-89ad-ebf486cdc93a, native head 01a07aa7-944a-70c3-bf77-d51b9fc766f2, PR32 source 2c35f6b1d1091cd593bc292134c7360c681df11b. Issue reports model/connection tests, and explicitly says sync metadata is not enabled sync. Prior synthetic renderer receipts remain separate from installed permission proof. No Clover rescore, provider research, tests or new dispatch; MHO-265 custody and existing historical-reach owners retained. Existing Clover source ledger: docs/provenance/clover-payment-persistence-source-proof.md in its owning repo.

Voice's dated September 7 installed list remains attributed, not independently refreshed. Current local native repo HEAD is 5f6cdd318b6a0d5db85b1a12f54e2aaffb65b035; filename search under twenty-apps returned no Drive/Sheets-named files. This narrow negative search does NOT establish absence of native/import/file capabilities. Connected Codex Google Drive tooling is not proof of native Workspace custody or durable ingestion. No new-build recommendation until native head supplies current feature/connection evidence.

### Scores and concrete jobs

| Candidate | User outcome and observed gap | Utility | Native gap | Licensed maintained reuse | API/auth/sync | Simplicity | Total |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Drive selected-file evidence | User selects an evidence file and can trace the imported evidence back to file identity and observed version; permission loss does not leave silently accessible stale content. Owner-prioritized job, but native attachment/link/import shortfall unproved. | 2 | 1 | 1 | 1 | 1 | **6/10 HOLD** |
| Sheets bounded import | User selects one spreadsheet and explicit range, previews typed rows, imports once with provenance and duplicate protection. Existing Finance UI stays independent; no outbound export or two-way sync proposed. Actual gap versus existing import tools unknown. | 2 | 1 | 1 | 1 | 1 | **6/10 HOLD** |

Gap=1 is provisional potential, not demonstrated missing feature. Reuse=1 because official samples exist with exact Apache-2.0 license but are quickstarts, not qualified native adapters. Reliability=1 because provider mechanisms exist while MHOO reconciliation, permissions and concurrent-edit behavior are unproved. Both job classes remain “capability coverage unknown,” not classified as defects or setup failures.

### Official sources and useful findings (checked 2026-09-07)

- Discovery only: [Zapier Drive](https://zapier.com/apps/google-drive/integrations), [Zapier Sheets](https://zapier.com/apps/google-sheets/integrations). Directory availability is not demand, license or operating proof.
- [Drive scopes](https://developers.google.com/workspace/drive/api/guides/api-specific-auth): drive.file is per-file and non-sensitive, supported with Picker; it permits modification as well as access. It is NOT a read-only token. Broad drive.readonly/metadata.readonly are restricted scopes; choosing read-only broadly is not automatically least privilege. Future selection must pair native operation allowlists with accepted credential custody; actual consent/app verification remains unproved.
- [Sheets scopes](https://developers.google.com/workspace/sheets/api/scopes): scopes apply at spreadsheet-file level, not individual tabs/ranges. drive.file can authorize selected files but includes writes; spreadsheets.readonly reads all spreadsheets accessible through that scope. A range picker is an application constraint, not an OAuth boundary. Protected ranges restrict edits, not reading.
- [Sheets values.get](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets.values/get): explicit range and render options matter; formatted values are default, and date rendering is ignored when formatted values are selected. A future import needs declared formula/value, date/timezone, numeric and blank-cell semantics and source spreadsheet/sheet/range identity. Row number alone is not a durable business key.
- [Drive changes](https://developers.google.com/workspace/drive/api/guides/manage-changes): change tokens/pages provide a reconciliation primitive. Future design must distinguish removal/access loss, file revision/modified time and fetched content; no claim of complete immutable document versioning from a current file link. Cursor commit/replay and retention rules not validated here.
- [Sheets limits/pricing](https://developers.google.com/workspace/sheets/api/limits): standard usage documented at no additional cost, with over-quota charging planned later in 2026. Do not promise perpetual free operation or assume an account's billing state. [Drive limits](https://developers.google.com/workspace/drive/api/guides/limits) also needs workload/account-specific quota review; no service purchased or quota requested.

### Exact reusable source

Official [googleworkspace/node-samples](https://github.com/googleworkspace/node-samples/tree/dc39b4f4dca7af02bbec94c10a125ff643cc1820) snapshot dc39b4f4dca7af02bbec94c10a125ff643cc1820 inspected via public GitHub:
[LICENSE](https://github.com/googleworkspace/node-samples/blob/dc39b4f4dca7af02bbec94c10a125ff643cc1820/LICENSE) Apache License 2.0;
[Drive quickstart](https://github.com/googleworkspace/node-samples/blob/dc39b4f4dca7af02bbec94c10a125ff643cc1820/drive/quickstart/index.js) uses drive.metadata.readonly and local credentials.json;
[Sheets quickstart](https://github.com/googleworkspace/node-samples/blob/dc39b4f4dca7af02bbec94c10a125ff643cc1820/sheets/quickstart/index.js) uses spreadsheets.readonly and local credentials.json.
These are provider call examples, not acceptable copied auth/custody defaults for MHOO. No sample copied/executed; dependency and recent per-file maintenance review remains incomplete. Prior Pipedream/Activepieces/Nango license observations retained without rechecking unchanged snapshots; none selected over native/official primitives.

### Gates and next owner/action

Security/license/custody gates are NOT collectively passed: an exact sample license is known, but intended reuse/dependencies, native file selection, token custody, per-user/App/Workspace denial and permission-loss retention remain unknown. Unknown current native inventory independently forces HOLD. Prefer existing links/import/file primitives if they complete the job; a new shared connector or credential authority is not earned.

Primary issue: none for Drive/Sheets; existing MHO-266 reused only as Clover handoff. Proposed implementation repository, if a gap earns work: owning App in mhoo-twenty-next; receiving native head 01a07aa7-944a-70c3-bf77-d51b9fc766f2, no assigned worker/accepted new scope. Product/native head owns exact sample-free user journey and inventory evidence; native head owns custody/permission decisions; mhoo owns any cross-system ADR; infrastructure owns future operations only after authorization.

Research owner/head: 01a07aa6-6d60-71f0-92e8-87c7c1561d5c. Base a2b9806008093b5799a67498a868719a1cc84c63, branch codex/integration-research-ledger initially clean. Authoritative AGENTS read at d60f3dcd3e72a741bc65ac340d1734aa6680b7d9, unchanged; origin/main freshly verified at d60f3dc, prior retained worktrees preserved. Existing run ledger /Users/mhoooo/Documents/Codex/2026-09-06/mhoo-coordinator/checkpoint.json; canonical research document 70320781-1678-4a87-a4ed-b5569fefb3e1.

Authorized next step: preserve findings and hand off planning gaps. Revisit these two jobs only on changed evidence. Next scheduled priority: existing Linear app job assessment and GitHub evidence reuse. No provider files/data read, implementation, install, grant, export, sends, fees, deployment, new issue/worker or schedule changes. Local documentation only, unpublished/no PR; diff check and link/source review required, no runtime checks invented.
