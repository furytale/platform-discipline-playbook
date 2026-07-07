# Bottom-Up Platform Discipline

## Core idea

A full platform can be too early. Platform discipline usually is not.

This page is for the stage where the product is still learning its own shape, but backend growth is already too expensive to leave informal. The team does not yet need a large Foundation. It does need a way to notice repetition, classify service candidates, track deviations, and prevent shared code from becoming shared drift.

The useful question is not:

> Should we build a platform now?

The better question is:

> How do we keep an early backend from becoming chaotic while a full platform is still too early?

## The discipline layer

Discipline is not a personality trait. It is a tracking loop.

Every new service or major module should answer two questions:

1. Can we ship this capability safely?
2. What did this teach us about the next service?

That second question is where platform signals appear.

A service candidate should leave a decision trace, not only a new repository. A repeated concern should be named before it becomes five slightly different implementations. A shared helper should not become a platform promise until someone owns its versioning, support, and upgrade path.

## Platform signal loop

```text
New service / major module
        |
        v
Service candidate review
        |
        v
What repeated? What changed?
        |
        v
Repeated service-shape ledger
        |
        v
Decision gate
        |
        +-- keep local
        +-- document pattern
        +-- extract shared helper
        +-- promote to shared library candidate
        +-- encode in skeleton/template
        +-- explore generator support
        +-- add governance rule
        +-- revisit later
        |
        v
Adoption / deviation tracking
        |
        v
Baseline update or exception
        |
        +-- back to next service
```

The loop is simple. The hard part is keeping it alive while delivery pressure is loud.

See [`../diagrams/platform-signal-loop.md`](../diagrams/platform-signal-loop.md).

## Minimum viable architecture discipline

You do not need a large architecture board. You need enough routine for architectural memory to live somewhere other than one person's head.

| Routine | Purpose | Typical artifact |
|---|---|---|
| Service creation review | Decide whether the boundary deserves separation. | [`service-candidate-register.md`](../templates/service-candidate-register.md) |
| Post-service review | Record what repeated and what was new. | [`repeated-service-shape-ledger.md`](../templates/repeated-service-shape-ledger.md) |
| Repetition review | Decide the smallest useful move for repeated concerns. | [`repeated-pattern-review.md`](../runbooks/repeated-pattern-review.md) |
| Platform candidate review | Keep candidates visible without calling them assets too early. | [`platform-candidate-backlog.md`](../templates/platform-candidate-backlog.md) |
| Shared library review | Prevent shared code from becoming a ghost platform. | [`shared-library-register.md`](../templates/shared-library-register.md) |
| Skeleton review | Decide whether a service baseline is stable enough to encode. | [`skeleton-readiness-checklist.md`](../templates/skeleton-readiness-checklist.md) |
| Generator review | Prevent generator enthusiasm from outrunning governance. | [`generator-candidate-register.md`](../templates/generator-candidate-register.md) |
| Exception/deviation review | Make deviations visible, time-bounded, and useful. | [`exception-deviation-log.md`](../templates/exception-deviation-log.md) |
| Import review | Decide ownership after platform code enters a product. | [`platform-import-adr.md`](../templates/platform-import-adr.md) |
| Monthly signal review | Keep the loop alive. | [`monthly-platform-signal-review.md`](../runbooks/monthly-platform-signal-review.md) |

## Service boundary gate

A new service needs a reason.

Do not create a service because “microservices” is the target style. Create a service when the boundary is clearer than the coordination cost.

### Extract when one or more of these become clear

- lifecycle differs;
- ownership differs;
- runtime profile differs;
- integration pressure differs;
- isolation or security needs differ;
- read/query pressure differs;
- operational responsibility becomes clearer outside the central backend.

### Keep central or local when

- product meaning is still changing together;
- workflows are still tightly coupled;
- ownership is unclear;
- splitting would turn uncertainty into distributed uncertainty;
- the team cannot operate another boundary;
- the proposed service exists mainly because the diagram would look cleaner.

A new repository is not an architecture decision. It is only where the consequences start paying rent.

## Service archetypes

“Microservice” is too broad to govern.

| Archetype | Platform should standardize | Platform should not over-own |
|---|---|---|
| Domain capability | Service structure, observability, contracts, baseline runtime behavior. | Business meaning and domain invariants. |
| Platform capability | Runtime/security baseline, compatibility rules, operational contracts. | Product-specific policy beyond explicit extension points. |
| Read-model edge | Projection lifecycle, query conventions, refresh behavior, observability. | Canonical domain truth. |
| Integration worker | Retries, idempotency, external boundary handling, failure visibility. | Whole domain workflow outside the integration boundary. |
| Internal tooling | Reproducible setup, configuration safety, local-development ergonomics. | Runtime service governance if it is not a runtime service. |
| Template/generated service | Startup conventions, baseline tests, package structure, extension points. | All future service behavior. |

Treating every service as the same kind of thing creates false consistency. It makes the diagram cleaner and the governance worse.

## Repetition is evidence, not permission

Repetition is the first serious signal. It is not enough by itself.

A repeated concern becomes platform material only when it passes a stronger test:

- it appeared in more than one real service;
- solving it differently creates operational or delivery risk;
- the concern is stable enough to standardize;
- it belongs mostly to execution mechanics, not unstable product meaning;
- the team can define ownership, versioning, and an update path;
- the next service becomes cheaper or safer if this becomes the default.

Without that test, repetition is duplication with better vocabulary.

With that test, repetition becomes architecture evidence.

## Promotion ladder

```text
Local implementation
        |
        | repeats once
        v
Named pattern
        |
        | repeats across services
        v
Shared helper / library candidate
        |
        | stable at service start
        v
Skeleton / template candidate
        |
        | stable, testable, versioned
        v
Generator candidate
        |
        | owned, supported, adopted, governed
        v
Platform / Foundation asset
```

The ladder is not automatic. Every promotion needs evidence, ownership, and a lower cost for the next service.

See [`../diagrams/promotion-ladder.md`](../diagrams/promotion-ladder.md).

## Decision gates

| Gate | Question | Output |
|---|---|---|
| Service candidate | Is the boundary clearer than the coordination cost? | Keep central / extract / revisit. |
| Repeated shape | Is this execution mechanics or unstable product meaning? | Document / keep local / platform candidate. |
| Shared library candidate | Will shared code reduce divergence more than it creates coupling? | Local helper / shared library / wait. |
| Skeleton candidate | Should every new service of this archetype start with this? | Checklist / template / skeleton baseline. |
| Generator candidate | Is the pattern stable enough to encode, test, version, and support? | No generator / scaffold / semantic generator experiment. |
| Governance candidate | Who owns compatibility, support, exceptions, upgrades, and deprecation? | Useful asset / governed platform asset. |

## Failure modes

### Shared library with no constitution

The same shared code appears across services, but nobody knows the source of truth, versioning rule, compatibility policy, or support owner.

Response: run [`shared-library-extraction.md`](../runbooks/shared-library-extraction.md) and record the asset in [`shared-library-register.md`](../templates/shared-library-register.md).

### Skeleton as copy-paste ritual

New services start from a template, then immediately diverge with no update path.

Response: use [`skeleton-readiness-checklist.md`](../templates/skeleton-readiness-checklist.md) before expanding the skeleton.

### Generator before governance

The generator creates files faster than the team can own them.

Response: wait, or record a narrow candidate in [`generator-candidate-register.md`](../templates/generator-candidate-register.md). A generator should encode decisions the team already understands. It should not manufacture uncertainty faster.

### Local deviations hiding as deadlines

Every service has a good local reason to differ. Nobody tracks whether the baseline is wrong or the teams are drifting.

Response: record them in [`exception-deviation-log.md`](../templates/exception-deviation-log.md) and make them time-bounded in the monthly signal review.

## When not to apply bottom-up platform discipline

Do not force this process when:

- the system is still a small single-service product with low repetition;
- service boundaries are mostly speculative;
- the team cannot maintain even lightweight records;
- the decision is a one-off product experiment;
- the repeated concern is clearly product meaning owned by one domain;
- the cure would be heavier than the drift.

Architecture discipline should make platform signals visible. It should not become a tax on every small engineering decision.

## Related files

- [`../templates/service-candidate-register.md`](../templates/service-candidate-register.md)
- [`../templates/repeated-service-shape-ledger.md`](../templates/repeated-service-shape-ledger.md)
- [`../templates/platform-candidate-backlog.md`](../templates/platform-candidate-backlog.md)
- [`../templates/shared-library-register.md`](../templates/shared-library-register.md)
- [`../templates/skeleton-readiness-checklist.md`](../templates/skeleton-readiness-checklist.md)
- [`../templates/generator-candidate-register.md`](../templates/generator-candidate-register.md)
- [`../templates/exception-deviation-log.md`](../templates/exception-deviation-log.md)
- [`../runbooks/new-service-candidate-review.md`](../runbooks/new-service-candidate-review.md)
- [`../runbooks/repeated-pattern-review.md`](../runbooks/repeated-pattern-review.md)
- [`../runbooks/monthly-platform-signal-review.md`](../runbooks/monthly-platform-signal-review.md)
