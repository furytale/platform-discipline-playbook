# Consumer Onboarding Runbook

## Purpose

Guide a product or stream-aligned team through platform adoption without hiding adoption work inside feature delivery.

## Trigger

Run this when:

- a consumer team adopts a platform asset;
- a product imports platform code;
- a reusable package becomes mandatory;
- adoption requires enablement, examples, migration, or conformance.

## Inputs

- Platform capability.
- Team API.
- Adoption plan.
- Ownership split.
- Funding model.
- Docs/examples.
- Known exceptions.

## Participants

| Role | Responsibility |
|---|---|
| Architect / technical lead | checks boundary and decision quality |
| Owner | accepts future cost |
| Consumer representative | validates adoption and usability |
| Delivery lead | confirms capacity and delivery impact |

## Procedure

### 1. Confirm fit

Ask what product problem is being solved, whether the platform asset fits, what is unsupported, and what remains product-owned.

### 2. Choose adoption mode

Guided, paired, self-service, or not ready.

### 3. Prepare onboarding materials

Docs, reference example, migration guide, support path, contribution rules, exception process, conformance checks.

### 4. Run first adoption

Track what worked, what confused consumers, and what should become docs, examples, exception, or backlog item.

### 5. Review conformance and ownership

Check compatibility expectation, local adaptation ownership, runtime responsibility, and support after onboarding.

### 6. Close onboarding

Close only when consumer can operate within agreed support model.

## Outputs

- Adoption plan.
- Team API updates.
- Conformance status.
- Support handoff.
- Exceptions and feedback.

## Completion criteria

- Adoption mode followed.
- Supported/unsupported use clear.
- Support owner named.
- Runtime ownership clear.
- No critical knowledge remains private.

## No-go signals

- Consumer cannot use asset without private explanation.
- Local adaptation breaks compatibility without ADR.
- Support/runtime ownership unclear.

## Public-safe reminder

Keep entries generalized and synthetic. Do not record real service names, repo paths, commits, schemas, queue/event/table names, screenshots, logs, vendors, exact timelines, payment/security/compliance details, or identifiable client/project facts.

## Related files

- [`../templates/platform-adoption-plan.md`](../templates/platform-adoption-plan.md)
- [`../templates/team-api.md`](../templates/team-api.md)
