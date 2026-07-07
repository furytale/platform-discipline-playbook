# Typed Core, Metadata Edges

## Core question

Where should metadata/configuration live, and where must typed code remain in control?

## What belongs in typed code

Typed code should own service contracts, authorization boundaries, transactions, inbox/outbox, workflow runtime, idempotency, core invariants, and orchestration substrate.

## What can become metadata

Metadata/configuration can be useful for field catalogs, mapping rules, transform rules, value sets, validation profiles, activation states, source-specific translation, and other bounded semantic edges.

## Metadata edge candidate test

Use metadata only when variability is real and repeated, meaning can be named, validation and activation are explicit, rollback exists, ownership is named, and typed execution guarantees remain intact.

## Governance requirements

A metadata edge needs ownership, validation, activation, versioning, rollback, compatibility, observability, exception path, and deprecation.

## Failure modes

Metadata everywhere creates fog in the core. Hidden product logic in runtime configuration weakens testability and ownership. Configurable does not mean unowned.

## Related artifacts

- [`../templates/metadata-edge-candidate.md`](../templates/metadata-edge-candidate.md)
- [`../runbooks/metadata-edge-review.md`](../runbooks/metadata-edge-review.md)
- [`../diagrams/typed-core-metadata-edges.md`](../diagrams/typed-core-metadata-edges.md)

## What this must not imply

- This is not a universal methodology.
- This is not proof that one platform shape always wins.
- This does not replace local architecture judgment.
- This should be adapted, not adopted blindly.
