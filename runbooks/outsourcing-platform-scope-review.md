# Outsourcing Platform Scope Review Runbook

## Purpose

Run before promising platform reuse inside client/product delivery. Separate feature delivery from platform stewardship before both are quietly assigned to the same calendar.

## Trigger

Run this when:

- client/product delivery includes reusable platform ambition;
- reusable assets are proposed as delivery accelerators;
- one engagement is expected to create assets for future engagements;
- support/evolution responsibilities are unclear.

## Inputs

- Product delivery obligations, generalized.
- Proposed reusable platform work.
- Existing platform assets/candidates.
- Funding model.
- Team topology assumptions.
- Import/adoption mechanism.

## Participants

| Role | Responsibility |
|---|---|
| Architect / technical lead | checks boundary and decision quality |
| Owner | accepts future cost |
| Consumer representative | validates adoption and usability |
| Delivery lead | confirms capacity and delivery impact |

## Procedure

### 1. Define product delivery obligations

Name what the product must ship in generalized terms. Do not hide platform work behind feature labels.

### 2. Identify reusable platform work

List reusable packages, skeletons, shared primitives, product-integrated core, migration helpers, docs/examples, support, compatibility work.

### 3. Separate product work from stewardship

Classify each item as product delivery, platform build, platform adoption, support, compatibility/migration, productization, deprecation, or unknown.

### 4. Decide platform scope

Choose no platform scope, internal accelerator, product-local reusable core, funded platform asset, platform experiment with expiry, or block until owner/funding exists.

### 5. Record what remains local

Local is fine. Unowned is not.

## Outputs

- Scope decision.
- Funding model update.
- Ownership split.
- Adoption plan or import ADR if needed.
- Risks.

## Completion criteria

- Product and platform work are separated.
- Funding/capacity are named or scope is reduced.
- Support/compatibility are not assumed.

## No-go signals

- No one funds adoption/support.
- No owner accepts responsibility.
- Product team is expected to absorb platform ownership silently.

## Public-safe reminder

Keep entries generalized and synthetic. Do not record real service names, repo paths, commits, schemas, queue/event/table names, screenshots, logs, vendors, exact timelines, payment/security/compliance details, or identifiable client/project facts.

## Related files

- [`../templates/platform-funding-model.md`](../templates/platform-funding-model.md)
- [`../templates/platform-ownership-split.md`](../templates/platform-ownership-split.md)
