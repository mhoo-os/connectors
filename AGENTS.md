# AGENTS.md

## Repository role

`connectors` is the conditional source boundary for provider contracts and
accepted shared or integration-heavy adapters. Under accepted ADR-0008,
App-local provider logic belongs with its Mhoo Twenty App and uses Twenty
Connections by default. Accepted [ADR-0012](https://github.com/mhoo-os/mhoo/blob/abdc2be8a2adb6d979905db8bcf6a3ae6c41225c/ADR/0012-cloudflare-connector-runtime-ownership.md)
assigns the Cloudflare operations control plane to
`mhoo-os/infrastructure/cloudflare/connector-runtime/`, not this repository.
The current tree is documentation only; it contains no
runtime, credential, or configured provider call.

## Sources of truth

- Current Git state establishes the present implementation boundary. Do not
  describe planned Clover or Nango work as an existing runtime capability.
- The committed Clover and Nango boundary documents provide historical design
  context; ADR-0008 and the current Mhoo architecture sources govern ownership
  and the Connections-first default.
- Provider API behavior, scopes, receipts, and account state must be verified
  from the provider and implementation evidence when a connector is built.

## Authority and data rules

- External providers remain authoritative for provider facts. A connector may
  preserve, translate, and deliver evidence; it must not silently become the
  business-domain authority.
- Preserve provider-specific identity, revision, timestamp, scope, and error
  semantics through normalization. Evidence must retain enough source identity
  to be traced and replayed safely.
- Keep credentials, refresh tokens, API keys, and raw secrets out of Git, logs,
  fixtures, and receipts. Never import legacy provider credentials implicitly.
- Do not make provider calls, create OAuth clients, or alter provider data
  without explicit authorization and an implementation-specific proof plan.

## Implementation and validation

- Do not manually edit a generated Mhoo context block. Run the central checker
  for context changes; verify current-state prose from this repository's tree.
- Build here only after a concrete requirement earns a shared adapter or
  integration runtime and its cross-system owner is accepted. Add source-level
  validation with the implementation; do not invent runtime rules or commands
  before code exists.
- Keep credential lifecycle, tenancy, retries, idempotency, and failure
  semantics explicit rather than hiding them behind a generic abstraction.
- A new connector must not introduce a generic connector platform, identity
  system, separate data plane, Twenty Workspace authority, or
  deployment/cutover authority.

## Architecture changes

- An authority, credential-custody, tenancy, or cross-repository data-flow
  change requires a reviewed decision in `../mhoo/ADR/` before implementation.
  Deploy and production operations belong to `../infrastructure`.

## Working and handoff rules

- Before probes or checks, read the existing issue, PR receipts, and run ledger.
  For the current desk transition, start with
  `/Users/mhoooo/Documents/Codex/MHOO-DESK-SETUP.md` and
  `/Users/mhoooo/Documents/Codex/2026-09-06/mhoo-coordinator/checkpoint.json`.
  These are local coordination pointers, not portable build dependencies.
- Verify origin, remote default branch, exact source commit, dirty state, and
  worktrees. Reuse matching evidence; rerun only for a changed input, failure,
  or unresolved question. Preserve older local branches and other workers' work.
- The repo head accepts a scoped issue/worker/evidence handoff before dispatch.
  Existing workers stay with their coordinator until explicitly transferred.
  Native Clover App work remains with its existing `mhoo-twenty-next` worker;
  a provider or project name does not assign implementation here.
- Continue safe, reversible work within the accepted scope. Escalate conflicting
  ownership, missing authority, or a material security/cost/reversibility choice
  with the exact missing decision. Request central catalog/generator changes
  from the coordinator; never hand-edit generated context or change an ADR here.
- Finish with the issue or dispatch reference, base/head commits, PR, checks and
  evidence pointers, remaining limits, and next owner/action. Distinguish
  committed, proposed for review, merged, and available on the default branch.
  When the scope is complete, wait for the next handoff rather than invent work.
- For documentation changes, run `git diff --check` and review links, source
  claims, and the diff. This tree has no build, test, coverage, or lint tooling;
  do not invent commands or add placeholder CI. Generated-context changes use
  the central checker documented in Mhoo's README governance.
- Classify stale branches/worktrees for the handoff; do not delete or reset them
  as cleanup. Source work does not authorize merge, deployment, or credentials.
