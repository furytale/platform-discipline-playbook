# Platform Discipline Playbook

Reusable code is not a platform.

A shared library, template, generator, vendored package, product-integrated core, or service skeleton can become a platform asset only when it has ownership, versioning, adoption rules, support, compatibility policy, exception handling, and a team model around it.

This repository is a public, clean-room companion asset for a professional article series about platform foundations, software architecture, governance, and technical leadership.

The articles provide the narrative and decision argument. This repository provides the practical method: playbook sections, runbooks, templates, and diagrams.

## Who this is for

- CTOs and technical founders deciding whether platform work deserves capacity.
- Engineering managers and engineering leads trying to keep delivery pressure from turning into architecture drift.
- Principal architects, staff engineers, solution architects, and platform engineers designing reusable execution capability.
- Outsourcing technical leaders and platform/product leaders who need to separate client-product delivery from reusable platform stewardship.

## What this repository helps you decide

Use this playbook when a team needs to answer questions like:

- Is this repeated backend pain a platform signal or just local duplication?
- Should this capability stay inside the current service, become a documented pattern, move into a shared helper, become a shared library, enter a skeleton, or wait?
- When is a service skeleton useful, and when is it just copy-paste with better posture?
- When is an execution-core Foundation justified before product semantics are stable?
- Where should metadata/configuration stop, and where should typed execution remain?
- What changes when platform code is imported, vendored, generated, copied, forked, or locally adapted inside a product?
- Who owns compatibility, support, exceptions, adoption, upgrade cost, and runtime responsibility?
- What team topology is needed so platform adoption does not become one architect's private hobby?
- What should the team do every month so platform discipline does not depend on one architect's memory?

This playbook is not a platform religion. It is a set of decision aids for teams trying to keep reusable code from becoming unmanaged infrastructure folklore.

## Repository map

| Area | Purpose |
|---|---|
| [`docs/`](docs/) | Playbook sections: how to think and decide. |
| [`templates/`](templates/) | Fillable artifacts: what to record. |
| [`runbooks/`](runbooks/) | Repeatable procedures: what to do when a trigger appears. |
| [`diagrams/`](diagrams/) | Clean-room decision diagrams for articles, reviews, and internal conversations. |

## Start here

1. Read [`docs/00-introduction.md`](docs/00-introduction.md) to understand the vocabulary and boundaries.
2. Use [`docs/01-bottom-up-platform-discipline.md`](docs/01-bottom-up-platform-discipline.md) when a full platform is too early, but backend growth already needs discipline.
3. Use [`docs/02-execution-core-foundation.md`](docs/02-execution-core-foundation.md) when stable execution mechanics justify deliberate Foundation scope.
4. Use [`docs/03-typed-core-metadata-edges.md`](docs/03-typed-core-metadata-edges.md) when configurable behavior appears and the team needs to keep metadata at bounded semantic edges.
5. Use [`docs/04-reuse-mechanisms.md`](docs/04-reuse-mechanisms.md) to choose the smallest useful reuse mechanism.
6. Use [`docs/05-governance-operating-model.md`](docs/05-governance-operating-model.md) before calling any reusable asset a platform asset.
7. Use [`docs/06-outsourcing-platform-governance.md`](docs/06-outsourcing-platform-governance.md) when client-owned delivery and platform stewardship compete for the same capacity.
8. Use [`docs/07-platform-productization-for-outsourcing.md`](docs/07-platform-productization-for-outsourcing.md) when reusable assets need productization, not only reuse.
9. Use [`docs/08-team-topology-and-team-api.md`](docs/08-team-topology-and-team-api.md) when platform adoption depends on support, enablement, interaction mode, and ownership boundaries.
10. Use the runbooks when the work becomes recurring.

## Playbook, runbook, template, diagram

| Artifact type | Meaning | Example |
|---|---|---|
| Playbook | How to think and decide. | Should repeated service setup become a platform candidate? |
| Runbook | What to do repeatedly. | Run the repeated-pattern review. |
| Template | What to fill in. | Record a service candidate decision. |
| Diagram | How to explain the model. | Show the platform signal loop. |

## Current contents

### Playbook sections

- [`docs/00-introduction.md`](docs/00-introduction.md)
- [`docs/01-bottom-up-platform-discipline.md`](docs/01-bottom-up-platform-discipline.md)
- [`docs/02-execution-core-foundation.md`](docs/02-execution-core-foundation.md)
- [`docs/03-typed-core-metadata-edges.md`](docs/03-typed-core-metadata-edges.md)
- [`docs/04-reuse-mechanisms.md`](docs/04-reuse-mechanisms.md)
- [`docs/05-governance-operating-model.md`](docs/05-governance-operating-model.md)
- [`docs/06-outsourcing-platform-governance.md`](docs/06-outsourcing-platform-governance.md)
- [`docs/07-platform-productization-for-outsourcing.md`](docs/07-platform-productization-for-outsourcing.md)
- [`docs/08-team-topology-and-team-api.md`](docs/08-team-topology-and-team-api.md)

### Templates

- [`templates/service-candidate-register.md`](templates/service-candidate-register.md)
- [`templates/repeated-service-shape-ledger.md`](templates/repeated-service-shape-ledger.md)
- [`templates/platform-candidate-backlog.md`](templates/platform-candidate-backlog.md)
- [`templates/shared-library-register.md`](templates/shared-library-register.md)
- [`templates/skeleton-readiness-checklist.md`](templates/skeleton-readiness-checklist.md)
- [`templates/generator-candidate-register.md`](templates/generator-candidate-register.md)
- [`templates/exception-deviation-log.md`](templates/exception-deviation-log.md)
- [`templates/platform-import-adr.md`](templates/platform-import-adr.md)
- [`templates/execution-core-scope-map.md`](templates/execution-core-scope-map.md)
- [`templates/foundation-capability-register.md`](templates/foundation-capability-register.md)
- [`templates/platform-drift-assessment.md`](templates/platform-drift-assessment.md)
- [`templates/metadata-edge-candidate.md`](templates/metadata-edge-candidate.md)
- [`templates/architecture-to-delivery-governance-map.md`](templates/architecture-to-delivery-governance-map.md)
- [`templates/platform-funding-model.md`](templates/platform-funding-model.md)
- [`templates/team-api.md`](templates/team-api.md)
- [`templates/platform-ownership-split.md`](templates/platform-ownership-split.md)
- [`templates/reusable-asset-productization-checklist.md`](templates/reusable-asset-productization-checklist.md)
- [`templates/platform-adoption-plan.md`](templates/platform-adoption-plan.md)

### Runbooks

- [`runbooks/new-service-candidate-review.md`](runbooks/new-service-candidate-review.md)
- [`runbooks/repeated-pattern-review.md`](runbooks/repeated-pattern-review.md)
- [`runbooks/shared-library-extraction.md`](runbooks/shared-library-extraction.md)
- [`runbooks/platform-import-review.md`](runbooks/platform-import-review.md)
- [`runbooks/monthly-platform-signal-review.md`](runbooks/monthly-platform-signal-review.md)
- [`runbooks/foundation-scope-review.md`](runbooks/foundation-scope-review.md)
- [`runbooks/platform-drift-review.md`](runbooks/platform-drift-review.md)
- [`runbooks/metadata-edge-review.md`](runbooks/metadata-edge-review.md)
- [`runbooks/execution-core-conformance-review.md`](runbooks/execution-core-conformance-review.md)
- [`runbooks/architecture-to-delivery-governance.md`](runbooks/architecture-to-delivery-governance.md)
- [`runbooks/outsourcing-platform-scope-review.md`](runbooks/outsourcing-platform-scope-review.md)
- [`runbooks/platform-funding-review.md`](runbooks/platform-funding-review.md)
- [`runbooks/team-topology-review.md`](runbooks/team-topology-review.md)
- [`runbooks/reusable-asset-productization-review.md`](runbooks/reusable-asset-productization-review.md)
- [`runbooks/consumer-onboarding.md`](runbooks/consumer-onboarding.md)
- [`runbooks/platform-asset-deprecation.md`](runbooks/platform-asset-deprecation.md)

### Diagrams

- [`diagrams/platform-signal-loop.md`](diagrams/platform-signal-loop.md)
- [`diagrams/promotion-ladder.md`](diagrams/promotion-ladder.md)
- [`diagrams/platform-import-ownership.md`](diagrams/platform-import-ownership.md)
- [`diagrams/execution-core-boundary.md`](diagrams/execution-core-boundary.md)
- [`diagrams/typed-core-metadata-edges.md`](diagrams/typed-core-metadata-edges.md)
- [`diagrams/foundation-governance-loop.md`](diagrams/foundation-governance-loop.md)
- [`diagrams/platform-drift-loop.md`](diagrams/platform-drift-loop.md)
- [`diagrams/platform-team-api.md`](diagrams/platform-team-api.md)
- [`diagrams/outsourcing-platform-funding-loop.md`](diagrams/outsourcing-platform-funding-loop.md)
- [`diagrams/platform-ownership-split.md`](diagrams/platform-ownership-split.md)
- [`diagrams/reusable-asset-productization-funnel.md`](diagrams/reusable-asset-productization-funnel.md)
- [`diagrams/stream-aligned-vs-platform-team.md`](diagrams/stream-aligned-vs-platform-team.md)

## Article companion map

| Article type | Recommended repo links |
|---|---|
| Platform discipline before platform | `docs/01-bottom-up-platform-discipline.md`, `templates/service-candidate-register.md`, `templates/repeated-service-shape-ledger.md`, `templates/platform-candidate-backlog.md`, `templates/skeleton-readiness-checklist.md`, `templates/generator-candidate-register.md`, `templates/exception-deviation-log.md`, `diagrams/platform-signal-loop.md`, `diagrams/promotion-ladder.md`, `runbooks/monthly-platform-signal-review.md` |
| Execution-core Foundation under product uncertainty | [`docs/02-execution-core-foundation.md`](docs/02-execution-core-foundation.md), [`docs/03-typed-core-metadata-edges.md`](docs/03-typed-core-metadata-edges.md), [`templates/execution-core-scope-map.md`](templates/execution-core-scope-map.md), [`templates/foundation-capability-register.md`](templates/foundation-capability-register.md), [`templates/platform-drift-assessment.md`](templates/platform-drift-assessment.md), [`templates/metadata-edge-candidate.md`](templates/metadata-edge-candidate.md), [`runbooks/foundation-scope-review.md`](runbooks/foundation-scope-review.md), [`runbooks/platform-drift-review.md`](runbooks/platform-drift-review.md), [`runbooks/metadata-edge-review.md`](runbooks/metadata-edge-review.md), [`runbooks/execution-core-conformance-review.md`](runbooks/execution-core-conformance-review.md), [`diagrams/execution-core-boundary.md`](diagrams/execution-core-boundary.md), [`diagrams/typed-core-metadata-edges.md`](diagrams/typed-core-metadata-edges.md), [`diagrams/foundation-governance-loop.md`](diagrams/foundation-governance-loop.md) |
| Platform reuse under outsourcing/client-owned constraints | [`docs/06-outsourcing-platform-governance.md`](docs/06-outsourcing-platform-governance.md), [`docs/07-platform-productization-for-outsourcing.md`](docs/07-platform-productization-for-outsourcing.md), [`docs/08-team-topology-and-team-api.md`](docs/08-team-topology-and-team-api.md), [`templates/platform-funding-model.md`](templates/platform-funding-model.md), [`templates/team-api.md`](templates/team-api.md), [`templates/platform-ownership-split.md`](templates/platform-ownership-split.md), [`templates/reusable-asset-productization-checklist.md`](templates/reusable-asset-productization-checklist.md), [`templates/platform-adoption-plan.md`](templates/platform-adoption-plan.md), [`templates/platform-import-adr.md`](templates/platform-import-adr.md), [`runbooks/outsourcing-platform-scope-review.md`](runbooks/outsourcing-platform-scope-review.md), [`runbooks/platform-funding-review.md`](runbooks/platform-funding-review.md), [`runbooks/platform-import-review.md`](runbooks/platform-import-review.md), [`runbooks/team-topology-review.md`](runbooks/team-topology-review.md), [`runbooks/reusable-asset-productization-review.md`](runbooks/reusable-asset-productization-review.md), [`runbooks/consumer-onboarding.md`](runbooks/consumer-onboarding.md), [`runbooks/platform-asset-deprecation.md`](runbooks/platform-asset-deprecation.md), [`diagrams/platform-import-ownership.md`](diagrams/platform-import-ownership.md), [`diagrams/platform-team-api.md`](diagrams/platform-team-api.md), [`diagrams/outsourcing-platform-funding-loop.md`](diagrams/outsourcing-platform-funding-loop.md), [`diagrams/platform-ownership-split.md`](diagrams/platform-ownership-split.md) |
| Synthesis: reusable code is not a platform | `README.md`, [`docs/04-reuse-mechanisms.md`](docs/04-reuse-mechanisms.md), [`docs/05-governance-operating-model.md`](docs/05-governance-operating-model.md), [`docs/08-team-topology-and-team-api.md`](docs/08-team-topology-and-team-api.md) |

## Clean-room and confidentiality posture

All examples in this repository are synthetic and generalized. They are designed to illustrate decision models, not to document any specific client or product architecture.

Do not add real company names, product names, personal names, repository names, service names, schemas, field names, queue names, event names, file paths, commit hashes, logs, screenshots, internal diagrams, exact timelines, vendors, security findings, payment details, production incidents, or raw evidence.

Use this repository as a public-safe method library, not as a second evidence repository.

## What this is not

This is not:

- a universal methodology;
- a maturity model;
- a certification framework;
- a consulting slide deck in Markdown clothing;
- a claim that platforms should always be built early;
- a claim that platforms should always wait;
- a claim that metadata should replace typed product logic;
- a claim that outsourcing makes platforms impossible;
- a claim that generators, templates, shared libraries, imports, vendored code, or product-integrated cores solve governance by themselves.

Adapt it. Do not adopt it blindly.

## Working principle

Build enough product to see repetition. Keep enough discipline that repetition is visible. Standardize stable execution mechanics when they are known. Keep product meaning owned. Productize reusable assets before calling them a platform. Govern the boundary before shared code becomes shared chaos.
