# AGENTS.md

## Repository role

`connectors` is the conditional source boundary for provider contracts and
accepted shared or integration-heavy adapters. Under accepted ADR-0008,
App-local provider logic belongs with its Mhoo Twenty App and uses Twenty
Connections by default. The current tree is documentation only; it contains no
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
