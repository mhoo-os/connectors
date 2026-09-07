## 2026-09-08 05:27 Bangkok — pass 011 — selected RSS/Atom monitoring

**RSS/Atom monitoring 6/10 HOLD. One candidate.**
Potential job: show new items from owner-selected public industry/news feeds with original links and source timestamps. Exact feeds, user workflow and current native gap remain unconfirmed.

Scores utility1, native gap1, maintained licensed reuse1, API/auth/sync1, simplicity2: **6/10**. Simplicity assumes explicitly public feeds without credentials. Security, feed-content rights and ownership gates remain UNKNOWN; no implementation recommendation.

### Primary-source findings

[RSS 2.0 specification](https://www.rssboard.org/rss-specification) makes item guid and pubDate optional; guid is publisher-defined. Descriptions may contain HTML; ttl and skip hints guide polling. A future adapter must preserve original identity and timestamps and document fallback deduplication when guid is absent. A missing item in a rolling feed must not automatically mean deletion; completeness and retention need feed-specific evidence.

[Atom RFC 4287 section 4.2.6](https://www.rfc-editor.org/rfc/rfc4287) defines permanent entry/feed identifiers retained across revisions and compared case-sensitively without dereferencing. Do not normalize Atom identifiers as ordinary destination URLs. Preserve source identity separately from the clickable article URL.

Public GitHub metadata identified [rbren/rss-parser](https://github.com/rbren/rss-parser/tree/394178530e87fa010efc6e8d5dd4e801715c5e63), latest observed commit394178530e87fa010efc6e8d5dd4e801715c5e63 dated2026-08-25. Its pinned [LICENSE](https://github.com/rbren/rss-parser/blob/394178530e87fa010efc6e8d5dd4e801715c5e63/LICENSE) is MIT. This is a parsing-library lead, not an accepted connector or security/dependency audit. Library licensing does not establish rights to republish any selected feed content. [Zapier RSS directory](https://zapier.com/apps/rss/integrations) was discovery context only; no account or installed capability verified.

Future acceptance questions: approved feed URLs and content use; redirect/private-network restrictions; XML parsing and HTML display safety; response-size/time bounds; polling and duplicate policy. These are unimplemented proof requirements, not verified protections. Private/token-bearing feeds require a separate Connections custody decision.

### Owner, evidence and authorized next step

Primary issue none; retained implementation worker none; implementation-owning repo and accepting head unassigned. App-local mhoo-twenty-next is the default if demand earns work, with native head01a07aa7-944a-70c3-bf77-d51b9fc766f2 accepting scope first. Research coordinator01a07aa6-6d60-71f0-92e8-87c7c1561d5c retains the missing feed/job/owner decision. Dated installed inventory reused only as attributed context; current RSS overlap unknown. An existing feed reader/source links might already meet the need. Twenty retains identity/Connections/permissions.

Base057575519b342b52ee0043dddf24c994c6515f48, initially clean branch. AGENTS authority d60f3dcd3e72a741bc65ac340d1734aa6680b7d9 and desk/checkpoint reading path retained from earlier passes: /Users/mhoooo/Documents/Codex/MHOO-DESK-SETUP.md and /Users/mhoooo/Documents/Codex/2026-09-06/mhoo-coordinator/checkpoint.json. Shared Linear ledger read before append; prior remote/worktree receipts reused. Local unpublished documentation, no PR. No live feed/account calls, credentials, installs, implementation, provider writes, purchases, new issues/workers or schedule changes. Next authorized action: publish this research receipt to the existing shared ledger/head; next scheduled topic YouTube/TikTok. Reopen RSS only on changed evidence.
