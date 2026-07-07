# Metadata Edge Candidate

Use this template when configurable behavior appears and the team must decide whether it belongs at a bounded semantic edge or should remain typed/domain-owned.

All entries should stay public-safe, generalized, and synthetic. Do not include real product, company, service, repository, schema, queue, event, vendor, timeline, incident, or person details.

## Candidate

- Requested variability:
- Consumers:
- Source/system boundary, generalized:
- Product/domain owner:
- Lifecycle:
- Current implementation:

## Candidate test

| Question | Answer | Notes |
|---|---|---|
| Is variability real and repeated? | yes / no / unclear | |
| Is meaning stable enough to name? | yes / no / unclear | |
| Can validation be explicit? | yes / no / unclear | |
| Can activation/promotion be governed? | yes / no / unclear | |
| Can rollback be handled? | yes / no / unclear | |
| Is ownership named? | yes / no / unclear | |
| Does this protect typed execution guarantees? | yes / no / unclear | |

## Decision

- [ ] Keep typed.
- [ ] Introduce bounded metadata edge.
- [ ] Defer.
- [ ] Split into typed core + metadata edge.
- [ ] Reject as product semantics pretending to be platform flexibility.

## Governance

- Owner:
- Validation rule:
- Versioning:
- Activation rule:
- Rollback rule:
- Exception path:
- Conformance check:

## When not to use this template

- The decision is purely local and has no reusable/platform implication.
- The entry would require exposing raw evidence or identifiable client/project details.
- Nobody can own the follow-up.
- The template would create ceremony without changing a decision.

## Related files

- [`../runbooks/metadata-edge-review.md`](../runbooks/metadata-edge-review.md)
