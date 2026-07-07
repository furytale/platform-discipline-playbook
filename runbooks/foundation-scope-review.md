# Foundation Scope Review Runbook

## Purpose

Decide whether a capability should enter or expand the execution-core Foundation. The Foundation needs a boundary, not a mood.

## Trigger

Run this when:

- a new Foundation primitive is proposed;
- repeated execution concern appears;
- product teams ask Foundation to absorb product semantics;
- drift suggests missing Foundation support.

## Inputs

- Proposed capability.
- Execution core scope map.
- Foundation capability register.
- Evidence of repetition, generalized.
- Support and ownership expectations.

## Participants

| Role | Responsibility |
|---|---|
| Architect / technical lead | checks boundary and decision quality |
| Owner | accepts future cost |
| Consumer representative | validates adoption and usability |
| Delivery lead | confirms capacity and delivery impact |

## Procedure

### 1. Define the proposed capability

Write one plain sentence: `The proposed Foundation capability is X, and it exists to solve Y execution problem.` If product-specific language is required, stop and reclassify.

### 2. Classify the concern

Choose: execution mechanic, product semantic, integration edge, operational concern, metadata edge, local product convenience, or unknown.

### 3. Check repetition and stability

Ask whether this repeats across real services/archetypes, whether divergence is risky, and whether the repeated part is stable enough to test.

### 4. Check governance readiness

Confirm owner, canonical path, support boundary, compatibility rule, conformance check, exception path, and deprecation path.

### 5. Decide

Add to Foundation scope, keep local, document pattern, keep as shared helper/library, create bounded metadata edge, defer, or reject as product semantics.

## Outputs

- Scope decision.
- Capability register update.
- Owner/support boundary.
- Conformance check.
- Exception path.

## Completion criteria

- Capability is classified.
- Platform-owned and product-owned parts are separated.
- Owner is named.
- Canonical path exists or capability is rejected.
- Templates are updated.

## No-go signals

- Capability is product meaning.
- No owner/support model exists.
- No conformance signal exists.
- Adoption support is needed but unfunded.

## Public-safe reminder

Keep entries generalized and synthetic. Do not record real service names, repo paths, commits, schemas, queue/event/table names, screenshots, logs, vendors, exact timelines, payment/security/compliance details, or identifiable client/project facts.

## Related files

- [`../templates/execution-core-scope-map.md`](../templates/execution-core-scope-map.md)
- [`../templates/foundation-capability-register.md`](../templates/foundation-capability-register.md)
