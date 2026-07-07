# Introduction

## The point of this playbook

This playbook helps engineering leaders decide when repeated delivery pain should become platform work and when it should stay local.

The core thesis is simple:

> Reusable code becomes a platform asset only when it has ownership, versioning, adoption rules, support, compatibility policy, exception handling, and a team model around it.

A shared library can be valuable. A service skeleton can save time. A generator can encode learning. A vendored core package can help a product move. None of those are automatically a platform.

The platform is the agreement around the reusable asset: what it owns, what it does not own, how teams adopt it, how exceptions work, who supports it, how compatibility is protected, and who pays the cost of keeping the boundary true.

## Playbook versus runbook versus template

| Artifact | Use it when | Output |
|---|---|---|
| Playbook | You need a decision model or trade-off lens. | A clearer architectural choice. |
| Runbook | The same situation happens repeatedly. | A consistent procedure and recorded decision. |
| Template | The team needs a lightweight record. | A fillable artifact. |
| Diagram | The decision model needs to be explained quickly. | A clean-room visual. |

A playbook says: **how should we think about this?**

A runbook says: **what do we do when this trigger appears?**

A template says: **what must be recorded so the decision does not evaporate?**

A diagram says: **how do we make the model visible without leaking real architecture?**

## Vocabulary

### Platform candidate

A repeated concern, pattern, helper, template, or imported asset that might become platform material, but is not yet governed enough to be treated as a platform asset.

### Platform asset

A reusable capability with explicit ownership, source of truth, versioning, support, compatibility policy, adoption rules, exception handling, and lifecycle management.

### Foundation

A governed set of reusable execution, integration, service-construction, and operational primitives that should stay coherent across product or client delivery.

Foundation should not mean “large framework.” A smaller, governed asset is healthier than a broad reusable promise nobody can support.

### Execution mechanics

Cross-cutting runtime concerns such as configuration, logging, tracing, health checks, metrics, transaction handling, idempotency, durable event propagation, messaging envelopes, use case execution, and service startup conventions.

### Product meaning

Domain-specific behavior, business semantics, workflow meaning, customer-specific policy, product rules, and domain invariants. These usually belong to product/domain ownership, not to a general platform.

### Governance

The operating model that keeps reusable assets coherent under delivery pressure: ownership, versioning, support, exceptions, compatibility, adoption, deprecation, conformance, and review cadence.

### Team API

The way a team exposes its platform capability to other teams: documentation, examples, support channel, roadmap, versioning policy, contribution rules, escalation path, adoption path, and exception process.

## The recurring decision

Most platform questions hide the same decision:

> What should stay local, what should become reusable, and what is governed strongly enough to become platform material?

Use this sequence:

1. **Notice repetition.** What keeps appearing across services or product areas?
2. **Classify the concern.** Is it execution mechanics or product meaning?
3. **Estimate divergence cost.** What happens if every team keeps doing it differently?
4. **Choose the smallest useful move.** Document, helper, shared library, skeleton, generator, import rule, or wait.
5. **Assign ownership.** Who owns the future cost of change?
6. **Define adoption and exceptions.** How do teams use it, and when may they deviate?
7. **Review periodically.** A useful asset can drift into platform debt if nobody watches it.

## When to use this repo

Use it when:

- services repeat the same setup and runtime concerns;
- a shared library is becoming an unofficial platform;
- a service skeleton is being proposed;
- a generator is tempting the team before the pattern is stable;
- platform code is imported, copied, vendored, generated, or locally adapted;
- product teams are bypassing platform defaults;
- nobody can say who owns compatibility or support;
- platform work is becoming hidden labor under delivery pressure.

## When not to use this repo

Do not use it as a process tax when:

- the concern exists in only one implementation and is not inherently cross-cutting;
- product meaning is still too unstable to standardize;
- the team cannot name an owner;
- a local decision is cheaper and has low divergence risk;
- the template would create records nobody reads;
- the runbook would slow urgent recovery work;
- the real issue is lack of product direction, not lack of platform discipline.

The point is not to make every decision heavier. The point is to keep the expensive ones from becoming invisible.

## Public-safe use

This repository is designed for public sharing. Keep it clean-room:

- use generic service archetypes;
- use synthetic examples;
- use abstract diagrams;
- avoid exact timelines and identifying technology clusters;
- do not paste real ADRs, logs, schemas, names, repository paths, or internal diagrams.

Useful architecture writing does not require exposing the client. Preserve the forces, trade-offs, and lessons. Remove the fingerprints.

## Related files

- [`01-bottom-up-platform-discipline.md`](01-bottom-up-platform-discipline.md)
- [`04-reuse-mechanisms.md`](04-reuse-mechanisms.md)
- [`05-governance-operating-model.md`](05-governance-operating-model.md)
- [`../templates/platform-candidate-backlog.md`](../templates/platform-candidate-backlog.md)
- [`../templates/generator-candidate-register.md`](../templates/generator-candidate-register.md)
- [`../templates/exception-deviation-log.md`](../templates/exception-deviation-log.md)
- [`../diagrams/platform-signal-loop.md`](../diagrams/platform-signal-loop.md)
- [`../diagrams/promotion-ladder.md`](../diagrams/promotion-ladder.md)
