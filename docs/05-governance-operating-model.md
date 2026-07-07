# Governance Operating Model

## Core idea

Governance is architecture.

Not because every decision needs ceremony. Because reusable code changes the operating model of the team. Once several services depend on the same asset, the hard questions move from “can we reuse this?” to “can we keep this coherent while delivery pressure changes around it?”

A platform asset needs more than code:

- ownership;
- source of truth;
- versioning;
- compatibility policy;
- adoption path;
- support model;
- exception handling;
- conformance checks;
- deprecation policy;
- feedback loop;
- team model.

Without those, shared code can help the first adopters and hurt everyone later.

## Minimum governance boundary

Do not call an asset a platform asset until the team can answer these questions.

| Area | Question |
|---|---|
| Scope | What does this asset own, and what does it explicitly not own? |
| Owner | Which role or team owns changes, support, compatibility, and lifecycle? |
| Source of truth | Where is the canonical version? |
| Versioning | How are changes released, consumed, and retired? |
| Compatibility | What can break, what must not break, and how are breaking changes handled? |
| Adoption | How does a service or team start using it? |
| Support | Where do consumers go when it fails, blocks delivery, or needs clarification? |
| Exceptions | How does a team deviate without hiding drift? |
| Conformance | How do we know consumers still follow the baseline where it matters? |
| Deprecation | How does old platform behavior leave the system? |
| Feedback | How do consumer pain and local deviations change the roadmap? |
| Team topology | Who is the platform owner, who enables adoption, and who consumes it? |

The platform was not the library. It was not the skeleton. It was not the generator. The platform was the agreement around them.

## Governance levels

| Level | Description | Allowed language |
|---|---|---|
| Local pattern | One or two teams use it; reuse is not governed. | “Local pattern” or “candidate.” |
| Documented pattern | The pattern is named and reviewed, but not enforced. | “Recommended pattern.” |
| Shared asset | Code or template is reused; owner and source of truth exist. | “Shared asset.” |
| Supported asset | Compatibility, support, and upgrade path are defined. | “Supported shared asset.” |
| Governed platform asset | Adoption rules, exceptions, conformance, support, versioning, and team model exist. | “Platform asset.” |

Avoid platform inflation. Calling something a platform does not make it governed. It only makes the missing governance harder to ignore.

## Operating model components

### 1. Ownership

Every reusable asset needs an owner. “Everyone uses it” is not ownership. “The architect knows it” is not ownership. “The original team still cares about it” is not ownership.

A useful ownership statement includes:

- owning team or role;
- decision rights;
- support responsibility;
- release responsibility;
- compatibility responsibility;
- deprecation responsibility;
- backup owner or escalation path.

### 2. Source of truth

The team must know which version is canonical.

Possible source-of-truth models:

- versioned package;
- shared repository;
- template repository;
- generator source;
- internal platform service;
- product-owned local adaptation;
- temporary fork with sync-back rules.

If several copies exist and nobody knows which one is canon, the asset is already drifting.

### 3. Versioning and compatibility

A platform asset changes slower than local product code because consumers need trust.

Define:

- supported versions;
- breaking-change rules;
- migration window;
- compatibility tests;
- consumer notification path;
- upgrade ownership;
- rollback expectation.

Compatibility is not politeness. It is the price of reuse.

### 4. Adoption path

Consumers need more than a link.

A credible adoption path includes:

- when to adopt;
- when not to adopt;
- setup instructions;
- minimal example;
- service archetypes supported;
- acceptance criteria;
- common mistakes;
- support channel;
- exception path.

If adoption requires a guided tour from the only person who understands the asset, the platform is not self-service yet.

### 5. Support model

Define support before the first serious consumer depends on the asset.

Support can include:

- office hours;
- issue queue;
- review gate;
- pairing during first adoption;
- documentation ownership;
- incident or defect escalation;
- service-level expectation for internal consumers.

Support does not have to be heavyweight. It does have to exist.

### 6. Exception handling

Exceptions are not moral failures. They are signals.

Some exceptions are justified local choices. Some show the baseline is wrong. Some are drift wearing a deadline costume.

A useful exception record includes:

- what deviated;
- why;
- who approved it;
- expiry or revisit trigger;
- whether the baseline should change;
- whether this is a new archetype.

### 7. Conformance

Conformance does not mean every service looks identical.

It means the mandatory parts stay true:

- runtime baseline;
- security assumptions;
- observability;
- messaging envelope;
- transaction rules;
- service startup conventions;
- upgrade requirements;
- exception records.

Conformance can be checked through review, tests, generator output validation, static checks, template validation, or architecture decision review.

### 8. Deprecation

Reusable assets need a way to die.

Define:

- deprecated modules;
- replacement path;
- migration window;
- consumer inventory;
- removal owner;
- risk if not removed.

Without deprecation, platform assets become a museum. The exhibits are still imported in production.

### 9. Feedback loop

A platform asset should learn from adoption:

- support requests;
- exceptions;
- local forks;
- repeated consumer patches;
- template edits after generation;
- compatibility pain;
- missing examples;
- recurring review comments.

Feedback should change the platform backlog. Otherwise the platform is not an internal product. It is a rulebook with imports.

### 10. Team topology

Platform governance includes team design.

At minimum, decide:

- who owns the platform asset;
- who helps product teams adopt it;
- who consumes it;
- what interaction mode is expected: collaboration, facilitation, or self-service consumption;
- who funds support and evolution.

A platform owned by nobody becomes architect-owned intent. That works until the architect becomes the bottleneck.

## Governance gate

Use this before promoting a shared asset to platform asset.

```text
Asset name:
Asset type: shared library / skeleton / generator / versioned package / imported core / platform service / other

Scope defined?                 yes / no
Explicit non-scope defined?    yes / no
Owner named?                   yes / no
Source of truth defined?       yes / no
Versioning rule defined?       yes / no
Compatibility policy defined?  yes / no
Adoption path documented?      yes / no
Support model documented?      yes / no
Exception process defined?     yes / no
Conformance check exists?      yes / no
Deprecation path exists?       yes / no
Feedback loop exists?          yes / no
Team model defined?            yes / no

Decision:
- not a platform asset yet
- supported shared asset
- governed platform asset
- retire / merge / keep local
```

## When not to govern heavily

Do not build a governance machine around:

- one-off experiments;
- local product semantics;
- short-lived prototypes;
- tooling used by one team with low blast radius;
- repeated concerns that are cheap to diverge;
- assets with no owner;
- assets consumers do not trust or need.

A small asset with clear ownership beats a large platform promise with ceremonial governance and no adoption.

## Failure patterns

### Documentation mistaken for governance

The docs say what should happen. Delivery does something else.

Fix: add review gates, conformance checks, ownership, and exception handling.

### Architect-owned platform

The platform exists because one person remembers the intent and reviews everything.

Fix: assign team ownership and create a team API.

### Compatibility by hope

Consumers update when they can. Breaking changes are discovered late.

Fix: version releases and define migration windows.

### Exceptions disappear

Teams deviate for good reasons and bad reasons, but nobody records the difference.

Fix: create [`exception-deviation-log.md`](../templates/exception-deviation-log.md) entries and review them regularly.

### Platform absorbs product meaning

The platform starts owning domain semantics because it already owns execution mechanics.

Fix: narrow the platform promise. Keep product meaning in domain ownership.

## Related files

- [`../templates/platform-candidate-backlog.md`](../templates/platform-candidate-backlog.md)
- [`../templates/shared-library-register.md`](../templates/shared-library-register.md)
- [`../templates/generator-candidate-register.md`](../templates/generator-candidate-register.md)
- [`../templates/exception-deviation-log.md`](../templates/exception-deviation-log.md)
- [`../templates/platform-import-adr.md`](../templates/platform-import-adr.md)
- [`../runbooks/shared-library-extraction.md`](../runbooks/shared-library-extraction.md)
- [`../runbooks/platform-import-review.md`](../runbooks/platform-import-review.md)
- [`../runbooks/monthly-platform-signal-review.md`](../runbooks/monthly-platform-signal-review.md)
- [`../diagrams/platform-import-ownership.md`](../diagrams/platform-import-ownership.md)
