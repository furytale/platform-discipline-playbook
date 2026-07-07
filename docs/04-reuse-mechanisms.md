# Reuse Mechanisms

## Core idea

The reuse mechanism is an architecture decision.

A local helper, shared library, service skeleton, generator, versioned dependency, vendored package, copied module, and product-integrated core all create different ownership, upgrade, support, and compatibility obligations.

The wrong question is:

> How do we reuse this code?

The better question is:

> What reuse mechanism matches the evidence, adoption cost, ownership model, and governance strength we actually have?

## Mechanism map

| Mechanism | Use when | Do not use when | Ownership implication | Main risk |
|---|---|---|---|---|
| Local implementation | One service has a concern; repetition is unproven. | Divergence is already costly across services. | Local team owns it. | Repeated pain stays invisible. |
| Named pattern | Two or more services solve a concern similarly. | The team needs enforceable consistency now. | Pattern owner or architect tracks it. | Becomes advice nobody follows. |
| Shared helper | Small stable runtime concern repeats. | The helper depends on product meaning. | Helper owner maintains a small surface. | Grows into an accidental framework. |
| Shared library | Repeated execution mechanics are stable and costly to diverge. | Source of truth, versioning, and support are not named. | Library owner owns compatibility and releases. | Ghost platform with no constitution. |
| Service skeleton/template | New services need the same baseline at creation time. | Service archetypes are not stable enough. | Template owner owns generated baseline and update policy. | Copy-paste ritual with no upgrade path. |
| Generator | Stable patterns can be encoded and tested. | The team has not governed the pattern manually yet. | Generator owner owns inputs, templates, outputs, and compatibility. | Faster production of inconsistent architecture. |
| Versioned dependency | Platform remains outside product through a release boundary. | The product needs heavy local adaptation immediately. | Platform team owns releases; consumer owns adoption. | Upgrade friction if compatibility is weak. |
| Vendored or imported code | Product needs local control under delivery pressure. | Nobody defines what flows back or who owns divergence. | Product may become custodian or fork owner. | Platform boundary dissolves silently. |
| Product-integrated core | Reuse must be close to product delivery shape. | The team still expects it to behave like a neutral platform. | Product/platform ownership must be explicit. | Product assumptions leak into reusable asset. |
| Wait / do nothing yet | Repetition is weak, unstable, or mostly product meaning. | Divergence cost is already high. | Local teams keep ownership. | Platform debt may accumulate if not revisited. |

The smallest useful move is usually better than the most impressive abstraction.

## Decision sequence

Before choosing a reuse mechanism, answer:

1. **How many real implementations exist?** One implementation is usually not enough.
2. **What kind of concern is repeating?** Execution mechanics are better platform candidates than product meaning.
3. **What is the cost of divergence?** Inconsistency is not automatically expensive. Some variation is healthy.
4. **Who owns the future cost of change?** Reuse without ownership is debt wearing a helpful name tag.
5. **How will adoption work?** Documentation alone is rarely enough for a broad platform surface.
6. **How will exceptions work?** If teams cannot deviate safely, they will deviate quietly.
7. **How will old versions die?** A shared asset without deprecation becomes archaeology.

## Reuse by evidence level

| Evidence | Smallest useful move |
|---|---|
| One service has a pattern. | Keep local; document if it may repeat. |
| Two services repeat it. | Name the pattern; compare differences. |
| Several services repeat it with costly divergence. | Shared helper or library candidate. |
| New services repeat the same startup baseline. | Skeleton/template candidate. |
| Baseline is stable, testable, and versioned. | Generator candidate. |
| Multiple teams depend on it. | Governance gate before calling it platform. |
| Product code imported platform logic. | Platform import ADR and ownership decision. |

## Mechanism details

### Local implementation

Use local implementation when the pattern is still young. One service can inspire a pattern, but it should not usually define a platform abstraction alone.

Good local implementation still leaves a trace. If the pattern smells reusable, write a short note or link it into the repeated-shape ledger.

**When not to use:** divergence is already causing defects, operational risk, repeated setup cost, or incompatible service behavior.

### Named pattern

A named pattern is useful before shared code. It gives the team language without creating coupling.

Use it for repeated structures that are still being tested:

- use case shape;
- validation boundary;
- integration worker style;
- read-model refresh policy;
- service startup convention.

**When not to use:** teams need a mandatory runtime behavior or compatibility guarantee now.

### Shared helper

A shared helper is smaller than a shared library. It should do one boring thing well.

Good candidates:

- trace context extraction;
- error mapping;
- configuration validation;
- health response shape;
- idempotency key parsing;
- message metadata normalization.

**When not to use:** the helper starts owning product semantics, workflow meaning, or domain policy.

### Shared library

A shared library becomes useful when repeated execution mechanics are stable enough and divergence is expensive.

Before extraction, define:

- source of truth;
- owner;
- supported modules;
- versioning rule;
- compatibility policy;
- upgrade path;
- deprecation plan;
- support boundary.

A shared library is useful because the pain is real. It is risky because it starts acting like a platform before it has platform rules.

Use [`../templates/shared-library-register.md`](../templates/shared-library-register.md) and [`../runbooks/shared-library-extraction.md`](../runbooks/shared-library-extraction.md).

### Skeleton or template

A skeleton makes the right default cheap at service creation time.

Good candidates:

- health and readiness;
- metrics;
- tracing;
- configuration loading;
- logging;
- transport wiring;
- local development setup;
- package conventions;
- minimal test baseline;
- post-generation checklist.

A skeleton is not exciting architecture. That is the point. It makes the boring correct things cheaper than the creative wrong things.

Use [`../templates/skeleton-readiness-checklist.md`](../templates/skeleton-readiness-checklist.md).

### Generator

A generator should encode decisions the team already understands.

Before generator work, define:

- input model;
- generated files;
- handwritten files;
- regeneration policy;
- output tests;
- versioning;
- escape hatches;
- owner;
- adoption rule.

A generator before repetition is speculation. A generator after repeated service shape can become codified learning.

### Versioned dependency

A versioned dependency keeps platform code outside the product boundary. It works well when the platform team can support releases and consumers can absorb upgrades.

Use when:

- compatibility can be stated;
- consumers need a stable boundary;
- platform team owns releases;
- product teams can plan upgrades.

**When not to use:** the product needs heavy local adaptation before the platform has a compatible extension model.

### Vendored or imported code

Vendoring or importing platform code can be practical under delivery pressure. It lowers coordination cost and gives the product local control.

It also changes ownership.

Once platform code enters the product, answer:

- what remains platform-owned?
- what becomes product-owned?
- what changes flow back?
- what stays local?
- who supports divergence?
- when is the import reviewed again?

Use [`../templates/platform-import-adr.md`](../templates/platform-import-adr.md), [`../runbooks/platform-import-review.md`](../runbooks/platform-import-review.md), and [`../diagrams/platform-import-ownership.md`](../diagrams/platform-import-ownership.md).

### Product-integrated core

A product-integrated core can be a valid reuse shape when teams need shared packages, reusable service structures, and common runtime conventions close to product delivery.

It is not automatically better than a reusable-bricks platform. It is closer to the product, which can reduce adoption load and increase local usefulness. It can also leak product assumptions into shared assets and make later extraction harder.

Use only with explicit ownership rules.

### Wait

Waiting is a real architecture move.

Use it when the team has not seen enough repetition, the concern is mostly product meaning, or governance would cost more than divergence.

Do not wait quietly. Add a revisit trigger.

## Mechanism selection checklist

```text
Repeated?                  yes / no / partial
Stable?                    yes / no / partial
Mostly execution mechanics? yes / no / mixed
Costly to diverge?          low / medium / high
Owner named?                yes / no
Adoption path clear?        yes / no
Exception path clear?       yes / no
Upgrade path clear?         yes / no
Smallest useful move?       local / pattern / helper / library / skeleton / generator / import ADR / wait
```

## Anti-patterns

### Framework looking for adoption

The team builds a broad reusable layer before real consumers prove the shape.

Response: shrink the promise. Extract from repeated delivery pain, not from hope.

### Shared library as unofficial platform

Many services depend on it. Nobody owns compatibility.

Response: record it in [`platform-candidate-backlog.md`](../templates/platform-candidate-backlog.md) and run the governance gate.

### Generator as theatre

Generated output looks consistent, but generated services diverge immediately.

Response: record the candidate in [`generator-candidate-register.md`](../templates/generator-candidate-register.md), test the output, define regeneration rules, and keep generator scope small.

### Vendoring as fake governance

Code is copied into the product and everyone assumes the platform still owns it.

Response: write the import ADR. The future cost of change needs an owner.

### Product-integrated core as accidental platform

Product-local packages start being reused elsewhere, but still carry one product's assumptions.

Response: classify the asset. Either keep it product-owned or productize it deliberately.

## Related files

- [`../templates/platform-candidate-backlog.md`](../templates/platform-candidate-backlog.md)
- [`../templates/shared-library-register.md`](../templates/shared-library-register.md)
- [`../templates/skeleton-readiness-checklist.md`](../templates/skeleton-readiness-checklist.md)
- [`../templates/generator-candidate-register.md`](../templates/generator-candidate-register.md)
- [`../templates/exception-deviation-log.md`](../templates/exception-deviation-log.md)
- [`../templates/platform-import-adr.md`](../templates/platform-import-adr.md)
- [`../runbooks/repeated-pattern-review.md`](../runbooks/repeated-pattern-review.md)
- [`../runbooks/shared-library-extraction.md`](../runbooks/shared-library-extraction.md)
- [`../runbooks/platform-import-review.md`](../runbooks/platform-import-review.md)
