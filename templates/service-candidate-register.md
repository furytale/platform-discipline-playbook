# Service Candidate Register

Use this template before creating a new service or extracting a major capability.

Purpose: make service extraction a decision, not a repository event.

All entries should use generalized names when shared publicly. Do not include real service names, repository names, paths, domains, schemas, queue names, or internal issue links.

---

## Candidate summary

| Field | Value |
|---|---|
| Candidate ID | `SC-000` |
| Proposed capability |  |
| Proposed service archetype | Domain capability / platform capability / read-model edge / integration worker / internal tool / other |
| Current location | Central backend / existing service / local module / external boundary / unknown |
| Requested by | Role/team, not person name |
| Review owner |  |
| Status | Proposed / reviewing / accepted / rejected / revisit |

## Why separate?

Check all that apply.

- [ ] Different lifecycle
- [ ] Different ownership
- [ ] Different runtime profile
- [ ] Different scaling profile
- [ ] Integration boundary
- [ ] Security or isolation boundary
- [ ] Read/query model pressure
- [ ] Operational responsibility
- [ ] Repeated capability across product areas
- [ ] Other: 

One-sentence reason for separation:

> 

## Boundary test

| Question | Answer |
|---|---|
| Is the boundary clearer than the coordination cost? | Yes / no / not yet |
| What does this candidate own? |  |
| What does it explicitly not own? |  |
| Which product/domain team owns the meaning? |  |
| Which team owns runtime operation? |  |
| Which data or state belongs here? |  |
| Which data or state must remain elsewhere? |  |
| Which consumers depend on this boundary? | Generalized list only |
| Which integration contracts are needed? | Generalized list only |

## Service archetype assessment

| Archetype | Fit | Notes |
|---|---:|---|
| Domain capability | Low / medium / high |  |
| Platform capability | Low / medium / high |  |
| Read-model edge | Low / medium / high |  |
| Integration worker | Low / medium / high |  |
| Internal tooling | Low / medium / high |  |
| Template/generated service | Low / medium / high |  |

## Risks if extracted now

- [ ] Boundary still unstable
- [ ] Product meaning unclear
- [ ] Runtime ownership unclear
- [ ] Operational load too high
- [ ] Integration contract not ready
- [ ] Duplicate semantics likely
- [ ] Team cannot support another deployable unit
- [ ] Other: 

Notes:

> 

## Risks if kept central/local

- [ ] Coupling increases
- [ ] Ownership remains implicit
- [ ] Integration logic stays hidden
- [ ] Runtime behavior diverges
- [ ] Repeated pattern remains invisible
- [ ] Central backend becomes bottleneck
- [ ] Other: 

Notes:

> 

## Repeated concerns observed

Use this section to feed the repeated service-shape ledger.

| Concern | Already seen elsewhere? | Execution mechanics or product meaning? | Next move |
|---|---|---|---|
| Configuration | Yes / no / unknown | Execution / product / mixed | Keep local / document / shared helper / shared library / skeleton |
| Logging | Yes / no / unknown | Execution / product / mixed |  |
| Tracing | Yes / no / unknown | Execution / product / mixed |  |
| Error mapping | Yes / no / unknown | Execution / product / mixed |  |
| Authentication integration | Yes / no / unknown | Execution / product / mixed |  |
| Validation | Yes / no / unknown | Execution / product / mixed |  |
| Transaction boundary | Yes / no / unknown | Execution / product / mixed |  |
| Messaging / event envelope | Yes / no / unknown | Execution / product / mixed |  |
| Idempotency | Yes / no / unknown | Execution / product / mixed |  |
| Health/readiness | Yes / no / unknown | Execution / product / mixed |  |
| Metrics | Yes / no / unknown | Execution / product / mixed |  |
| Service startup structure | Yes / no / unknown | Execution / product / mixed |  |

## Decision

Choose one.

- [ ] Keep central/local
- [ ] Extract service now
- [ ] Extract after boundary clarification
- [ ] Document pattern only
- [ ] Create shared helper/library candidate
- [ ] Create skeleton/template candidate
- [ ] Revisit after more delivery evidence

Decision statement:

> 

## Follow-up actions

| Action | Owner | Target / trigger |
|---|---|---|
| Update repeated service-shape ledger |  |  |
| Add platform candidate backlog item, if needed |  |  |
| Create or update ADR |  |  |
| Define owner and support model |  |  |
| Create exception/deviation entry if deviating from baseline |  |  |
| Revisit boundary |  |  |

## Revisit trigger

Revisit this candidate when:

- [ ] Another service needs the same capability
- [ ] Ownership boundary becomes clearer
- [ ] Runtime profile changes
- [ ] Integration contract stabilizes
- [ ] Product semantics stabilize
- [ ] Local duplication becomes costly
- [ ] Other: 

## Review note

A new service is justified when the boundary is clearer than the coordination cost. If the main reason is “the architecture diagram looks cleaner,” keep the capability local and improve the seams first.
