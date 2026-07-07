# Generator Candidate Register

Use this register before turning repeated service shape into generated output.

Purpose: prevent generator enthusiasm from outrunning governance. A generator should encode decisions the team already understands. It should not become a machine for manufacturing uncertainty faster.

Do not include real repository paths, template paths, service names, schemas, business field names, internal CLI names, commit hashes, issue links, vendors, or production examples in public copies.

---

## Candidate summary

| Field | Value |
|---|---|
| Candidate ID | `GCR-000` |
| Generator candidate name |  |
| Candidate type | File copier / service skeleton / package generator / contract generator / schema-driven generator / semantic generator / other |
| Supported service archetype | Domain capability / platform capability / read-model edge / integration worker / internal tooling / template-generated service / other |
| Status | Idea / prototype / pilot / supported / deprecated / rejected / revisit |
| Review owner |  |
| Proposed generator owner |  |

## Why generate?

Describe the repeated problem the generator would remove.

> 

Check all that apply.

- [ ] Service startup cost repeats
- [ ] Template copying causes drift
- [ ] Baseline wiring is stable
- [ ] Generated output can be tested
- [ ] The same module/package shape repeats
- [ ] Contract or schema structure is stable enough
- [ ] Manual setup creates runtime or integration risk
- [ ] Other: 

## Preconditions

Do not proceed unless most of these are true.

| Question | Answer |
|---|---|
| Has the shape repeated across real services or modules? | Yes / no / partial |
| Is the generated portion mostly execution mechanics or stable structure? | Yes / no / mixed |
| Is product meaning kept handwritten/domain-owned? | Yes / no / unclear |
| Can generated output be tested? | Yes / no |
| Is there an owner for generator and templates? | Yes / no |
| Is there a regeneration or update policy? | Yes / no / not needed |
| Are extension points defined? | Yes / no |
| Is there an escape hatch for justified local variation? | Yes / no |
| Is adoption evidence available? | Prototype / pilot / production use / none |

A generator before repetition is speculation. A generator after repeated service shape can become codified learning.

## Input model

What does the generator read?

- [ ] Simple prompt / answers
- [ ] Service type declaration
- [ ] Configuration file
- [ ] Contract description
- [ ] Schema or model definition
- [ ] Entity metadata
- [ ] Package/module manifest
- [ ] Existing template baseline
- [ ] Other: 

Input versioning rule:

> 

Input validation rule:

> 

## Generation boundary

### Can generate safely

| Output area | Generate once / regenerate / never | Notes |
|---|---|---|
| Service skeleton |  |  |
| Package/module structure |  |  |
| Transport wiring |  |  |
| Configuration loading |  |  |
| Health/readiness |  |  |
| Observability baseline |  |  |
| DTOs/contracts |  |  |
| Persistence mapping |  |  |
| Tests / smoke checks |  |  |
| Documentation stub |  |  |

### Must remain handwritten or owned elsewhere

| Area | Owner | Reason |
|---|---|---|
| Business logic | Domain/product team | Product meaning belongs outside the generator. |
| Domain invariants | Domain/product team | Invariants need explicit ownership and review. |
| Authorization decisions | Security/domain owner | Rules may be product-specific and high-risk. |
| Workflow meaning | Domain/product team | Runtime mechanics may be shared; meaning should not vanish into generated glue. |
| Provider/customer-specific policy | Product/domain owner | Do not platformize customer-specific semantics. |

## Regeneration policy

Choose one.

- [ ] Generate once; generated files become product-owned
- [ ] Regenerate safely; generated regions are protected
- [ ] Regenerate only during scaffold creation
- [ ] Regenerate contracts only
- [ ] Regenerate tests/docs only
- [ ] No regeneration until policy exists

Policy note:

> 

## Generated-output validation

| Check | Exists? | Owner |
|---|---|---|
| Unit tests for generator | Yes / no |  |
| Snapshot or golden-output tests | Yes / no |  |
| Generated service smoke test | Yes / no |  |
| Lint/static checks | Yes / no |  |
| Contract compatibility check | Yes / no / not applicable |  |
| Post-generation checklist | Yes / no |  |
| Manual review gate | Yes / no |  |

## Adoption and support

| Field | Value |
|---|---|
| Intended consumers | Generalized service archetypes only |
| Adoption path |  |
| Support owner |  |
| Compatibility expectation |  |
| Exception path |  |
| Deprecation path |  |
| Documentation/example status | None / draft / usable / supported |

## Decision

Choose one.

- [ ] Do not generate yet
- [ ] Keep as experiment
- [ ] Build scaffold generator
- [ ] Add to skeleton/template process
- [ ] Generate narrow package/module only
- [ ] Pilot with one service archetype
- [ ] Promote to supported generator
- [ ] Retire generator candidate

Decision statement:

> 

## No-go signals

Do not promote this generator when:

- [ ] it is based on one implementation only;
- [ ] it hides product meaning inside generated files;
- [ ] generated output cannot be tested;
- [ ] teams edit generated files with no policy;
- [ ] service archetypes need different baselines;
- [ ] no team owns generator compatibility;
- [ ] the generator exists mainly because generation feels modern;
- [ ] adoption requires a guided tour every time.

## Review history

| Date / review marker | Decision | Reason | Owner | Next trigger |
|---|---|---|---|---|
|  |  |  |  |  |

## Reminder

A generator before governance is a copy-paste machine with better manners.

