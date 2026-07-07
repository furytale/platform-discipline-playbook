# Platform Ownership Split

Use this template when a reusable asset has both platform-owned and product-owned responsibilities.

All entries should stay public-safe, generalized, and synthetic. Do not include real product, company, service, repository, schema, queue, event, vendor, timeline, incident, or person details.

## Context

- Asset / capability:
- Current classification:
- Platform owner/team:
- Product owner/team:
- Enabling role:
- Review date:

## Responsibility split

| Concern | Platform-owned | Product-owned | Shared with named rule | Notes |
|---|---|---|---|---|
| Baseline code | | | | |
| Product adaptation | | | | |
| Compatibility | | | | |
| Support | | | | |
| Exceptions | | | | |
| Local runtime | | | | |
| Migration | | | | |
| Documentation | | | | |
| Contribution back | | | | |
| Deprecation | | | | |

## Runtime ownership

| Runtime concern | Owner | Evidence / check | Gap |
|---|---|---|---|
| Worker/process execution | | | |
| Scheduling/timers | | | |
| Consumer behavior, generalized | | | |
| Retry/failure recovery | | | |
| Monitoring/alerts | | | |
| Deployment entrypoint | | | |

## Decision

- [ ] Platform-owned through versioned boundary.
- [ ] Product-owned local adaptation.
- [ ] Shared ownership with explicit responsibility rows.
- [ ] Temporary fork with sync-back policy.
- [ ] Product-integrated core with explicit governance.
- [ ] Ownership unclear; block until clarified.

## When not to use this template

- The decision is purely local and has no reusable/platform implication.
- The entry would require exposing raw evidence or identifiable client/project details.
- Nobody can own the follow-up.
- The template would create ceremony without changing a decision.

## Related files

- [`../runbooks/team-topology-review.md`](../runbooks/team-topology-review.md)
