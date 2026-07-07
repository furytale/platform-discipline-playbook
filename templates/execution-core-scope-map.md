# Execution Core Scope Map

Use this template to define what an execution-core Foundation owns, does not own, conditionally owns, and explicitly excludes.

All entries should stay public-safe, generalized, and synthetic. Do not include real product, company, service, repository, schema, queue, event, vendor, timeline, incident, or person details.

## Context

- Product/system context, generalized:
- Current uncertainty layer:
- Stable execution concerns:
- Review cadence:
- Owner:

## Foundation owns

| Capability | Why platform-owned | Consumers / archetypes | Mandatory? | Owner | Maturity | Canonical path |
|---|---|---|---|---|---|---|
| Transaction control | | | yes / no / conditional | | experimental / supported / deprecated | |
| Inbox / deduplication | | | yes / no / conditional | | experimental / supported / deprecated | |
| Outbox / durable publication | | | yes / no / conditional | | experimental / supported / deprecated | |
| Workflow runtime | | | yes / no / conditional | | experimental / supported / deprecated | |
| Idempotency | | | yes / no / conditional | | experimental / supported / deprecated | |

## Foundation does not own

| Concern | Owner | Reason it stays product/domain-owned | Review trigger |
|---|---|---|---|
| Product meaning | | | |
| Domain invariants | | | |
| Product-specific workflow meaning | | | |
| Customer-specific policy | | | |

## Conditional / bounded ownership

| Concern | Platform responsibility | Product responsibility | Boundary rule | Exception path |
|---|---|---|---|---|
| Workflow | runtime, retry, resume, observability | workflow meaning, domain state | | |
| Metadata edge | validation/promotion mechanics | semantic meaning and lifecycle | | |

## Governance

- Canonical path:
- Exception path:
- Conformance check:
- Review cadence:
- Support owner:
- Deprecation rule:

## When not to use this template

- The decision is purely local and has no reusable/platform implication.
- The entry would require exposing raw evidence or identifiable client/project details.
- Nobody can own the follow-up.
- The template would create ceremony without changing a decision.

## Related files

- [`../runbooks/foundation-scope-review.md`](../runbooks/foundation-scope-review.md)
