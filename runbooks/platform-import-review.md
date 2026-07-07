# Platform Import Review Runbook

## Purpose

Decide ownership when platform code is imported, vendored, copied, generated, forked, or locally adapted inside a product.

The core question:

> Who owns the future cost of changing this code now?

## Trigger

Run this when:

- a product consumes platform code through a versioned dependency;
- platform code is vendored, copied, or squashed into a product;
- generator output becomes product code;
- a product forks or locally adapts a platform package;
- a product-integrated core starts acting like a platform asset;
- teams are unsure whether the platform or product owns support.

## Inputs

- Proposed platform capability.
- Import mechanism.
- Product need and delivery constraint.
- Current platform owner.
- Current product owner.
- Compatibility expectations.
- Expected local adaptations.
- Support expectations.
- Existing ADRs or decisions.

Use [`../templates/platform-import-adr.md`](../templates/platform-import-adr.md) during the review.

## Participants

| Role | Responsibility |
|---|---|
| Platform owner | Defines platform source, compatibility, and support boundary. |
| Product owner / product technical lead | Defines product adaptation need and local ownership. |
| Architect / technical lead | Ensures ownership model matches architecture. |
| Delivery lead | Confirms capacity and timeline pressure. |
| Consumer team representative | Validates adoption and support path. |

## Procedure

### 1. Name the import mechanism

Choose one:

- versioned dependency;
- vendored package;
- copied module;
- squashed import;
- temporary fork;
- generator output;
- manual adaptation;
- product-integrated core.

Do not hide the mechanism behind vague language like “we reuse the platform.” The mechanism decides the ownership problem.

### 2. State why import is needed

Ask:

- Why not consume through a versioned boundary?
- Why not keep this local?
- Why not wait?
- What delivery pressure exists?
- What adoption cost is being reduced?
- What support or compatibility cost is being created?

### 3. Choose ownership model

| Ownership model | Use when | Risk |
|---|---|---|
| Remains platform-owned through versioned boundary | Platform team can support releases and consumers can upgrade. | Upgrade friction. |
| Product-owned local adaptation | Product needs local control and accepts ownership. | Platform boundary dissolves. |
| Temporary fork with sync-back policy | Product needs short-term divergence, but platform source remains relevant. | Temporary becomes permanent. |
| Product-integrated core with explicit governance | Product shape is the platform surface for now. | Product assumptions leak into platform. |
| Shared ownership | Both platform and product have named responsibilities. | Ambiguity if split is not concrete. |
| Block import | Ownership is unclear. | Delivery may need another path. |

### 4. Split responsibilities

Fill the ownership table in the ADR:

- source code changes;
- compatibility;
- support;
- runtime baseline;
- product-specific adaptation;
- testing;
- documentation;
- deprecation;
- migration/upgrade.

If every row says “shared,” the decision is not finished.

### 5. Define compatibility and sync-back

Ask:

- Must the product remain compatible with platform source?
- How is compatibility checked?
- Which changes flow back?
- Which changes stay local?
- Who reviews sync-back?
- What happens if divergence becomes permanent?
- When will this be reviewed again?

### 6. Define support after import

After import, support may change.

Choose:

- platform supports it;
- product supports it;
- platform supports baseline, product supports local adaptations;
- support is time-bounded during transition;
- no support until ownership is clarified.

No support model means no platform import. It is just copied code with optimism.

### 7. Record risks and decision

Use the ADR risk table. Include at least:

- platform boundary dissolves;
- local changes cannot flow back;
- compatibility breaks later;
- support responsibility unclear;
- product assumptions leak into reusable asset;
- imported code becomes unowned.

### 8. Add review trigger

Every import needs a revisit condition:

- local changes accumulate;
- platform source changes;
- more consumers appear;
- support requests increase;
- temporary fork becomes permanent;
- product-integrated core becomes the real platform;
- asset should be deprecated.

## Completion criteria

The review is complete when:

- import mechanism is explicit;
- ownership model is selected;
- platform-owned and product-owned parts are separated;
- support model is documented;
- compatibility policy exists or is explicitly not required;
- sync-back policy exists if platform source remains relevant;
- risks are recorded;
- review trigger is defined;
- ADR is accepted or import is blocked.

## No-go signals

Block or delay import when:

- nobody owns the imported code after it enters the product;
- the platform team assumes ownership but cannot support local adaptation;
- the product team assumes platform support but changes code locally;
- compatibility is required but not testable;
- the import creates hidden commercial or delivery obligations;
- the imported asset contains product meaning from another context.

## Outputs

- Completed [`../templates/platform-import-adr.md`](../templates/platform-import-adr.md).
- Updated shared-library or platform asset register, if needed.
- Support and compatibility notes.
- Sync-back or divergence policy.
- Monthly signal review item.

## Reminder

A versioned dependency, vendored copy, squashed import, generator output, and manual copy are not the same governance model. The code may look similar. The ownership is not.
