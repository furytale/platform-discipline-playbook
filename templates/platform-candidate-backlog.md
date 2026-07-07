# Platform Candidate Backlog

Use this backlog to separate **possible platform material** from **actual platform assets**.

Purpose: keep ambition visible without pretending every candidate is already governed. A platform backlog should include things the team is not ready to platformize yet. That is how ambition learns manners.

Do not include real service names, repository names, client names, schemas, queue names, field names, internal links, timelines, vendors, or raw evidence in public copies. Use generic service archetypes and synthetic labels.

---

## Backlog summary

| Field | Value |
|---|---|
| Review period |  |
| Review owner |  |
| Platform owner, if any |  |
| Related signal review |  |
| Public-safe status | Internal / sanitized / public-safe |

## Candidate index

| Candidate ID | Candidate | Candidate type | Signal source | Current state | Evidence strength | Governance readiness | Decision | Owner | Next review trigger |
|---|---|---|---|---|---|---|---|---|---|
| PCB-000 |  | Pattern / helper / shared library / skeleton / generator / import / governance rule / platform service / other | Service review / repeated-shape ledger / exception/deviation log / import ADR / support request / consumer feedback | Local / documented / experimental / supported / deprecated / unknown | Weak / medium / strong | Low / medium / high | Keep local / document / promote / shrink / retire / revisit |  |  |

## Candidate detail

### Candidate ID

`PCB-000`

### Candidate name

Use a generalized name.

Examples:

- request tracing baseline;
- health/readiness default;
- message envelope convention;
- idempotency helper;
- service startup skeleton;
- generator input model;
- import ownership rule;
- compatibility review gate.

### Candidate type

Choose one primary type.

- [ ] Local pattern
- [ ] Documented pattern
- [ ] Shared helper
- [ ] Shared library candidate
- [ ] Skeleton/template candidate
- [ ] Generator candidate
- [ ] Platform import / local adaptation
- [ ] Governance rule
- [ ] Platform service
- [ ] Other: 

## Signal source

Where did this candidate come from?

- [ ] Service candidate review
- [ ] Repeated service-shape ledger
- [ ] Shared library extraction review
- [ ] Skeleton readiness review
- [ ] Generator candidate review
- [ ] Platform import review
- [ ] Exception/deviation log
- [ ] Monthly platform signal review
- [ ] Consumer feedback or support request
- [ ] Other: 

Signal note:

> 

## Evidence check

| Question | Answer |
|---|---|
| Has this appeared in more than one real service or product area? | Yes / no / partial |
| Is the repeated concern mostly execution mechanics? | Yes / no / mixed |
| Is the concern stable enough to standardize? | Yes / no / partial |
| Is divergence already costly? | Low / medium / high |
| Would a shared move make the next service cheaper or safer? | Yes / no / unknown |
| Is a reference implementation or example available? | Yes / no / not needed |
| Is this based on evidence rather than hope? | Yes / no / unclear |

Evidence summary:

> 

## Governance readiness

| Area | Current answer |
|---|---|
| Owner named | Yes / no |
| Source of truth known | Yes / no / not applicable yet |
| Versioning model known | Yes / no / not applicable yet |
| Compatibility expectation known | Yes / no |
| Adoption path known | Yes / no |
| Support path known | Yes / no |
| Exception path known | Yes / no |
| Deprecation or retirement path known | Yes / no |
| Team model known | Yes / no |

No owner, no promotion.

## Current move

Choose the smallest useful move.

- [ ] Keep local
- [ ] Name and document the pattern
- [ ] Create reference example
- [ ] Extract shared helper
- [ ] Prepare shared library register entry
- [ ] Prepare skeleton readiness checklist
- [ ] Prepare generator candidate register entry
- [ ] Prepare platform import ADR
- [ ] Add governance rule
- [ ] Approve time-boxed exception
- [ ] Retire or remove
- [ ] Revisit later

Decision statement:

> 

## What must not happen yet

Use this section to keep the candidate honest.

- [ ] Do not call this a platform asset yet
- [ ] Do not make adoption mandatory yet
- [ ] Do not extract code yet
- [ ] Do not generate from this yet
- [ ] Do not publish as a supported baseline yet
- [ ] Do not move product meaning into the platform
- [ ] Other: 

Reason:

> 

## Promotion criteria

This candidate may move toward platform asset status when:

- [ ] repeated use is visible;
- [ ] divergence cost is real;
- [ ] scope and non-scope are clear;
- [ ] product meaning remains domain-owned;
- [ ] owner is named;
- [ ] adoption path exists;
- [ ] compatibility policy exists;
- [ ] support and exception paths exist;
- [ ] consumers can use it without a guided tour;
- [ ] the next service becomes cheaper or safer.

## Review history

| Date / review marker | Decision | Reason | Owner | Next trigger |
|---|---|---|---|---|
|  |  |  |  |  |

## Reminder

A candidate is not a platform asset. It is a signal with a parking space.

Platform work gets expensive when teams skip the boring middle: evidence, owner, adoption path, compatibility, exceptions, and support.

