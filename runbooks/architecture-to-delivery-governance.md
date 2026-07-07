# Architecture To Delivery Governance Runbook

## Purpose

Translate architecture decisions into delivery gates, acceptance criteria, owners, exceptions, and conformance evidence.

## Trigger

Run this when:

- an architecture rule is introduced;
- Foundation scope changes;
- drift reveals an unenforced rule;
- delivery teams do not know how a decision affects acceptance criteria.

## Inputs

- Architecture decision.
- Relevant playbook section.
- Current delivery process.
- Owner/consumer teams.
- Known exceptions.

## Participants

| Role | Responsibility |
|---|---|
| Architect / technical lead | checks boundary and decision quality |
| Owner | accepts future cost |
| Consumer representative | validates adoption and usability |
| Delivery lead | confirms capacity and delivery impact |

## Procedure

### 1. Identify architecture rule

Write the rule in one plain sentence. If it cannot be written plainly, do not turn it into a delivery gate yet.

### 2. Convert rule into delivery check

Define where it is checked, who checks it, what evidence is enough, and what happens if it fails.

### 3. Add review gate

Choose service candidate review, design review, PR checklist, conformance test, release readiness, or monthly signal review.

### 4. Define acceptance criteria

Make criteria observable. `No direct publish in transactional path` beats `follow platform`.

### 5. Define exception path

Name approver, justification, expiry, log location, and baseline feedback path.

## Outputs

- Updated governance map.
- Delivery gate.
- Acceptance criteria.
- Owner and exception path.
- Evidence requirement.

## Completion criteria

- Rule is plain.
- Control is defined.
- Acceptance criteria are observable.
- Owner and exception path exist.

## No-go signals

- Nobody can check the rule.
- Rule is product-specific but presented platform-wide.
- Control creates ceremony without decision quality.

## Public-safe reminder

Keep entries generalized and synthetic. Do not record real service names, repo paths, commits, schemas, queue/event/table names, screenshots, logs, vendors, exact timelines, payment/security/compliance details, or identifiable client/project facts.

## Related files

- [`../templates/architecture-to-delivery-governance-map.md`](../templates/architecture-to-delivery-governance-map.md)
