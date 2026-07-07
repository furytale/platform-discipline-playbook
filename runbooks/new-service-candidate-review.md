# New Service Candidate Review Runbook

## Purpose

Decide whether a new service should exist separately or whether the capability should remain inside the current backend, product service, or module.

The goal is not to prevent service extraction. The goal is to make service extraction a decision, not a reflex.

## Trigger

Run this when:

- a new service is proposed;
- a major capability is being extracted;
- a module is becoming independently owned or operated;
- a team wants a new deployable unit;
- a product boundary appears to need its own lifecycle.

Do not run it for tiny internal refactors with low architectural impact.

## Inputs

- Proposed capability description.
- Current implementation location.
- Expected ownership boundary.
- Runtime or operational reason for separation.
- Expected consumers.
- Known repeated concerns.
- Any existing ADRs or architecture notes.
- Current service archetype if known.

Use public-safe generalized labels in any shared copy.

## Participants

| Role | Responsibility |
|---|---|
| Architect / technical lead | Boundary review and platform-signal classification. |
| Senior engineer(s) | Implementation reality check. |
| Engineering manager / delivery lead | Capacity and delivery trade-off. |
| Product/domain representative | Product ownership and semantic boundary. |
| Platform owner, if one exists | Baseline, templates, support, and adoption impact. |

## Procedure

### 1. State the candidate

Fill the summary section in [`../templates/service-candidate-register.md`](../templates/service-candidate-register.md).

Do not begin with technology. Begin with capability and ownership.

### 2. Test the boundary

Ask:

- What does this candidate own?
- What does it explicitly not own?
- Is the boundary clearer than the coordination cost?
- Is ownership clearer outside the current service?
- Does runtime operation justify separation?
- Does the capability have a different lifecycle?
- Would splitting now create distributed uncertainty?

If the boundary is not clearer than the coordination cost, keep it central/local and improve seams.

### 3. Classify the service archetype

Choose the closest archetype:

- domain capability;
- platform capability;
- read-model edge;
- integration worker;
- internal tooling;
- template/generated service;
- other.

Different archetypes need different governance. Do not force one service shape onto everything.

### 4. Identify repeated concerns

Record what this candidate repeats from previous services:

- configuration;
- logging;
- tracing;
- error mapping;
- auth integration;
- validation;
- transaction boundary;
- messaging envelope;
- idempotency;
- health/readiness;
- metrics;
- service startup structure;
- test baseline;
- deployment/runtime assumptions.

Feed repeated items into [`../templates/repeated-service-shape-ledger.md`](../templates/repeated-service-shape-ledger.md). If the concern may become platform material, add it to [`../templates/platform-candidate-backlog.md`](../templates/platform-candidate-backlog.md).

### 5. Decide the service move

Choose one:

| Decision | Use when |
|---|---|
| Keep central/local | Boundary or ownership is unclear. |
| Extract now | Boundary, ownership, runtime, and integration contract are clear enough. |
| Extract later | Direction is likely, but more product evidence is needed. |
| Document pattern only | Repetition exists, but service boundary is not ready. |
| Create shared helper/library candidate | Repeated execution concern is stable and costly to diverge. |
| Create skeleton candidate | Repeated service startup baseline is stable enough to review. |
| Revisit | Product meaning is still moving. |

### 6. Record decision and follow-up

Update the service candidate register with:

- decision;
- reason;
- owner;
- expected consumers;
- repeated concerns;
- follow-up actions;
- revisit trigger.

If extraction is accepted, also record:

- service archetype;
- runtime ownership;
- support expectation;
- baseline template or skeleton to use;
- exceptions from baseline.

## Completion criteria

The review is complete when:

- the candidate is recorded;
- the boundary decision is explicit;
- service archetype is selected;
- owner is named;
- runtime responsibility is clear enough;
- repeated concerns are logged;
- follow-up actions have owners;
- revisit trigger exists if decision is delayed.

## Exception path

If delivery pressure requires creating the service before full review:

1. create a temporary entry in [`../templates/exception-deviation-log.md`](../templates/exception-deviation-log.md);
2. name the risk;
3. define the revisit trigger;
4. schedule the post-service review;
5. avoid presenting the rushed boundary as the final architecture.

Fast decisions are sometimes necessary. Invisible decisions are optional.

## Common failure modes

### Service created because the diagram looked cleaner

Response: force the boundary test. A clean diagram does not operate the service.

### Service extracted without runtime owner

Response: block extraction or name temporary operational ownership.

### Product semantics split too early

Response: keep local until ownership and invariants become clearer.

### Repetition noticed but not recorded

Response: update the repeated service-shape ledger before closing the review.

## Outputs

- Updated [`service-candidate-register.md`](../templates/service-candidate-register.md).
- Updated [`repeated-service-shape-ledger.md`](../templates/repeated-service-shape-ledger.md), if repeated concerns were found.
- New or updated ADR, if needed.
- Exception/deviation entry in [`../templates/exception-deviation-log.md`](../templates/exception-deviation-log.md), if deviating from baseline.
- Follow-up item for monthly platform signal review.
