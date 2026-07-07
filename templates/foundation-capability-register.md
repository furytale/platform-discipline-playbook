# Foundation Capability Register

Use this register to inventory Foundation primitives and their maturity, adoption, exceptions, and drift signals.

All entries should stay public-safe, generalized, and synthetic. Do not include real product, company, service, repository, schema, queue, event, vendor, timeline, incident, or person details.

## Capability table

| Capability | Type | Owner | Maturity | Canonical usage | Consumers | Required tests | Exceptions | Drift signals |
|---|---|---|---|---|---|---|---|---|
| | transaction / inbox / outbox / workflow / idempotency / eventing / observability | | experimental / supported / deprecated | | | | | |

## Capability detail

- Capability:
- Owner:
- Source of truth:
- Canonical path:
- Supported consumers:
- Not supported:
- Compatibility policy:
- Support boundary:
- Deprecation rule:

## Maturity labels

| Label | Meaning |
|---|---|
| Experimental | usable only with review; no broad compatibility promise |
| Supported | canonical path, support, and conformance are defined |
| Deprecated | migration path exists; new adoption should stop |

## When not to use this template

- The decision is purely local and has no reusable/platform implication.
- The entry would require exposing raw evidence or identifiable client/project details.
- Nobody can own the follow-up.
- The template would create ceremony without changing a decision.

## Related files

- [`execution-core-scope-map.md`](execution-core-scope-map.md)
- [`../runbooks/foundation-scope-review.md`](../runbooks/foundation-scope-review.md)
