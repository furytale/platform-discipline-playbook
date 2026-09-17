# Startup: test the next bet and keep work moving

[Back to the Playbook](../README.md) · [Core](../core.md) · [Research work](../research-work.md)

In a startup, the next decision may concern either a first user scenario or a change to a product already in use. In both cases, [Core](../core.md) helps identify which unknown is worth checking before the next investment. The scale of the check depends on the consequences of an error and whether the action can be reversed.

## A. A new idea or direction

### Choose the next check

If the problem is not yet clear, start by choosing an audience and a situation the team can investigate. “We are building a service for small businesses” is too broad. “We are checking whether small service teams have a recurring problem handling requests and are willing to try a different approach” defines the work more clearly.

The next decision here is whether to invite participants to a pilot, clarify the problem, test another scenario, or hold off on development. Name the person authorized to allocate resources to this work. A complete product architecture is usually not needed for this decision yet.

### Gather evidence from the audience

Market reports, web research, and competitor analysis help reveal context, alternatives, and possible segments. They do not establish that particular people need the proposed product or will use it.

A founder does not have to set up a research department in advance. Finding a first use case requires audience and market research skills; if someone on the current team has them, a separate role is unnecessary. If those skills are missing, a product specialist with the relevant skills can join a specific check, with time allowed to interpret its results, following the guidance on choosing competencies in [Evidence](../core.md#evidence).

Talk to people who actually encounter the suspected problem. A research question such as “Where does handling requests create avoidable work?” can lead to an interview prompt: “Walk me through the last request you had to handle twice.” Examine what happened, how they handled it, what it cost them, and who chooses and pays for a solution. Their account provides evidence of that experience; distinguish their explanation from what the case establishes. An interview alone does not test behavior in actual use.

Distinguish polite interest from action: someone supplied an example, made time, tried a new approach, or returned to it. Even this behavior in a small selected group does not establish market size or sustained demand. Rejection and a lack of repeat use also provide grounds to reconsider the next step.

Technical feasibility and user value require different checks. A working prototype shows that a particular function has been implemented under the tested conditions. It does not establish that the function is worth changing an established process for. Audience interest, in turn, does not establish data availability or the feasibility of the required integration.

### Bound the bet and set a review point

Before a pilot, define its participants, one scenario, time and spending limits, permitted manual work, and an observable result. Agree on the outcomes that would lead you to expand the work, change the proposal, or stop. Mandatory conditions for safe action still apply to a small pilot.

In the request-handling example, consider whether clarifying responsibility or adding a narrow automation could reduce repeated work. Both may depend on receiving complete information. Check that shared assumption on recent requests before building either solution. If a gap remains, choose an appropriate next check: observation of a prototype, manual provision of the service, or a bounded pilot. There is no requirement to build parallel MVPs; use the [assumption-testing boundaries in Core](../core.md#evidence).

If the idea depends on temporary interest in a technology or market, compare delivery time with the conditions underpinning the bet. The observation that “there is interest now” may be outdated by the time the product ships. Revisit that assumption before an expensive expansion; sometimes a shorter pilot can provide a useful answer sooner.

Set a review date or trigger and name the decision owner. At the effort limit, choose whether to narrow the step, justify another bounded check, wait, or hold off on building under [Sufficient depth](../core.md#sufficient-depth). Remaining questions do not require more research when the next small bet already has enough applicable evidence.

## B. An architect or CTO joins a running startup

### Start with one result

Do not demand a lengthy period of studying the company by default. With the business and the team, agree on the next result, deadline, boundaries, and the person who will accept it. For a clear, reversible task, a short discussion and a routine check of the change may be enough.

Take one real end-to-end scenario: a user action, data processing, an external dependency, and an observable result. With the person doing the work, examine a successful case and a material exception. Then trace that path through the code and system behavior with an engineer. The presence of a component or a single passing test does not yet establish that the whole chain works.

### Check what could invalidate an expensive decision

Along the chosen path, identify what works, what is assumed, and what is still missing. Prioritize checks of conditions that could change what you implement next: availability of the required operation, permissions, data quality, error handling, and the ability to retry safely. A technical probe answers a technical question; the value of the result needs to be checked with the user or process owner.

Before expanding a shared platform mechanism, identify its first consumer, the required scope, and who will maintain the solution. Tie further study of the system to upcoming tasks.

### Build checks into delivery

Show the business how the check relates to the result: “Before implementation, we will check whether the required operation is available. The answer will determine scope and timing.” Account for this work within the team's available capacity.

If an external condition blocks part of the solution, name the person responsible for clarifying it and when to revisit the question. Continue safe, independent work: tests, local changes, and preparation of parts that remain useful under either answer. Do not carry a known contradiction into dependent code or a promised deadline.

Leave a brief record in the current task: confirmed evidence, the remaining assumption, the chosen step, boundaries, and the review trigger. If new information changes scope, the person responsible for priorities explicitly chooses the next action under [Decision / stop](../core.md#decision-stop); the architect explains options and consequences.

If several initiatives compete for the same scarce expertise, you can use [flow control with DBR](outsourcing-presales.md#flow-control). A single hypothesis without this competition does not need it.

---

[Core](../core.md) · [Product company](product-company.md) · [Outsourcing and presales](outsourcing-presales.md)
