# Example — should email intake become a mandatory form?

[Back to the Playbook](../README.md) · [Core](../core.md) · [Working note](../core.md#working-note)

> **Independent hypothetical exercise.** The organization, records, participants, observations, and choice below are invented to demonstrate the method. They do not describe a client engagement or a measured result from the playbook.

A service team receives customer requests by email. Some arrive without information the team needs, and operators spend time asking follow-up questions. The operations manager proposes replacing email with a form that requires every field before a request can be submitted.

The next decision is not whether forms are generally better than email. It is whether a fully mandatory form is the right next change for this intake process.

## Before the check

- **Choice:** introduce the proposed mandatory form, try a narrower change, or keep the current intake while another cause is investigated. The operations manager can choose the process change within the current budget.
- **Intended benefit:** reduce avoidable clarification without delaying the start of valid work.
- **What must not get worse:** urgent requests must still enter the queue, and requesters must not be pushed into invented placeholder values.
- **Material unknown:** are required details omitted even when requesters know them, or are they often unavailable at the time of the first request? A mandatory field can help with the first problem and worsen the second.
- **Check:** the BA reviews the 30 most recent requests and their follow-up messages, then walks through one complete and one incomplete request with four people who submit this kind of work. The sample and participant count belong to this fictional exercise; they are not a prescribed minimum.
- **Limit:** one working day for review, walkthroughs, and a short result. Form design, software implementation, organization-wide rollout, and a savings estimate are outside this question.

Before reviewing the records, the team writes down how different observations would affect the choice:

| Observation | What it would mean for this choice | Next action |
|---|---|---|
| Most missing values were known but simply omitted | The proposed form may address the main source of clarification. | Prepare a bounded form trial and define the guardrails. |
| Most missing values did not yet exist or depended on later work | Requiring every field would not remove the underlying gap. | Reject or narrow the mandatory-field proposal. |
| The cases show both problems | One intake rule is unlikely to fit every request. | Compare a minimal first step with a later completion step. |
| Records and walkthroughs cannot reveal why the information was missing | The check does not answer the question. | Keep the choice open and change the method. |

## What was observed

In the fictional record review:

- 11 of 30 requests needed at least one clarification;
- in 7 of those 11, the missing information was not yet available when the request was submitted;
- in 3, the requester and operator understood the requested category differently;
- in 1, information already known to the requester had simply been omitted.

During the four walkthroughs, every participant could provide the few details needed to route a request. Three could not provide at least one field from the proposed full form at the first contact. Two said they would enter a placeholder to get past a mandatory field.

The records establish what happened in these 30 cases. The walkthroughs show how four participants understood the proposed fields. They do not establish a population-wide rate, the behavior of every customer, or the effect of a form that has not yet been tried.

## Interpretation and challenge

The evidence does not support the assumption behind the original proposal: that most missing information was already known and simply omitted. In the reviewed cases, unavailable information and ambiguous categories mattered more than omission of known details.

That finding weakens the fully mandatory form, but it does not prove that every form would fail. A smaller first step could still improve routing while allowing details to remain pending.

Before presenting the result, the BA checks two possible overreaches:

1. “Customers cannot complete forms” is too broad. The check only concerned the proposed fields and four walkthroughs.
2. “The current process works” is also unsupported. Eleven requests still required clarification; the result changes the candidate response, not the existence of the problem.

## Recommendation and choice

The BA recommends against requiring every proposed field at first contact. Instead, the team can compare the current email path with a two-step intake for one service queue:

1. require only the information needed to route and acknowledge the request;
2. mark unavailable details as pending and make their owner visible;
3. ask for the remaining information before the work reaches the point that depends on it.

The operations manager accepts that bounded trial. The decision does not authorize an organization-wide rollout or claim a reduction in effort.

## Changes made after the choice

- The task is changed from “replace email with a mandatory form” to “trial a two-step intake in one queue.”
- The draft form removes fields that cannot always be known at first contact and adds an explicit pending state.
- The current email route remains available for urgent requests during the trial.
- The BA records clarification cycles, time to first acknowledgment, placeholder values, and requests that fail to enter the queue.
- The operations manager reviews the result after two weeks or sooner if an urgent request is delayed.

The original proposal was not rejected because “users dislike forms.” It was narrowed because the observed cause did not match the mechanism of the proposed solution. The next check concerns the two-step intake under its stated conditions.
