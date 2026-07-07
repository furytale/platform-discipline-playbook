# Exception / Deviation Log

Use this log to make deviations visible, time-bounded, and useful.

Purpose: turn exceptions into feedback, not hidden drift. Some deviations are justified local choices. Some show the baseline is wrong. Some are just drift wearing a deadline costume.

Do not include real service names, repository names, people names, issue links, incident details, schemas, queue names, exact dates, vendors, or production/security/compliance details in public copies.

---

## Log summary

| Field | Value |
|---|---|
| Review period |  |
| Review owner |  |
| Baseline or asset reviewed | Generalized name |
| Related runbook | Monthly platform signal review / repeated pattern review / platform import review / other |
| Public-safe status | Internal / sanitized / public-safe |

## Deviation index

| Deviation ID | Area | Archetype | Baseline deviated from | Reason category | Risk | Status | Owner | Expiry / revisit trigger |
|---|---|---|---|---|---|---|---|---|
| EXC-000 |  | Domain capability / platform capability / read-model edge / integration worker / internal tooling / template-generated service / other |  | Justified local choice / missing baseline support / delivery pressure / obsolete rule / experiment / drift / other | Low / medium / high | Proposed / approved / rejected / expired / closed / baseline update needed |  |  |

## Deviation detail

### Deviation ID

`EXC-000`

### What deviated?

Describe the difference generically.

> 

### Baseline or rule affected

| Field | Value |
|---|---|
| Baseline / asset / pattern |  |
| Expected behavior |  |
| Actual behavior |  |
| Related service archetype |  |
| Related candidate or asset ID |  |

## Reason classification

Check all that apply.

- [ ] Justified local choice
- [ ] Product/domain semantics require variation
- [ ] Baseline does not support this archetype
- [ ] Baseline is obsolete
- [ ] Delivery pressure created a temporary workaround
- [ ] Platform asset is too hard to adopt
- [ ] Compatibility gap
- [ ] Support gap
- [ ] Experiment with explicit learning goal
- [ ] Unmanaged drift
- [ ] Unknown

Reason statement:

> 

## Risk assessment

| Question | Answer |
|---|---|
| Does this create runtime risk? | Low / medium / high / unknown |
| Does this create compatibility risk? | Low / medium / high / unknown |
| Does this create security/compliance risk? | Low / medium / high / unknown |
| Does this create support or ownership confusion? | Low / medium / high / unknown |
| Does this make future migration harder? | Low / medium / high / unknown |
| Does this reveal that the baseline may be wrong? | Yes / no / maybe |

Risk note:

> 

Do not publish sensitive details. If security, payment, compliance, legal, or production exposure exists, keep the public copy abstract.

## Decision

Choose one.

- [ ] Approve as local variation
- [ ] Approve as time-boxed exception
- [ ] Reject and align to baseline
- [ ] Update baseline
- [ ] Create new service archetype rule
- [ ] Create platform candidate backlog item
- [ ] Create shared library / skeleton / generator review item
- [ ] Convert into platform import ADR
- [ ] Revisit later

Decision statement:

> 

## Ownership and expiry

| Field | Value |
|---|---|
| Deviation owner |  |
| Baseline owner |  |
| Approver role |  |
| Expiry / revisit trigger |  |
| Cleanup owner |  |
| Follow-up artifact |  |

## Follow-up actions

| Action | Owner | Trigger / target |
|---|---|---|
|  |  |  |

## Monthly review section

| Review question | Notes |
|---|---|
| Which deviations expired? |  |
| Which deviations were justified? |  |
| Which deviations reveal a wrong baseline? |  |
| Which deviations should become platform backlog items? |  |
| Which deviations are unmanaged drift? |  |
| Which deviations need public-risk review before being referenced externally? |  |

## Closure

| Field | Value |
|---|---|
| Closure status | Closed / superseded / still active / baseline updated / retired |
| Closure note |  |
| Evidence retained internally? | Yes / no / not needed |
| Public-safe summary needed? | Yes / no |

## Reminder

Exceptions are not moral failures. They are architecture signals with a deadline.

The dangerous exception is the one nobody records.

