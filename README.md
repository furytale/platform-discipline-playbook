# Discovery Playbook

**What to find out, what to rely on, and when to act.**

Development is already scheduled, but the team still does not know whether an integration supports the operation it needs. Or the reverse: research continues even though there are enough answers for the next decision.

This playbook proposes working through such situations around a specific decision, rather than a mandatory set of meetings and documents.

> **Discovery helps establish a sufficient basis for the next consequential action—or a reasoned decision not to take it.**

The outcome may be a first use case, a boundary for reuse, a pilot decision, clarified scope, or a decision to stop pursuing a direction. Documents support that choice but do not replace it. A check that confirms the original plan is also a useful result.

## The work this playbook is for

Discovery is a broad word. I use it here for the work between an important unanswered question and a decision the team can responsibly act on.

Sometimes that work is customer research. Sometimes it is a process walkthrough, a technical check, a review of existing evidence, or a conversation that exposes a decision nobody has made. The playbook does not replace those crafts. It helps decide which one is needed, what it must establish, and when there is enough basis to move—or a reason to stop.

The playbook is written for CTOs, solution architects, business analysts, product leaders, and technical founders. It is deliberately narrower than a complete guide to product research, business analysis, software architecture, or compliance. Use the relevant professional method inside the check. Use this playbook to keep the question, evidence, limits, authority, and next action connected.

**Version 0.2.** A practitioner playbook developed from firsthand work and refined through use. Its rules are contextual rather than universal; later applications may sharpen, narrow, or challenge them.

## How to use it

Start with one choice or learning goal. If current, applicable evidence already answers the question, record that basis and take it to the decision owner; do not invent another check. Otherwise:

1. [Prepare one bounded question](core.md#start-here) and decide what observations would support, challenge, or leave it open.
2. Copy the [working note](core.md#working-note) into the task or document the team already uses.
3. Use the [technical example](core.md#example) or the [process example](examples/mandatory-intake-form.md) to see the plan, observation, choice, and updated work together.
4. Open [Research work](research-work.md) when the question needs decomposition, several investigators, a revised working answer, or a checked handoff.

The same person may investigate and decide when they have the authority. These links describe work to perform, not required meetings, roles, documents, or phases. Not every task needs a large discovery effort.

## Start where the work is stuck

You do not need to read the repository in order. Start with the responsibility in front of you and bring one question that still affects an action.

| Your current responsibility | Start with | Bring this question |
|---|---|---|
| CTO or technical leader | [Decision](core.md#decision), [Sufficient depth](core.md#sufficient-depth), then the relevant context pattern | Which investment or commitment cannot yet be justified, and what basis would be enough to choose? |
| Business analyst | [Uncertainty](core.md#uncertainty), [Evidence](core.md#evidence), and [Research work](research-work.md) | Which part of the process or requirement is established, disputed, or still assumed—and what decision depends on it? |
| Solution architect | [Evidence](core.md#evidence), [Sufficient depth](core.md#sufficient-depth), then the relevant context pattern | Which technical condition could invalidate the option, change the estimate, or limit a safe rollout? |
| Founder or product leader | [Decision](core.md#decision), then the relevant [application context](#three-application-contexts) | Which problem, audience, or bounded bet is worth the next investment? |

Roles do not own parts of the Core. The table only offers an entry point. One person may carry several responsibilities, and a consequential question may need more than one kind of competence.

## Start with the Core

| Element | Main question |
|---|---|
| [Decision](core.md#decision) | What do we want to decide, and who has the authority to decide it? |
| [Uncertainty](core.md#uncertainty) | What could change that decision? |
| [Evidence](core.md#evidence) | What information actually answers our question? |
| [Sufficient depth](core.md#sufficient-depth) | What basis is enough for the next step, and where does the check stop? |
| [Decision / stop](core.md#decision-stop) | What do we do now, on what basis, and within what boundaries? |

**The Core is a reasoning discipline, not five mandatory stages.** It tests whether the work keeps five things connected: a decision, material uncertainty, suitable evidence, a sufficient basis for the next step, and an explicit action or stop.

The six functions in [Research work](research-work.md) describe what people may need to do when the answer is not already available: frame, acquire, interpret, challenge, decide and record, act and learn. They are work, not a second lifecycle. A small question may use only part of them; a difficult one may revisit several.

Set cost and effort limits before material checks. New information may change the original question. A small, reversible change may need only 20 minutes; a specific unknown in a new direction may call for a separate investigation. Each Core element explains its purpose, the failure it prevents, a minimum rule, and when it is enough. You can also use the [next-action map](core.md#core-decision-map).

## Three application contexts

The Core is shared across all three contexts. The application patterns explain differences in budget, authority, access to people, and commitments:

- [Startup](patterns/startup.md): test a new idea with a bounded bet, or embed discovery in ongoing delivery when an architect or CTO joins.
- [Product company](patterns/product-company.md): test a new direction, market, integration, AI capability, or platform capability while accounting for the existing product and commitments.
- [Outsourcing / presales](patterns/outsourcing-presales.md): connect request qualification, context handoff, effort limits, review of findings, and the transition to an estimate and statement of work (SOW).

These are ways to apply the same Core. You can read the Core and go straight to your context.

## What to add when needed

Add coordination, relevant review, and escalation only where findings, authority, or commitments would otherwise be lost. The playbook does not replace development, quality checks, or management decisions.

[Research work](research-work.md) contains the shared procedures for conducting one inquiry, coordinating related questions, and carrying findings into the next action. [AI-assisted research in discovery](ai-assisted-research.md) applies those procedures when AI helps inspect, compare, challenge, or synthesize material. Neither page is a fourth application context or a prerequisite for a clear small question.

**DBR** is described in the section on [managing a discovery queue](patterns/outsourcing-presales.md#flow-control). It is an optional way to align work release with available constrained capacity, not a research method or a sixth Core element. It fits situations where several initiatives compete for one specialist, access to an environment, or another shared limited capability.

DBR is not required for a single bounded question without a flow problem. In a startup or product company, it makes sense when the same competition for shared capacity exists.

English is the canonical language of this playbook, future contributions, and the related article.

## Foundations and development

I developed this playbook through firsthand discovery and AI-assisted research: organizing investigations, working with participants and constraints, and dealing with errors, rework, and decisions. Notes labeled **From my practice** describe real episodes with identifying details omitted. Teaching examples are explicitly marked as hypothetical.

Selected refinements draw on Teresa Torres, *Continuous Discovery Habits: Discover Products That Create Customer Value and Business Value* (Product Talk LLC, 2021): intended effects (chs. 3, 11), comparing options and testing assumptions (chs. 2, 5, 9–10), shared understanding (chs. 1–2, 13), and continued learning (chs. 1, 5, 11, 14). Torres's model includes a product trio and at least weekly customer touchpoints by the team building the product. This playbook adapts selected ideas to broader contexts; competence-based participation, no fixed quota of alternatives, and finite-engagement boundaries are the author's adaptations, not a reproduction of her full method. DBR is attributed separately and used only as optional flow control, not as a research method.

Continue to improve the playbook through use: review which assumption changed, where a decision was lost, and what helped people make it. [Learning from use](learning-from-use.md) provides a short record for a consequential application without turning every small question into a retrospective. A serious one-off failure can justify a targeted safeguard; recurring problems can reveal where a rule needs to change.

## License

Except where otherwise noted, the original text and diagrams in this repository are licensed under the [Creative Commons Attribution 4.0 International License](LICENSE).

Copyright © 2026 Anton Kazka. Third-party quotations and linked materials remain the property of their respective owners and are not relicensed by this repository.

---

Author: Anton Kazka.
