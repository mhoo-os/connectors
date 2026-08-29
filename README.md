<!-- mhoo-os-context:start -->
### Mhoo OS Connectors: Mhoo OS context

This repository is the provider-integration boundary for authorization flows, APIs, webhooks, cursors, retries, identifiers, and provider semantics.

- **Owns:** provider authorization flows; provider APIs and webhooks; cursors, retries, identifiers, and provider semantics; versioned Core ingress translation.
- **Does not own:** provider facts; Core durable state; human identity or Workspaces; deployment authority.
- **Architecture authority:** [accepted Mhoo OS blueprint](https://github.com/mhoo-os/mhoo/blob/1374bbbe2a059320c29c8268ff971efbd9dfa256/docs/architecture/SYSTEM_BLUEPRINT.md) and [ADR-0006](https://github.com/mhoo-os/mhoo/blob/1374bbbe2a059320c29c8268ff971efbd9dfa256/ADR/0006-mhoo-os-system-architecture-blueprint.md).
- **Current implementation evidence:** [repository-owned source and records](https://github.com/mhoo-os/connectors/tree/main).
- **Deployment and production evidence:** owned separately by [Mhoo OS Infrastructure](https://github.com/mhoo-os/infrastructure/tree/main/docs); source, CI, publication, and rehearsal are not deployment or cutover proof.
- **Upstream context:** Mhoo-native boundary repository; not an upstream product fork.
- **Contributors:** start with the [repository instructions](https://github.com/mhoo-os/connectors/blob/main/AGENTS.md). Generated context is governed by [README governance](https://github.com/mhoo-os/mhoo/blob/main/docs/architecture/README_GOVERNANCE.md).
<!-- mhoo-os-context:end -->

# Mhoo OS Connectors

[![Status: Documentation only](https://img.shields.io/badge/status-documentation_only-2563eb)](https://github.com/mhoo-os/connectors)

This repository owns the Mhoo OS provider-integration boundary: provider
authorization flows, APIs, webhooks, cursors, retries, provider identifiers,
provider semantics, and translation into versioned Core ingress contracts.

The current `main` tree contains documentation and boundary definitions only;
it does not prove a connector runtime, provider call, credential, or production
integration. External providers remain authoritative for provider facts. A
connector preserves provenance and provider semantics without becoming Core or
Twenty authority.

## Directories

- `clover/` — Clover integration requirements and boundaries.
- `nango/` — Nango abstraction and connector architecture.
- `docs/` — shared connector documentation.
