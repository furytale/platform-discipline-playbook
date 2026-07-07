# Platform Drift Review Runbook

## Purpose

Review where services bypass, replace, copy, or reinterpret Foundation rules, then decide whether drift is justified variation or unmanaged erosion.

## Trigger

Run this when:

- services bypass Foundation transaction, inbox, outbox, workflow, or idempotency paths;
- multiple local variants appear;
- canonical path no longer matches delivery reality;
- exception count grows.

## Inputs

- Drift signals.
- Platform drift assessment.
- Foundation scope map.
- Capability register.
- Consumer feedback.

## Participants

| Role | Responsibility |
|---|---|
| Architect / technical lead | checks boundary and decision quality |
| Owner | accepts future cost |
| Consumer representative | validates adoption and usability |
| Delivery lead | confirms capacity and delivery impact |

## Procedure

### 1. List drift signals

Name each signal without blame. `Service archetype uses local transaction wrapper outside canonical path` is better than `team ignored the platform`.

### 2. Classify drift

Choose justified exception, missing Foundation support, unsupported product semantics, unmanaged erosion, obsolete rule, temporary delivery shortcut, or unknown.

### 3. Identify local reason

Ask whether the canonical path was too hard, missing, obsolete, over-owning semantics, or under-supporting a real archetype.

### 4. Decide action

Accept exception with expiry, update Foundation, restore canonical path, create new archetype, document non-scope, schedule migration, or deprecate old behavior.

### 5. Update artifacts

Update drift assessment, capability register, scope map, delivery governance, and monthly signal review item.

## Outputs

- Drift classification.
- Decision and owner.
- Migration or exception action.
- Updated artifacts.

## Completion criteria

- Every drift signal is classified.
- Exceptions have expiry/review trigger.
- Unmanaged erosion has action.
- Baseline feedback is captured.

## No-go signals

- Drift is blamed on people without investigating why.
- Every exception is permanent.
- Product meaning is pulled into platform scope to force consistency.

## Public-safe reminder

Keep entries generalized and synthetic. Do not record real service names, repo paths, commits, schemas, queue/event/table names, screenshots, logs, vendors, exact timelines, payment/security/compliance details, or identifiable client/project facts.

## Related files

- [`../templates/platform-drift-assessment.md`](../templates/platform-drift-assessment.md)
- [`../diagrams/platform-drift-loop.md`](../diagrams/platform-drift-loop.md)
