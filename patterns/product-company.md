# Product company: a new direction without putting the existing product on hold

[Back to the Playbook](../README.md) · [Core](../core.md) · [Research work](../research-work.md)

This pattern applies Core to a company that already has users, a working product, and commitments. Data and experience provide a starting point. At the same time, architecture, operations, customer agreements, and compliance requirements constrain the available options. A new direction has to be tested alongside ongoing work.

Unlike [a new idea in a startup](startup.md), here you can start with observed product use. But the success of an existing solution does not establish demand in a new region, the suitability of another provider, or the value of a new capability.

## Start with the next decision

“Launch a new direction” is too broad for a single check. Choose an action that will lead to material costs or commitments: inviting a group of users to a pilot, choosing a provider, starting a migration, or allocating a team. Name the decision owner, the deadline, and the first scenario.

Depending on the direction, the question might be:

- **New product line:** should we test a specific scenario with the current segment or first look for a different audience?
- **New market, region, or channel:** does the existing scenario fit the local process, buyer, and sales approach?
- **New integration or provider:** are the required operations supported under the available conditions, and is the cost of switching justified?
- **AI capability:** is the result useful on real tasks, and are the errors and the cost of human review acceptable?
- **Platform capability:** which product will use it first, and does that product's result justify developing, deploying, and maintaining the shared mechanism?
- **Material change across several products:** can the first transition preserve the necessary compatibility and current commitments?

These are examples of decisions, not a mandatory research list. Connect the chosen action to whose situation should improve, the expected customer and business benefit, a useful signal, and conditions that must not deteriorate. If the path is unclear, a bounded learning goal can guide the next check. For a clear, reversible change, a short review of existing data may be enough.

## Use existing data within its limits

Start with telemetry for the relevant scenario: who uses it, where they stop, and what errors occur. Compare it with support requests, reasons for rejection, customer conversations, and examples of manual work. Check that the data is current, events are complete, and the segment's composition is understood: an aggregate metric may hide different processes.

This information helps select a question. It does not automatically explain the reasons for behavior or establish that users will accept a proposed change. A request from one large customer does not establish demand across the market either.

Available analysts and process owners help make sense of the current product and how the company works. But experience with product telemetry does not automatically mean an ability to research a new market. For a new direction, check that the necessary skills are available and involve the specialist in the relevant check, taking their current commitments into account.

Fresh evidence is needed when the audience, process, or cost of an error changes. For a new region, examine a specific case with a local user and the people involved in the process. For a new workflow step, show it to the people who will have to use it. For AI, test representative tasks and material errors; a good demo using selected examples does not replace that check.

If the question concerns a technical capability, use applicable documentation, code, and a check of behavior in a suitable environment. A user interview does not establish that an API works, and a successful request does not establish product value. Keep the limits of the finding with the result, following the [Evidence](../core.md#evidence) rule.

## Make constraints part of the decision

Trace one end-to-end scenario through the affected systems and teams. Find out what data and permissions are needed, where existing contracts remain in place, who handles failures, and who will maintain the result. Include deployment, migration, and ongoing ownership in the platform or integration estimate.

Designing a shared capability around several known scenarios is **co-design**. It can improve the design, but does not by itself show how an already chosen solution transfers to another context. For a reuse question, identify the reference version and examine the other scenario's requirements separately enough to reveal differences. Show the adaptation, integration, adoption, and ownership costs. A version reference or snapshot can be enough; no permanent freeze is required. Synthetic contrast scenarios can inform this design question, but do not establish a real deployment or market acceptance.

Separately, compare the new step with current commitments: service availability, promised capabilities and deadlines, support workload, conditions for handling data, and required approvals. If commitments need to change, the initiative owner agrees on those changes with the owners of the affected products. A pilot plan does not authorize silently postponing their delivery or degrading service.

Distinguish an unknown fact from a decision that has not been made. Migration feasibility requires a technical check; postponing a commitment requires a decision by the authorized owner. A discovered contradiction must change the dependent plan before it reaches implementation. Safe, independent work can continue while the contradiction is being resolved.

## Bound the pilot and set a review point in advance

Choose a boundary that lets you test the next question: one scenario, segment, partner, or product. Before starting, agree on acceptable costs and timing, an observable result, conditions for stopping, and the people responsible for operations. Specify how to disable or restore the solution; if the action is irreversible, account for that when choosing the scale and depth of the check.

For example, an AI assistant could prepare drafts for a limited group of operators. Shipping it is an output and draft usage is a local signal; the intended benefit could be less operator effort and faster service for customers. Check total handling and correction time, and track consequential errors: usage alone does not establish reduced effort, and less effort alone does not prove a business benefit. Expansion depends on these results and data-handling conditions. Using a model does not justify automatically acting on an operator's behalf.

A small scale does not remove mandatory security and compliance requirements. Pilot success applies to the tested conditions; a broader launch may require additional evidence.

At the review point, the decision owner chooses whether to expand, narrow, repeat a justified check, wait, or stop. Confirming the original plan is also valid. Carry the analysis, conditions, and open questions into the work plan; launch authority follows [Decision / stop](../core.md#decision-stop), not an exhausted budget or absence of objections.

When closing the pilot question, retain its material assumptions and agree who will observe the delivered result and when to revisit it. For the assistant, that means checking whether continued use actually relates to operator effort, customer service, and consequential errors. Use existing telemetry and operating reviews where they fit; a convenient local signal is not a substitute for the intended effect.

An ongoing product team also maintains regular contact with customers to learn about their needs and unexpected opportunities, beyond monitoring this feature or waiting for a predefined trigger. Torres's model calls for at least weekly customer touchpoints by the team building the product; that cadence is not prescribed here for every technical check or finite engagement (see the [source and adaptation note](../README.md#foundations-and-development)).

## When initiatives compete for the same specialists

Several initiatives may need the same domain expert, architect, data specialist, or compliance specialist at the same time. Make this shared demand visible before promising dates. Those responsible for priorities must choose the order with current commitments in mind; the expert is not obliged to compensate for the conflict by constantly switching tasks.

If a persistent queue develops, you can use [the conditional DBR adaptation for flow control](outsourcing-presales.md#flow-control): keep a small queue of questions with the necessary inputs and release work as the shared specialist becomes available. A single initiative without this competition does not need a separate mechanism.

Separately from learning whether a product decision produced value, examine how discovery worked: which assumption was missed, which check changed the choice, and what delayed understanding. Refine a playbook rule when an observed failure justifies the change; a minor question need not trigger a separate retrospective or a new mandatory stage.

---

[Back to the Playbook](../README.md) · [Core](../core.md)
