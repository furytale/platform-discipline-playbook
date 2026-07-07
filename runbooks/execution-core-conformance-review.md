# Execution Core Conformance Review Runbook

## Purpose

Check whether a service or service archetype follows the Foundation canonical path for execution mechanics. Conformance is how the team knows whether the shared execution model still exists.

## Trigger

Run this when:

- a new service is created;
- a service adopts Foundation capability;
- a service changes transaction, messaging, workflow, or idempotency behavior;
- drift review finds local variants.

## Inputs

- Service/archetype, generalized.
- Foundation scope map.
- Capability register.
- Exceptions/deviations.
- Delivery governance map.

## Participants

| Role | Responsibility |
|---|---|
| Architect / technical lead | checks boundary and decision quality |
| Owner | accepts future cost |
| Consumer representative | validates adoption and usability |
| Delivery lead | confirms capacity and delivery impact |

## Procedure

### 1. Select review target

Name the generalized service archetype and relevant Foundation capabilities.

### 2. Check transaction boundaries

Record whether the service uses canonical transaction control or an approved exception.

### 3. Check durable publication and inbound handling

Check outbox/durable publication, inbox/deduplication, retry, and idempotency.

### 4. Check workflow runtime

Check retry, resume, timer, failure recovery, and runtime ownership.

### 5. Check application/infrastructure boundary

Look for infrastructure leakage or local convenience that creates global inconsistency.

### 6. Record result

Conforming, conforming with exception, drift/action required, unsupported archetype, or blocked.

## Outputs

- Conformance status.
- Exception updates.
- Drift assessment if needed.
- Action items.

## Completion criteria

- Core checks are recorded.
- Exceptions have owner and expiry.
- Drift has action.
- Unsupported archetypes route to scope review.

## No-go signals

- Runtime ownership is unclear.
- Direct side effects bypass required durable path.
- Product semantics moved into Foundation code to pass review.

## Public-safe reminder

Keep entries generalized and synthetic. Do not record real service names, repo paths, commits, schemas, queue/event/table names, screenshots, logs, vendors, exact timelines, payment/security/compliance details, or identifiable client/project facts.

## Related files

- [`foundation-scope-review.md`](foundation-scope-review.md)
- [`platform-drift-review.md`](platform-drift-review.md)
