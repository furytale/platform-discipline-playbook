# Monthly Platform Signal Review Runbook

## Purpose

Make platform discipline routine instead of dependent on one architect's memory.

This review looks for repeated service pain, local deviations, shared asset drift, import ownership gaps, and candidates that should be promoted, shrunk, retired, or governed harder.

The cadence does not have to be monthly. Use the rhythm that matches delivery. The important thing is that platform signals do not disappear between delivery cycles.

## Trigger

Run this:

- monthly;
- after several new service/module reviews;
- before a major platform release;
- after a delivery phase with many local deviations;
- before publishing or promoting new platform guidance;
- when shared code starts generating support requests.

## Inputs

- Service candidate register.
- Repeated service-shape ledger.
- Shared library register.
- Platform candidate backlog.
- Skeleton readiness checklists.
- Generator candidate register.
- Platform import ADRs.
- Exception/deviation log entries.
- Support requests.
- Consumer feedback.
- New or changed service archetypes.
- Deprecation candidates.

## Participants

| Role | Responsibility |
|---|---|
| Architect / technical lead | Facilitates signal review and decision classification. |
| Platform owner, if one exists | Owns platform asset decisions and roadmap impact. |
| Senior engineers | Validate implementation reality and adoption pain. |
| Engineering manager / delivery lead | Confirms capacity and scheduling. |
| Product/domain representative, if needed | Confirms product meaning and ownership boundaries. |

## Agenda

### 1. Review new service candidates

For each new candidate:

- Was the boundary decision recorded?
- Was the service archetype selected?
- Were repeated concerns added to the ledger?
- Did any candidate bypass review?
- Are any decisions due for revisit?

### 2. Review repeated service-shape ledger

Ask:

- Which concerns repeated since the last review?
- Which concerns now appear in several services?
- Which concerns have high divergence risk?
- Which are execution mechanics?
- Which are product meaning and should stay domain-owned?
- Which candidates should move to shared helper, library, skeleton, generator, governance, or wait?

### 3. Review shared libraries

Ask:

- Which shared libraries have new consumers?
- Which modules are copied but unused?
- Are consumers patching locally?
- Is source of truth still clear?
- Are compatibility and support expectations still true?
- Should any library be promoted, split, deprecated, or retired?

### 4. Review skeleton/template baseline

Ask:

- Did new services use the skeleton?
- What did they change immediately?
- Are deviations justified?
- Does the skeleton include dead weight?
- Are generated/template outputs tested?
- Does any baseline default need removal?

### 5. Review imports and local adaptations

Ask:

- Did platform code enter a product?
- Was the import mechanism recorded?
- Who owns the code now?
- Are local changes accumulating?
- Should changes flow back?
- Has a temporary fork become permanent?
- Is product-integrated core acting like a platform asset?

### 6. Review platform candidate backlog

Ask:

- Which candidates gained evidence?
- Which candidates lost relevance?
- Which candidates still have no owner?
- Which candidates should be promoted, shrunk, retired, or left waiting?
- Which candidates are pretending to be assets before governance exists?

### 7. Review exceptions and deviations

Ask:

- Which deviations expired?
- Which deviations were justified?
- Which deviations reveal a wrong baseline?
- Which deviations are drift?
- Which need platform backlog items?

### 8. Decide promotions and demotions

For each candidate, choose one:

- keep local;
- document pattern;
- create reference example;
- shared helper;
- shared library candidate;
- skeleton/template candidate;
- generator candidate;
- governed platform asset;
- product-owned local adaptation;
- retire;
- revisit.

Promotion is not success by default. Sometimes the mature decision is to shrink or kill the asset.

### 9. Update roadmap and owners

Every accepted action needs:

- owner;
- next artifact;
- review trigger;
- support impact;
- delivery capacity decision;
- public-safe summary if this will feed article material.

## Review board

Use this summary table.

| Area | Keep | Promote | Shrink | Retire | Needs owner | Notes |
|---|---|---|---|---|---|---|
| Service candidates |  |  |  |  |  |  |
| Repeated concerns |  |  |  |  |  |  |
| Shared libraries |  |  |  |  |  |  |
| Skeleton/template |  |  |  |  |  |  |
| Platform imports |  |  |  |  |  |  |
| Platform candidates |  |  |  |  |  |  |
| Exceptions |  |  |  |  |  |  |

## Completion criteria

The review is complete when:

- new candidates are classified;
- repeated concerns have decisions or revisit triggers;
- shared libraries have current owner/status;
- skeleton changes are accepted or rejected;
- import ownership gaps are assigned;
- expired exceptions are reviewed;
- platform candidates have next actions;
- unsupported assets are not presented as platform assets;
- decisions are recorded in the relevant templates.

## Signals worth tracking

| Signal | Why it matters |
|---|---|
| Same helper copied again | Candidate for shared helper or library. |
| Template edited immediately after generation | Baseline may be wrong or too large. |
| Local patch repeated across consumers | Platform asset may need update. |
| Support request repeats | Documentation or adoption path is weak. |
| Exception appears in several services | Baseline may not fit service archetype. |
| Imported code diverges | Ownership model needs review. |
| Shared library has unused modules | Scope is too broad or stale. |
| Product semantics enter platform asset | Platform promise may be overreaching. |

## Anti-patterns

### The review becomes status theatre

People report what happened, but no candidate moves.

Fix: every reviewed signal needs keep/promote/shrink/retire/revisit.

### Everything becomes platform backlog

The team treats every repeated concern as platform material.

Fix: apply the evidence and governance gates. Repetition is evidence, not permission.

### Exceptions are treated as bad behavior

Teams hide deviations because review sounds punitive.

Fix: treat exceptions as feedback. Some are justified. Some show the baseline is wrong.

### No capacity follows the decision

The team promotes assets without funding ownership, support, or migration.

Fix: promotion requires owner and capacity. Otherwise keep it as candidate.

## Outputs

- Updated service candidate register.
- Updated repeated service-shape ledger.
- Updated shared library register.
- Updated platform candidate backlog.
- Updated skeleton readiness decisions.
- Updated generator candidate register.
- Updated platform import ADRs.
- Updated exception/deviation log.
- Action list with owners.
- Candidate promotion/demotion decisions.
- Public-safe summary if needed for article or repo documentation.

## Reminder

Platform signals rarely arrive wearing a badge. They arrive as the third service copying the same setup, the fourth local patch to the shared helper, and the fifth temporary deviation nobody remembered to clean up.
