# Platform Asset Deprecation Runbook

## Purpose

Deprecate a platform asset, shared package, template, generator output path, or product-integrated core surface without leaving consumers in archaeology mode.

## Trigger

Run this when:

- a platform asset is replaced;
- a shared package/template is no longer supported;
- compatibility cost exceeds value;
- an imported asset should stop being synced or supported.

## Inputs

- Asset name, generalized.
- Known consumers/archetypes.
- Current owner.
- Replacement path.
- Compatibility expectations.
- Support obligations.

## Participants

| Role | Responsibility |
|---|---|
| Architect / technical lead | checks boundary and decision quality |
| Owner | accepts future cost |
| Consumer representative | validates adoption and usability |
| Delivery lead | confirms capacity and delivery impact |

## Procedure

### 1. Name deprecation reason

Replaced by better path, compatibility cost too high, no owner, product assumptions too specific, consumers no longer need it, or platform strategy narrowed.

### 2. Identify consumers

Use generalized consumer categories. Do not expose service names.

### 3. Define replacement or exit path

Migrate to new asset, keep local/product-owned, archive and stop new adoption, replace with template/generator path, remove after compatibility window, or explicit stop.

### 4. Define compatibility window

Start, end/review trigger, support level, breaking-change rule, consumer notification.

### 5. Define migration plan

List generalized consumers, current use, target path, owner, risk, and status.

### 6. Close deprecation

Close only when consumers migrated, accepted ownership, or explicitly remain unsupported.

## Outputs

- Deprecation decision.
- Consumer list.
- Replacement path.
- Compatibility window.
- Migration plan.
- Support transition.

## Completion criteria

- No new adoption uses old path.
- Consumers know support status.
- Migration/local ownership recorded.
- Docs no longer advertise old path.

## No-go signals

- Consumers still depend with no path.
- Support expectations remain implicit.
- Deprecation avoids fixing governance.

## Public-safe reminder

Keep entries generalized and synthetic. Do not record real service names, repo paths, commits, schemas, queue/event/table names, screenshots, logs, vendors, exact timelines, payment/security/compliance details, or identifiable client/project facts.

## Related files

- [`../templates/platform-ownership-split.md`](../templates/platform-ownership-split.md)
- [`../templates/platform-import-adr.md`](../templates/platform-import-adr.md)
