# Team Topology Review Runbook

## Purpose

Clarify the team model for platform reuse: platform owner, stream-aligned consumers, enabling capacity, support path, contribution model, and interaction mode.

## Trigger

Run this when:

- a product team adopts a platform asset;
- one team is expected to build product features and govern platform;
- imported platform code changes ownership;
- support/escalation/contribution paths are unclear.

## Inputs

- Platform capability.
- Consumer teams/archetypes.
- Ownership split.
- Adoption plan.
- Funding model.
- Support process.

## Participants

| Role | Responsibility |
|---|---|
| Architect / technical lead | checks boundary and decision quality |
| Owner | accepts future cost |
| Consumer representative | validates adoption and usability |
| Delivery lead | confirms capacity and delivery impact |

## Procedure

### 1. Identify platform owner/team

Name who owns roadmap, compatibility, support, and deprecation. If answer is one overloaded architect, topology is not ready.

### 2. Identify stream-aligned consumers

Name consuming product teams generically and check product/domain load and runtime responsibility.

### 3. Identify enabling role

Decide whether adoption requires learning, pairing, examples, guided review, and funded enablement.

### 4. Define team API

Complete the team API template.

### 5. Choose interaction mode

Collaboration, facilitating, X-as-a-Service, or mixed by adoption stage.

### 6. Define support and escalation

Support channel, escalation path, runtime ownership, exception process, contribution path, review cadence.

## Outputs

- Team API.
- Ownership split.
- Interaction mode.
- Support/escalation path.
- Enabling capacity decision.

## Completion criteria

- Platform owner is named.
- Consumers are named generically.
- Interaction mode is explicit.
- Runtime gaps are visible.

## No-go signals

- Adoption requires learning but no enabling role exists.
- Support path is private messages to one person.
- Consumer teams own global platform coherence silently.

## Public-safe reminder

Keep entries generalized and synthetic. Do not record real service names, repo paths, commits, schemas, queue/event/table names, screenshots, logs, vendors, exact timelines, payment/security/compliance details, or identifiable client/project facts.

## Related files

- [`../templates/team-api.md`](../templates/team-api.md)
- [`../templates/platform-ownership-split.md`](../templates/platform-ownership-split.md)
