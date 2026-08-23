# AGENTS.md

## Repository role

`connectors` defines and will implement Mhoo provider adapters. The current
tree is documentation and boundary definition; it does not contain a production
connector runtime, stored provider credentials, or configured provider calls.

## Sources of truth

- Current Git state establishes the present implementation boundary. Do not
  describe planned Clover or Nango work as an existing runtime capability.
- The committed Clover and Nango boundary documents provide design context;
  cross-repository authority is governed by accepted ADRs in `../mhoo/ADR/`.
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

- Build one bounded provider capability at a time. Add source-level validation
  with the implementation; do not invent runtime rules or commands before code
  exists.
- Keep credential lifecycle, tenancy, retries, idempotency, and failure
  semantics explicit rather than hiding them behind a generic abstraction.
- A new connector must not introduce an identity system, Core data-plane
  authority, Twenty Workspace authority, or deployment/cutover authority.

## Architecture changes

- An authority, credential-custody, tenancy, or cross-repository data-flow
  change requires a reviewed decision in `../mhoo/ADR/` before implementation.
  Deploy and production operations belong to `../infrastructure`.
