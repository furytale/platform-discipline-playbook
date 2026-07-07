# Platform Drift Assessment

Use this template when services bypass, replace, copy, or reinterpret Foundation behavior.

All entries should stay public-safe, generalized, and synthetic. Do not include real product, company, service, repository, schema, queue, event, vendor, timeline, incident, or person details.

## Drift signal

- [ ] Direct persistence usage bypasses canonical transaction path.
- [ ] Direct event publication bypasses durable publication path.
- [ ] Local retry/deduplication replaces inbox/idempotency rule.
- [ ] Local workflow execution bypasses supported runtime.
- [ ] Platform logic is copied locally.
- [ ] Unsupported metadata/configuration path appears.

## Assessment

| Service archetype | Drift type | Local reason | Risk | Justified? | Required action | Owner | Review trigger |
|---|---|---|---|---|---|---|---|
| | justified exception / missing support / unmanaged erosion / obsolete rule | | low / medium / high | yes / no / unclear | | | |

## Decision

- [ ] Accept as exception.
- [ ] Update Foundation.
- [ ] Restore canonical path.
- [ ] Create new supported archetype.
- [ ] Document non-scope.
- [ ] Schedule migration.

Decision summary:

>

## When not to use this template

- The decision is purely local and has no reusable/platform implication.
- The entry would require exposing raw evidence or identifiable client/project details.
- Nobody can own the follow-up.
- The template would create ceremony without changing a decision.

## Related files

- [`../runbooks/platform-drift-review.md`](../runbooks/platform-drift-review.md)
