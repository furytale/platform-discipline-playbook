# Platform Import ADR

Use this ADR when platform code enters a product through a versioned dependency, vendored package, copied module, squashed import, generated output, fork, or local adaptation.

Purpose: make import mechanics visible as ownership mechanics.

Do not include real repository names, file paths, package names, commit hashes, internal links, vendors, schemas, queue names, or client-specific details in public copies.

---

# ADR: Platform Code Import Ownership

## Status

Proposed / accepted / superseded / deprecated

## Context

Describe the situation in generalized terms.

- What platform capability is entering the product?
- Why is the product consuming or importing it now?
- What delivery pressure or adoption constraint exists?
- What would happen if the product did not import it?
- What would happen if the platform remained fully external?

Context summary:

> 

## Import mechanism

Choose the mechanism.

- [ ] Versioned dependency
- [ ] Vendored package
- [ ] Copied module
- [ ] Squashed import
- [ ] Temporary fork
- [ ] Generator output
- [ ] Manual adaptation from reference implementation
- [ ] Product-integrated core
- [ ] Other: 

Mechanism notes:

> 

## Decision

Decision statement:

> We will use `[mechanism]` for `[generalized platform capability]` because `[reason]`. Ownership after import will be `[ownership model]`.

## Ownership model

Choose the primary model.

- [ ] Remains platform-owned through versioned boundary
- [ ] Becomes product-owned local adaptation
- [ ] Temporary fork with sync-back policy
- [ ] Product-integrated core with explicit governance
- [ ] Shared ownership with named platform and product responsibilities
- [ ] Not decided; import blocked until ownership is clear

## Ownership split

| Area | Platform owner | Product owner | Shared / notes |
|---|---|---|---|
| Source code changes |  |  |  |
| Compatibility |  |  |  |
| Support |  |  |  |
| Security/runtime baseline |  |  |  |
| Product-specific adaptation |  |  |  |
| Testing |  |  |  |
| Documentation |  |  |  |
| Deprecation |  |  |  |
| Migration/upgrade |  |  |  |

## What remains platform-owned?

- 

## What becomes product-owned?

- 

## What may be changed locally?

- 

## What must not be changed locally without review?

- 

## Compatibility policy

| Question | Answer |
|---|---|
| Is compatibility with platform source required? | Yes / no / partial |
| How is compatibility checked? |  |
| What is the upgrade path? |  |
| What is the rollback path? |  |
| What is the migration window? |  |
| Who approves breaking changes? |  |

## Sync-back / contribution policy

| Question | Answer |
|---|---|
| Which changes should flow back to platform? |  |
| Which changes stay product-local? |  |
| Who reviews sync-back candidates? |  |
| How often is sync-back reviewed? |  |
| What happens if divergence becomes permanent? |  |

## Support model

| Field | Value |
|---|---|
| Primary support owner after import |  |
| Escalation path |  |
| Product team responsibilities |  |
| Platform team responsibilities |  |
| Known support gaps |  |

## Risks

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| Platform boundary dissolves silently | Low / medium / high | Low / medium / high |  |
| Product-local changes cannot flow back | Low / medium / high | Low / medium / high |  |
| Compatibility breaks later | Low / medium / high | Low / medium / high |  |
| Support responsibility unclear | Low / medium / high | Low / medium / high |  |
| Product assumptions leak into platform | Low / medium / high | Low / medium / high |  |
| Imported code becomes unowned | Low / medium / high | Low / medium / high |  |

## Alternatives considered

| Option | Why not chosen |
|---|---|
| Keep platform external through versioned dependency |  |
| Copy only minimal helper |  |
| Build local implementation |  |
| Wait and clarify platform boundary |  |
| Create product-integrated core deliberately |  |

## Review trigger

Revisit this ADR when:

- [ ] product-local changes accumulate;
- [ ] platform source changes incompatibly;
- [ ] more products need the same imported capability;
- [ ] support requests increase;
- [ ] ownership changes;
- [ ] the temporary fork becomes permanent;
- [ ] product-integrated core becomes the real platform;
- [ ] the asset should be deprecated.

## Consequences

### Positive

- 

### Negative

- 

### Open questions

- 

## Reminder

How code enters a product decides who owns the future cost of changing it.
