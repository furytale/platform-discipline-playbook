# Repeated Service-Shape Ledger

Use this ledger to record repeated service concerns before they become five local implementations with five defenders.

Purpose: make repetition visible, classify it, and decide the smallest useful next move.

Do not include real service names in public copies. Use generic service archetypes such as domain capability, platform capability, read-model edge, integration worker, internal tooling, or template-generated service.

---

## Ledger entries

| ID | Repeated concern | Appeared in archetypes | Occurrence bucket | Divergence risk | Execution mechanics or product meaning? | Current shape | Recommended next move | Owner | Revisit trigger |
|---|---|---|---|---|---|---|---|---|---|
| RSL-000 |  |  | One / two / several / many | Low / medium / high | Execution / product / mixed | Local / documented / helper / shared lib / skeleton / generator / imported | Keep local / document / helper / shared library / skeleton / generator / governance rule / revisit |  |  |

## Entry detail

### Ledger ID

`RSL-000`

### Concern

Name the concern generically.

Examples:

- configuration loading;
- logging setup;
- request tracing;
- error mapping;
- token verification;
- validation flow;
- repository facade;
- transaction helper;
- health/readiness endpoint;
- metrics setup;
- API documentation setup;
- message envelope;
- idempotency handling;
- service startup structure.

### Where it appeared

Use archetypes, not real service names.

| Service archetype | How the concern appeared | Notes |
|---|---|---|
| Domain capability |  |  |
| Platform capability |  |  |
| Read-model edge |  |  |
| Integration worker |  |  |
| Internal tooling |  |  |

### Similarity assessment

| Question | Answer |
|---|---|
| Are implementations solving the same problem? | Yes / no / partly |
| Are differences intentional? | Yes / no / unknown |
| Is divergence already expensive? | Yes / no / not yet |
| Is the concern stable enough to standardize? | Yes / no / partial |
| Does it belong mostly to execution mechanics? | Yes / no / mixed |
| Would a shared solution make the next service cheaper or safer? | Yes / no / unknown |

### Candidate move

Choose the smallest useful move.

- [ ] Keep local
- [ ] Document as named pattern
- [ ] Create reference example
- [ ] Extract shared helper
- [ ] Promote to shared library candidate
- [ ] Add to skeleton/template candidate list
- [ ] Explore generator support through [`generator-candidate-register.md`](generator-candidate-register.md)
- [ ] Add to [`platform-candidate-backlog.md`](platform-candidate-backlog.md)
- [ ] Add governance rule
- [ ] Create exception/deviation entry in [`exception-deviation-log.md`](exception-deviation-log.md)
- [ ] Revisit later

Decision note:

> 

### Ownership and support

| Field | Value |
|---|---|
| Proposed owner |  |
| Source of truth if extracted |  |
| Expected consumers | Generalized list |
| Support expectation | None / informal / named owner / supported asset |
| Compatibility expectation | None / best effort / explicit policy |
| Upgrade path needed? | Yes / no / later |

### No-go signals

Do not promote this concern yet if:

- [ ] it is based on one implementation only;
- [ ] the concern is mostly product meaning;
- [ ] the owner is unclear;
- [ ] service archetypes need different behavior;
- [ ] the shared abstraction would be larger than the problem;
- [ ] the team cannot support upgrades;
- [ ] the repeated pattern is actually a smell to remove.

## Monthly review summary

Use this section during the monthly signal review.

| Review item | Notes |
|---|---|
| New repeated concerns added |  |
| Concerns promoted |  |
| Concerns demoted or removed |  |
| Divergence risk increased |  |
| Baseline needs update |  |
| Exceptions need review |  |
| Owner needed |  |
| Candidate ready for runbook |  |

## Reminder

Repetition did not become platform evidence until the team had somewhere to record it.
