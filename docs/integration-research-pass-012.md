## 2026-09-08 06:26 Bangkok — pass 012 — owned video performance

**YouTube analytics 5/10 HOLD; TikTok authorized video monitoring 4/10 HOLD.** Two candidates. Expected job: an owned-channel operator sees dated video performance and original source links to decide future content. Exact account, metric and business decision remain unconfirmed. Public discovery, owner analytics, publishing and media generation are separate jobs.

| Candidate | Utility | Native gap | Maintained licensed reuse | API/auth/sync | Simplicity | Total |
| --- | --- | --- | --- | --- | --- | --- |
| YouTube | 1 | 1 | 1 | 1 | 1 | 5/10 |
| TikTok | 1 | 1 | 0 | 1 | 1 | 4/10 |

Both lack current authorized native/installed capability mapping and accepted security/credential custody; HOLD regardless of score. No observed failing journey establishes a defect or missing feature.

### YouTube

[Reports query](https://developers.google.com/youtube/analytics/reference/reports/query) binds channel reports to the authenticated user's channel. Its current top notice requires youtube.readonly, while its scope table and old examples list yt-analytics.readonly. Treat this mismatch as unresolved minimum-grant evidence, not permission to request broader scopes. Monetary reporting is separately scoped; content-owner reports have partner eligibility. Responses may stop before requested endDate when metrics are not all available, omit rows entirely, and lag recent days. Future UI must distinguish incomplete/unavailable data from zero.

[Data API quota calculator](https://developers.google.com/youtube/v3/determine_quota_cost) currently describes separate daily buckets of 100 calls each for search.list and videos.insert, plus 10,000 units for other endpoints; the page summary still contains older point figures. Use actual project quota and selected endpoint evidence before estimating capacity; these Data API figures do not establish Analytics API quota or dollar cost. No paid tier or free operating-cost claim verified.

Official GitHub [google-api-nodejs-client](https://github.com/googleapis/google-api-nodejs-client/tree/41a90ebe003d13f23f98074c6daecf1587075d55), latest observed commit41a90ebe003d13f23f98074c6daecf1587075d55 dated2026-09-04, has [Apache2.0 LICENSE](https://github.com/googleapis/google-api-nodejs-client/blob/41a90ebe003d13f23f98074c6daecf1587075d55/LICENSE). Source lead only: exact adapter and dependencies not audited. Do not copy stale authorization examples as custody design.

### TikTok

Official [Display getting started](https://developers.tiktok.com/doc/display-api-get-started/) requires Login Kit/API product approval and user.info.basic/video.list grants. [List Videos](https://developers.tiktok.com/docs/en/tiktok-api-v2-video-list) requires the user's authorization, returns their public videos newest first, maximum20/page, and cursor/has_more pagination. This is not proof of arbitrary-account search or private owner analytics. A creation-time cursor alone does not establish detection of older metric changes or removed videos.

[Research and Insights catalog](https://developers.tiktok.com/docs/en/research-insights-landing) advertises distinct research/commercial routes; neither that catalog nor Display access proves entitlement for this business job. Exact deeper analytics route, approval/access tier, metric history, costs and retention remain unknown. No suitably licensed maintained server adapter established this pass. No scraper substituted. Existing TikTok analytics UI may already satisfy demand.

### Custody and next step

Primary issue none. Implementation-owning repo/head and retained worker unassigned. App-local mhoo-twenty-next is the default proposal only after native head01a07aa7-944a-70c3-bf77-d51b9fc766f2 accepts the concrete job; no shared seam earned. Connectors head01a07aa6-6d60-71f0-92e8-87c7c1561d5c retains research and missing account/metric/owner decisions. Dated voice inventory reused as attributed history, not current connection proof. Twenty owns identity/Connections/permissions; Clover unchanged.

Base134434e97f6d33fe57418aaf93ec3810665039c9 initially clean. Shared ledger read before work; earlier remote/worktree receipts retained. AGENTS authority d60f3dcd3e72a741bc65ac340d1734aa6680b7d9 and reading paths /Users/mhoooo/Documents/Codex/MHOO-DESK-SETUP.md and /Users/mhoooo/Documents/Codex/2026-09-06/mhoo-coordinator/checkpoint.json retained. Local unpublished documentation/no PR. No live provider/account data, grants, installs, implementation, posts, charges, issues/workers or automation changes. Authorized next action: append findings and send meaningful documentation mismatches to research head. Next scheduled candidates Higgsfield and X, with generation/publishing separate and unauthorized.
