# Reusable Asset Productization Review Runbook

## Purpose

Decide whether an asset from one product, client delivery, or internal accelerator can become a reusable platform asset.

## Trigger

Run this when:

- code from one context may be reused elsewhere;
- an internal accelerator gains consumers;
- product-integrated core starts looking reusable;
- old project artifacts are proposed as platform material.

## Inputs

- Candidate asset.
- Original context, generalized.
- Expected consumers.
- Known assumptions.
- Packaging/versioning.
- Support/funding expectations.

## Participants

| Role | Responsibility |
|---|---|
| Architect / technical lead | checks boundary and decision quality |
| Owner | accepts future cost |
| Consumer representative | validates adoption and usability |
| Delivery lead | confirms capacity and delivery impact |

## Procedure

### 1. Remove local assumptions

List assumptions that must be removed, named, or turned into extension points. If they cannot be separated, keep product-local.

### 2. Define generic capability

Write: `This asset provides X for Y consumer archetypes.` If this only makes sense in one product, do not productize yet.

### 3. Define packaging and versioning

Choose shared package, service template, generator output, internal accelerator, product-integrated core, productized service, or not ready.

### 4. Define docs and examples

Confirm a new consumer can use this without private history, with supported and unsupported uses clear.

### 5. Define support and funding

Use the platform funding model.

### 6. Decide classification

Product-local, internal accelerator, reusable platform asset, productized service, archive, or defer.

## Outputs

- Completed productization checklist.
- Asset classification.
- Assumptions to remove.
- Owner/funding decision.
- Adoption plan.

## Completion criteria

- Generic capability is named.
- Local assumptions are handled.
- Support/funding explicit.
- Adoption path exists or asset is not promoted.

## No-go signals

- Asset is still client/product-shaped.
- Support is unfunded.
- Second consumer is speculative.
- Examples require real internal details.

## Public-safe reminder

Keep entries generalized and synthetic. Do not record real service names, repo paths, commits, schemas, queue/event/table names, screenshots, logs, vendors, exact timelines, payment/security/compliance details, or identifiable client/project facts.

## Related files

- [`../templates/reusable-asset-productization-checklist.md`](../templates/reusable-asset-productization-checklist.md)
- [`../diagrams/reusable-asset-productization-funnel.md`](../diagrams/reusable-asset-productization-funnel.md)
