# Execution-Core Foundation

## Core question

When can a Foundation be introduced deliberately and early, even while product semantics are still unstable?

## The uncertainty split

Product meaning can be unstable while execution mechanics are stable. That split is the whole reason early execution-platform work can be rational without becoming speculative platform-first design.

## What the execution core may own

Transactions, inbox/outbox, workflow runtime, idempotency, durable event delivery, use case execution, observability hooks, and the application/infrastructure boundary are strong candidates when they repeat and can be governed.

## What the Foundation must not own

Do not let the Foundation absorb business vocabulary, domain invariants, customer-specific policy, product-specific workflow meaning, semantic field meaning, or one-off integration behavior.

## When early Foundation is rational

Use it when operational complexity is real, local divergence is risky, execution concerns are stable enough to name, product semantics can remain outside the Foundation, and ownership/support/conformance exist.

## When it is too early

Do not build or expand Foundation when the concern has one product-specific implementation, no owner, no support path, no conformance check, or when the organization wants a framework without the operating model around it.

## Governance before drift

A platform without governance is a suggestion under delivery pressure. Scope map, capability register, conformance review, exception handling, support model, and drift review are part of the architecture.

## Related artifacts

- [`../templates/execution-core-scope-map.md`](../templates/execution-core-scope-map.md)
- [`../templates/foundation-capability-register.md`](../templates/foundation-capability-register.md)
- [`../templates/platform-drift-assessment.md`](../templates/platform-drift-assessment.md)
- [`../runbooks/foundation-scope-review.md`](../runbooks/foundation-scope-review.md)
- [`../runbooks/platform-drift-review.md`](../runbooks/platform-drift-review.md)
- [`../diagrams/execution-core-boundary.md`](../diagrams/execution-core-boundary.md)

## What this must not imply

- This is not a universal methodology.
- This is not proof that one platform shape always wins.
- This does not replace local architecture judgment.
- This should be adapted, not adopted blindly.
