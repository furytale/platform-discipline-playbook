# Skeleton Readiness Checklist

Use this checklist before creating or expanding a service skeleton, starter template, or generated baseline.

Purpose: decide whether a repeated service baseline is stable enough to encode.

A skeleton should make the boring correct things cheaper. It should not become a prettier copy-paste ritual.

---

## Candidate summary

| Field | Value |
|---|---|
| Candidate ID | `SK-000` |
| Skeleton / template name | Generalized label |
| Target service archetype | Domain capability / platform capability / read-model edge / integration worker / internal tool / other |
| Proposed owner |  |
| Status | Proposed / pilot / supported / deprecated |
| Review owner |  |

## Entry criteria

A concern can enter the skeleton when most of these are true.

| Criterion | Yes / no / partial | Notes |
|---|---|---|
| Appeared in several real services |  |  |
| Needed at service creation time |  |  |
| Divergence is expensive |  |  |
| Default behavior is stable enough |  |  |
| Belongs mostly to execution mechanics |  |  |
| Generated/template output can be tested |  |  |
| Service teams can understand what to change |  |  |
| Template has an owner |  |  |
| Update path is defined |  |  |
| Scope is small enough to maintain |  |  |

## Proposed baseline

Check what belongs in this skeleton.

- [ ] Health endpoint
- [ ] Readiness endpoint
- [ ] Metrics baseline
- [ ] Tracing initialization
- [ ] Configuration loading
- [ ] Configuration validation
- [ ] Logging setup
- [ ] Transport wiring
- [ ] Local infrastructure setup
- [ ] Package/module conventions
- [ ] Minimal test structure
- [ ] Example endpoint or handler
- [ ] Message envelope setup
- [ ] Transaction/use-case baseline
- [ ] Idempotency baseline
- [ ] API documentation setup
- [ ] Post-generation checklist
- [ ] Other: 

## Explicit exclusions

A skeleton should be honest about what it does not own.

Do not include:

- [ ] business logic;
- [ ] domain invariants;
- [ ] customer-specific policy;
- [ ] product workflow meaning;
- [ ] unproven abstractions;
- [ ] optional dependencies that most services do not need;
- [ ] future-looking modules with no owner;
- [ ] anything that cannot be tested or explained.

Additional exclusions:

> 

## Service archetype fit

| Archetype | Supported? | Notes |
|---|---|---|
| Domain capability | Yes / no / partial |  |
| Platform capability | Yes / no / partial |  |
| Read-model edge | Yes / no / partial |  |
| Integration worker | Yes / no / partial |  |
| Internal tooling | Yes / no / partial |  |

## Output and update policy

| Question | Answer |
|---|---|
| Is the output generated once or updated over time? | Generate once / updateable / mixed |
| Which files may teams edit? |  |
| Which files should remain aligned with baseline? |  |
| How are skeleton updates delivered? |  |
| How are generated/template outputs tested? |  |
| What happens when a service deviates? |  |
| Who approves baseline changes? |  |

## Readiness score

| Area | Score 0-2 | Notes |
|---|---:|---|
| Repetition evidence |  |  |
| Stability |  |  |
| Divergence cost |  |  |
| Testability |  |  |
| Ownership |  |  |
| Update path |  |  |
| Adoption clarity |  |  |
| Scope discipline |  |  |

Suggested interpretation:

- `0-6`: not ready; keep as documented pattern or reference example.
- `7-11`: candidate; pilot with one service archetype.
- `12-16`: ready for supported skeleton baseline if ownership and tests exist.

## Decision

Choose one.

- [ ] Not ready; keep local or documented
- [ ] Create reference example
- [ ] Create checklist only
- [ ] Pilot skeleton/template
- [ ] Promote to supported skeleton/template
- [ ] Explore generator support through [`generator-candidate-register.md`](generator-candidate-register.md)
- [ ] Deprecate old skeleton/template

Decision statement:

> 

## Post-generation checklist

Every generated or templated service should confirm:

- [ ] owner assigned;
- [ ] service archetype selected;
- [ ] generated defaults reviewed;
- [ ] local changes recorded;
- [ ] mandatory runtime checks pass;
- [ ] observability baseline present;
- [ ] security/auth assumptions reviewed;
- [ ] exception/deviation entries created for deviations in [`exception-deviation-log.md`](exception-deviation-log.md);
- [ ] upgrade/update path understood.

## Reminder

A skeleton is not exciting architecture. That is the point. It makes the boring correct things cheaper than the creative wrong things.
