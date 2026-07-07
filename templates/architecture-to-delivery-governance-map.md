# Architecture To Delivery Governance Map

Use this map to convert architecture decisions into delivery controls.

All entries should stay public-safe, generalized, and synthetic. Do not include real product, company, service, repository, schema, queue, event, vendor, timeline, incident, or person details.

## Governance table

| Architecture decision | Delivery control | Review gate | Acceptance criteria | Owner | Exception process |
|---|---|---|---|---|---|
| Use Foundation transaction boundary | checklist / conformance test | before service acceptance | no side effects outside unit of work | | |
| Use outbox for durable publication | PR/release check | before release | no direct publish in transactional path | | |
| Metadata edge only at bounded edge | design review | before activation | typed core remains code-owned | | |

## Exception path

- Who can approve:
- Required justification:
- Expiry / review trigger:
- Where exception is recorded:
- How baseline feedback is handled:

## When not to use this template

- The decision is purely local and has no reusable/platform implication.
- The entry would require exposing raw evidence or identifiable client/project details.
- Nobody can own the follow-up.
- The template would create ceremony without changing a decision.

## Related files

- [`../runbooks/architecture-to-delivery-governance.md`](../runbooks/architecture-to-delivery-governance.md)
