# Repeated Pattern Review Runbook

## Purpose

Review repeated service concerns and decide the smallest useful move.

The goal is not to platformize every repeated thing. The goal is to distinguish useful variation from expensive divergence.

## Trigger

Run this when:

- the repeated service-shape ledger has new entries;
- two or more services solve the same execution concern differently;
- a shared helper is being requested;
- a template or skeleton addition is proposed;
- a local deviation appears more than once;
- monthly platform signal review identifies a recurring concern.

## Inputs

- [`../templates/repeated-service-shape-ledger.md`](../templates/repeated-service-shape-ledger.md)
- Service candidate records.
- Existing shared library register entries.
- Skeleton readiness checklist entries.
- [`../templates/exception-deviation-log.md`](../templates/exception-deviation-log.md).
- Consumer feedback or support requests.

## Participants

| Role | Responsibility |
|---|---|
| Architect / technical lead | Classification and promotion decision. |
| Senior engineers | Validate whether repetition is real and stable. |
| Platform owner, if one exists | Owns candidate promotion, compatibility, and adoption impact. |
| Delivery lead | Confirms capacity and timing. |
| Product/domain owner, if product meaning is involved | Confirms semantic ownership. |

## Procedure

### 1. Select candidate patterns

Pick ledger entries with one or more of these signals:

- repeated in several services;
- divergence risk medium or high;
- repeated implementation complaints;
- local patches accumulating;
- repeated onboarding/setup cost;
- operational inconsistency;
- support requests;
- template edits after service creation.

### 2. Classify the concern

Ask:

- Is this execution mechanics or product meaning?
- Is the concern stable enough to standardize?
- Do service archetypes need different behavior?
- Does every service need this at startup?
- Is the repeated solution actually good, or just familiar?

If the concern is mostly product meaning, keep it domain-owned. A platform should not absorb semantics just because semantics repeated.

### 3. Estimate divergence cost

Use this scale:

| Risk | Meaning |
|---|---|
| Low | Differences are harmless or intentionally local. |
| Medium | Differences create onboarding, maintenance, or review cost. |
| High | Differences create defects, security gaps, runtime risk, integration failure, or incompatible service behavior. |

Only high or repeated medium risk usually justifies shared implementation.

### 4. Choose the smallest useful move

| Move | Use when |
|---|---|
| Keep local | Repetition is weak or variation is useful. |
| Document pattern | The team needs shared language but not shared code. |
| Reference example | One implementation is strong enough to teach, not govern. |
| Shared helper | A small stable execution concern repeats. |
| Shared library candidate | Several services need the same stable execution mechanics. |
| Skeleton/template candidate | The concern belongs at service creation time. |
| Generator candidate | The baseline is stable, testable, versioned, and owned. |
| Governance rule | Multiple consumers depend on consistency. |
| Exception review | Deviation is real and should be time-bounded. |
| Revisit later | Product or ownership is still too unclear. |

The smallest useful move is usually the safest one.

### 5. Assign owner and next artifact

| Move | Required artifact |
|---|---|
| Platform candidate | [`../templates/platform-candidate-backlog.md`](../templates/platform-candidate-backlog.md) |
| Shared library candidate | [`../templates/shared-library-register.md`](../templates/shared-library-register.md) |
| Skeleton/template candidate | [`../templates/skeleton-readiness-checklist.md`](../templates/skeleton-readiness-checklist.md) |
| Generator candidate | [`../templates/generator-candidate-register.md`](../templates/generator-candidate-register.md) |
| Platform import or local adaptation | [`../templates/platform-import-adr.md`](../templates/platform-import-adr.md) |
| Service boundary impact | [`../templates/service-candidate-register.md`](../templates/service-candidate-register.md) |
| Exception/deviation | [`../templates/exception-deviation-log.md`](../templates/exception-deviation-log.md) |
| Governance promotion | [`../docs/05-governance-operating-model.md`](../docs/05-governance-operating-model.md) gate |

No owner, no promotion.

### 6. Record decision

Update the repeated service-shape ledger with:

- decision;
- rationale;
- owner;
- next artifact;
- revisit trigger;
- exception if needed.

## Completion criteria

The review is complete when:

- each selected pattern has a decision;
- no candidate is promoted without owner;
- product meaning is not accidentally platformized;
- next artifacts are created where needed;
- revisit triggers are recorded;
- monthly signal review can track the outcome.

## No-go signals

Do not promote a pattern when:

- it appears in only one service and is not inherently cross-cutting;
- the repeated code is copied but not understood;
- product semantics are still unstable;
- service archetypes need different behavior;
- the shared abstraction would be larger than the repeated problem;
- no team can support it;
- the main motivation is “we should have a platform.”

## Outputs

- Updated repeated service-shape ledger.
- New platform-candidate backlog entry, if needed.
- New shared-library register entry, if needed.
- New skeleton readiness checklist, if needed.
- New generator-candidate register entry, if needed.
- New platform import ADR, if needed.
- Governance gate action, if asset is approaching platform status.
- Exception/deviation entry in [`../templates/exception-deviation-log.md`](../templates/exception-deviation-log.md), if local variation should remain visible.

## Reminder

Repetition is the smoke. Platform extraction starts only after the team understands what is burning, whether it will appear again, and who owns the extinguisher.
