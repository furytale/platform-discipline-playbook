# Metadata Edge Review Runbook

## Purpose

Decide whether configurable behavior belongs at a bounded semantic edge, remains typed/domain-owned, should be split, or should be deferred.

## Trigger

Run this when:

- a feature asks for configurable fields, mappings, transforms, value sets, or activation;
- teams propose pushing product behavior into configuration;
- a metadata/rules layer starts controlling runtime behavior.

## Inputs

- Requested variability.
- Typed execution boundary.
- Product/domain owner.
- Validation, activation, rollback, and versioning expectations.

## Participants

| Role | Responsibility |
|---|---|
| Architect / technical lead | checks boundary and decision quality |
| Owner | accepts future cost |
| Consumer representative | validates adoption and usability |
| Delivery lead | confirms capacity and delivery impact |

## Procedure

### 1. Define requested variability

Write what varies and across which generalized contexts. If variability cannot be named, do not turn it into metadata.

### 2. Separate semantics from execution

Identify what is product meaning, what is execution mechanics, and which typed guarantees must remain untouched.

### 3. Identify bounded semantic edge

Name the edge: mapping, transform, validation profile, activation lifecycle, or another generalized edge.

### 4. Check governance

Confirm owner, validation, activation, rollback, versioning, observability, compatibility, tests, and exception path.

### 5. Decide

Typed-only, bounded metadata edge, typed core + metadata edge, defer, or reject as unowned runtime configuration.

## Outputs

- Metadata edge decision.
- Boundary split.
- Owner.
- Activation/versioning/rollback rules.
- Conformance check.

## Completion criteria

- Variability is named.
- Typed core responsibilities are protected.
- Metadata owner is named.
- Validation/activation/rollback exist.

## No-go signals

- Metadata controls core invariants without strong governance.
- Authorization/transaction/workflow/idempotency guarantees weaken.
- No owner exists.

## Public-safe reminder

Keep entries generalized and synthetic. Do not record real service names, repo paths, commits, schemas, queue/event/table names, screenshots, logs, vendors, exact timelines, payment/security/compliance details, or identifiable client/project facts.

## Related files

- [`../templates/metadata-edge-candidate.md`](../templates/metadata-edge-candidate.md)
- [`../diagrams/typed-core-metadata-edges.md`](../diagrams/typed-core-metadata-edges.md)
