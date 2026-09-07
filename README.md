<!-- mhoo-os-context:start -->
### Mhoo OS Connectors: Mhoo OS context

This repository is the conditional source boundary for provider contracts and accepted shared or integration-heavy adapters.

- **Owns:** provider contracts and semantics; accepted shared provider adapters; an earned Nango-backed integration seam when a concrete requirement justifies it.
- **Does not own:** simple App-local OAuth or a generic connector service; provider facts; Twenty Workspace authority; deployment or cutover authority.
- **Architecture authority:** [accepted Mhoo OS blueprint](https://github.com/mhoo-os/mhoo/blob/92e43a7b9a59570c76729fb5f8850c66bda6ef78/docs/architecture/SYSTEM_BLUEPRINT.md) and [ADR-0008](https://github.com/mhoo-os/mhoo/blob/92e43a7b9a59570c76729fb5f8850c66bda6ef78/ADR/0008-twenty-framework-platform.md).
- **Current implementation evidence:** [repository-owned source and records](https://github.com/mhoo-os/connectors/tree/main).
- **Deployment and production evidence:** owned separately by [Mhoo OS Infrastructure](https://github.com/mhoo-os/infrastructure/tree/main/docs); source, CI, publication, and rehearsal are not deployment or cutover proof.
- **Upstream context:** Mhoo-native conditional boundary; current source is documentation only and App-local integrations belong with their Mhoo App by default.
- **Contributors:** start with the [repository instructions](https://github.com/mhoo-os/connectors/blob/main/AGENTS.md). Generated context is governed by [README governance](https://github.com/mhoo-os/mhoo/blob/main/docs/architecture/README_GOVERNANCE.md).
<!-- mhoo-os-context:end -->

# Mhoo OS Connectors

[![Status: Documentation only](https://img.shields.io/badge/status-documentation_only-2563eb)](https://github.com/mhoo-os/connectors)

This repository is the conditional source boundary for provider contracts and
accepted shared or integration-heavy adapters. App-local provider logic lives
with its Mhoo Twenty App and uses Twenty Connection Providers by default.

The current `main` tree contains documentation and boundary definitions only;
it does not prove a connector runtime, provider call, credential, or production
integration. External providers remain authoritative for provider facts. A
connector preserves provenance and provider semantics without becoming Twenty,
Workspace, domain, or reasoning authority.

## Accepted Twenty-framework boundary

[Mhoo ADR-0008](https://github.com/mhoo-os/mhoo/blob/0e94e6b00a3033215e4df3ab197e5559652c2436/ADR/0008-twenty-framework-platform.md)
selects Twenty Connection Providers for simple App-local OAuth and keeps
provider-specific translation in the owning Mhoo App. This repository does not
become a generic connector service or credential vault; it remains available
only for an accepted shared provider seam or an earned Nango-backed integration
runtime.

The architecture is accepted, but no provider implementation, runtime,
credential, or external call exists. See the
[transition note](docs/twenty-framework-transition.md) for the selection tests
and credential-custody rules.

## Working here

Start with [AGENTS.md](AGENTS.md): reuse the current issue, PR, and run-ledger
receipts before checks, verify the exact source, and obtain a scoped repo-head
handoff. This documentation-only tree has no build or test commands; documentation
validation is `git diff --check` plus source and link review.

[Accepted ADR-0012](https://github.com/mhoo-os/mhoo/blob/abdc2be8a2adb6d979905db8bcf6a3ae6c41225c/ADR/0012-cloudflare-connector-runtime-ownership.md)
places the Cloudflare operations control plane in
`mhoo-os/infrastructure/cloudflare/connector-runtime/`. Shared provider semantics
may belong here only after an accepted selection. Native Clover App work remains
in `mhoo-twenty-next`; the folders below do not establish runtime ownership.

## Directories

- `clover/` — Clover integration requirements and boundaries.
- `nango/` — historical Nango design context; not a selected implementation.
- `docs/` — shared connector documentation.
