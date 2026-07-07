# Platform Funding Review Runbook

## Purpose

Review platform work hidden inside product delivery, then decide whether to fund it, reduce it, defer it, keep it local, or stop calling it platform work.

## Trigger

Run this when:

- platform work is expected inside product delivery;
- adoption/support/compatibility/migration/docs are not funded;
- platform owner lacks capacity;
- platform roadmap competes with client/product deadlines.

## Inputs

- Candidate platform asset.
- Work types required.
- Current funding/capacity.
- Current owners.
- Consumer/adoption needs.
- Support expectations.

## Participants

| Role | Responsibility |
|---|---|
| Architect / technical lead | checks boundary and decision quality |
| Owner | accepts future cost |
| Consumer representative | validates adoption and usability |
| Delivery lead | confirms capacity and delivery impact |

## Procedure

### 1. List platform tasks

Classify build, adoption, support, education, docs, examples, compatibility, migration, productization, evolution, and deprecation.

### 2. Identify funding owner

Choose client project, central platform budget, shared investment, internal accelerator, or unfunded/hidden.

### 3. Identify capacity

Name who has time, review cadence, support owner, migration owner, and conflict rule when product delivery competes with support.

### 4. Decide

Fund, reduce scope, defer, keep local, treat as internal accelerator, productize later, abandon, or accept explicit risk.

### 5. Update roadmap or scope

Do not leave the decision as `we will see`. That phrase has escorted many platforms into the swamp.

## Outputs

- Completed funding model.
- Scope decision.
- Capacity decision.
- Risk record.
- Roadmap update.

## Completion criteria

- Every work type has funding status.
- Unfunded work has explicit decision.
- Ambition matches capacity.
- Owners are named.

## No-go signals

- Funding source is `whoever has time`.
- Adoption requires enablement but no enabling role exists.
- Nobody owns asset after delivery.

## Public-safe reminder

Keep entries generalized and synthetic. Do not record real service names, repo paths, commits, schemas, queue/event/table names, screenshots, logs, vendors, exact timelines, payment/security/compliance details, or identifiable client/project facts.

## Related files

- [`../templates/platform-funding-model.md`](../templates/platform-funding-model.md)
- [`../diagrams/outsourcing-platform-funding-loop.md`](../diagrams/outsourcing-platform-funding-loop.md)
