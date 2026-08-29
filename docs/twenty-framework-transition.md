# Accepted Twenty-framework connector boundary

- Status: `ACCEPTED ARCHITECTURE`; no connector implementation
- Current implementation: documentation only
- Governing decision: [Mhoo ADR-0008](https://github.com/mhoo-os/mhoo/blob/0e94e6b00a3033215e4df3ab197e5559652c2436/ADR/0008-twenty-framework-platform.md)
- Provider access and credentials: not configured or authorized

This note records the accepted connector boundary now that Mhoo uses Twenty as
its sole application and data framework. It does not select Nango, create a
provider integration, move a credential, or authorize an external effect.

## Accepted default

For a provider used by one Mhoo Twenty App:

1. use a Twenty Connection Provider for OAuth client registration, encrypted
   token storage, refresh, revoke, visibility, and connection lifecycle;
2. keep provider-specific translation and deterministic domain rules in the
   owning App;
3. persist normalized Mhoo records through Twenty objects and relations while
   retaining provider identifiers, revisions, timestamps, and provenance; and
4. run bounded pull, push, webhook, or delta work through the App's functions,
   jobs, events, and checkpoint state when those primitives meet the actual
   provider contract.

This path removes the proposed generic connector-service box. It does not make
Twenty authoritative for provider facts: the external provider remains the
source of truth, and the App records a traceable observation or projection.

## When this repository may still own source

A provider seam may remain here only after a concrete requirement proves that
an App-local integration is insufficient. Examples include a genuinely shared
adapter used by several Apps or a selected Nango runtime whose sync, webhook,
checkpoint, retry, provider-execution, or rate-limit mechanics materially
reduce Mhoo-owned infrastructure.

That selection requires all of the following:

- an accepted cross-system owner and interface;
- an exact provider contract and failure model;
- a credential-custody decision;
- a Workspace and record-correlation design that never treats a caller-supplied
  Workspace, tenant, or provider connection ID as authority;
- idempotency, replay, checkpoint, rate-limit, and dead-letter behavior; and
- repository-owned tests plus an Infrastructure-owned deployment and recovery
  plan.

If those conditions are absent, the target disposition for a generic connector
runtime is `REMOVE`, not `BUILD`.

## Credential and authority invariants

- One provider grant has exactly one credential and refresh owner. Twenty and
  Nango must never refresh or revoke the same grant.
- User-visible credentials belong to the user flow; shared background work
  needs an explicitly Workspace-scoped grant. A connection identifier is only
  a locator.
- Secrets, access tokens, refresh tokens, authorization headers, raw webhook
  bodies, and customer records do not enter Git, logs, examples, or receipts.
- Provider writes, OAuth registration, real webhooks, and credential changes
  require explicit authorization and provider-specific proof.
- Codex, agents, and models reason over authorized tools; a connector does not
  become an identity, domain, or reasoning authority.

## Implementation effect

This document describes a selection boundary, not an implemented runtime. A
concrete provider still needs its own
source, tests, permissions, operational plan, and approval before any external
effect occurs.
