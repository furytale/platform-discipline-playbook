# Shared Library Register

Use this template when shared code is already reused or is being proposed for extraction.

Purpose: prevent shared code from becoming an unofficial platform with no constitution.

Do not use real repository names, package names, file paths, service names, or internal links in public copies. Replace them with generalized labels.

---

## Library summary

| Field | Value |
|---|---|
| Library / module ID | `SL-000` |
| Generalized name |  |
| Concern type | Configuration / logging / tracing / error mapping / validation / transaction / messaging / service structure / other |
| Current status | Proposed / experimental / supported / deprecated / retired |
| Owner |  |
| Source of truth | Generalized location or internal reference placeholder |
| Known consumers | Generalized service archetypes only |
| Review owner |  |

## Why this should be shared

| Question | Answer |
|---|---|
| Which repeated concern does it solve? |  |
| How many implementations already exist? | One / two / several / many |
| What divergence risk does it reduce? |  |
| Is the concern mostly execution mechanics? | Yes / no / mixed |
| What should stay local? |  |
| What should not be included? |  |

## Scope

### This library owns

- 

### This library does not own

- 

### Supported service archetypes

- [ ] Domain capability
- [ ] Platform capability
- [ ] Read-model edge
- [ ] Integration worker
- [ ] Internal tooling
- [ ] Template/generated service
- [ ] Other: 

## Versioning and compatibility

| Field | Value |
|---|---|
| Versioning model | Local copy / versioned package / vendored snapshot / workspace package / not yet solved |
| Breaking-change policy |  |
| Compatibility guarantee | None / best effort / explicit / strict |
| Supported versions |  |
| Migration window |  |
| Upgrade owner | Platform owner / consuming team / shared responsibility / not defined |
| Compatibility tests |  |

## Adoption

| Field | Value |
|---|---|
| Adoption path |  |
| Minimal example exists? | Yes / no |
| Setup documentation exists? | Yes / no |
| First consumer support needed? | Yes / no |
| Review required before adoption? | Yes / no |
| Exception path defined? | Yes / no |

## Support

| Field | Value |
|---|---|
| Support owner |  |
| Support channel / mechanism | Generalized description |
| Defect handling |  |
| Feature request handling |  |
| Escalation path |  |
| Expected response model | Best effort / scheduled review / explicit internal SLA |

## Consumer inventory

Use generalized labels in public copies.

| Consumer archetype | Adoption status | Version / snapshot | Notes |
|---|---|---|---|
|  | Proposed / using / upgrading / deprecated |  |  |

## Dead-weight and drift check

| Question | Answer |
|---|---|
| Are modules copied but unused? | Yes / no / unknown |
| Are consumers patching locally? | Yes / no / unknown |
| Are consumers using different versions? | Yes / no / unknown |
| Is there a canonical source of truth? | Yes / no |
| Are future-looking helpers present but unsupported? | Yes / no |
| Is this library acting like a platform asset already? | Yes / no / partly |

## Decision

Choose one.

- [ ] Keep local
- [ ] Extract shared helper only
- [ ] Create experimental shared library
- [ ] Promote to supported shared asset
- [ ] Promote to governed platform asset after governance gate
- [ ] Split into smaller assets
- [ ] Deprecate
- [ ] Retire

Decision statement:

> 

## Governance requirements before platform promotion

- [ ] Owner named
- [ ] Source of truth defined
- [ ] Versioning rule defined
- [ ] Compatibility policy defined
- [ ] Support model defined
- [ ] Adoption path documented
- [ ] Exception process defined
- [ ] Consumer inventory exists
- [ ] Deprecation path defined
- [ ] Monthly review entry added

## Reminder

The first shared library is useful because the pain is real. It becomes dangerous when nobody knows which copy is canon.
