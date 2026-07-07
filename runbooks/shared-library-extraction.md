# Shared Library Extraction Runbook

## Purpose

Extract shared code deliberately, without letting it become an unofficial platform with no owner, source of truth, compatibility policy, or support path.

A shared library can be a Foundation precursor. It is not a platform just because many services import it.

## Trigger

Run this when:

- several services implement the same stable execution concern;
- local divergence is causing delivery or operational risk;
- teams request shared code;
- a helper is becoming critical;
- shared code already exists but has no owner or versioning rule;
- a repeated-pattern review promotes a concern to shared-library candidate.

## Preconditions

Do not start extraction until most of these are true:

- [ ] repeated concern exists in more than one real service;
- [ ] concern is stable enough to standardize;
- [ ] concern belongs mostly to execution mechanics;
- [ ] divergence cost is medium/high;
- [ ] owner is named;
- [ ] source of truth can be defined;
- [ ] compatibility expectation is known;
- [ ] adoption path is plausible;
- [ ] support boundary can be stated;
- [ ] product semantics remain domain-owned.

If these are not true, document the pattern or keep a local helper.

## Inputs

- Repeated service-shape ledger entry.
- Candidate implementations.
- Proposed consumers.
- Known local deviations from [`../templates/exception-deviation-log.md`](../templates/exception-deviation-log.md).
- Compatibility expectations.
- Proposed owner.
- Existing tests or examples.

## Participants

| Role | Responsibility |
|---|---|
| Library owner | Owns extraction, source of truth, releases, compatibility. |
| Architect / technical lead | Confirms scope and platform boundary. |
| Consumer service representatives | Validate adoption and migration cost. |
| Delivery lead | Confirms capacity and timing. |
| Platform owner, if separate | Confirms governance fit. |

## Procedure

### 1. Define scope

Write what the library owns and does not own.

Good scope:

- configuration validation;
- logging setup;
- tracing context;
- error mapping;
- idempotency helper;
- message envelope;
- transaction wrapper;
- health/readiness baseline.

Dangerous scope:

- product workflow meaning;
- domain invariants;
- customer-specific policy;
- broad application framework from one implementation;
- future-looking modules without adoption.

### 2. Create register entry

Fill [`../templates/shared-library-register.md`](../templates/shared-library-register.md). If the extraction is still not ready, keep it in [`../templates/platform-candidate-backlog.md`](../templates/platform-candidate-backlog.md).

Minimum required fields:

- owner;
- source of truth;
- concern solved;
- supported consumers;
- versioning model;
- compatibility policy;
- adoption path;
- support owner;
- deprecation approach.

### 3. Choose source-of-truth model

Options:

- versioned package;
- shared repository;
- workspace package;
- template-owned module;
- temporary shared helper;
- product-owned local adaptation;
- not extracted yet.

If the source of truth cannot be named, do not extract.

### 4. Define compatibility policy

Answer:

- what can break?
- what must not break?
- how are breaking changes announced?
- how are services upgraded?
- who owns migration work?
- how are old versions deprecated?
- what tests protect compatibility?

### 5. Prepare minimal implementation

Keep the library smaller than the repeated problem.

Remove:

- unused modules;
- speculative helpers;
- service-specific behavior;
- product semantics;
- optional dependencies most consumers do not need.

A shared library should reduce divergence, not collect architectural souvenirs.

### 6. Validate with consumers

For each initial consumer:

- confirm adoption path;
- record version or import mechanism;
- estimate migration cost;
- identify exceptions;
- confirm support expectation;
- confirm rollback or removal path.

### 7. Decide release status

Choose one:

| Status | Meaning |
|---|---|
| Experimental | Used by limited consumers; compatibility not guaranteed. |
| Supported | Owner, source of truth, adoption path, and compatibility policy exist. |
| Governed platform asset | Adoption, support, exceptions, conformance, deprecation, and team model exist. |
| Deprecated | Use is being removed or replaced. |

Do not skip from experimental to platform asset because the code looks useful.

### 8. Record exceptions

If consumers need local differences, record them in [`../templates/exception-deviation-log.md`](../templates/exception-deviation-log.md). Exceptions are feedback.

## Completion criteria

Extraction is complete when:

- register entry exists;
- owner is named;
- source of truth is clear;
- scope and non-scope are documented;
- compatibility policy exists;
- initial consumers are known;
- adoption path exists;
- support model exists;
- tests or validation path exist;
- deprecation approach is documented;
- monthly signal review tracks the asset.

## No-go signals

Stop or shrink extraction when:

- no owner exists;
- only one implementation exists;
- consumers disagree on semantics;
- the concern is domain-owned product meaning;
- adoption requires too much conceptual change;
- the library would include unused future-looking modules;
- compatibility cannot be protected;
- consumers need local adaptation more than shared code.

## Outputs

- Updated shared library register.
- Migration/adoption notes for consumers.
- Compatibility policy.
- Support and exception/deviation path.
- Monthly signal review item.
- Optional ADR if the asset is critical.

## Reminder

The first shared library is useful because the pain is real. It becomes dangerous when nobody knows which copy is canon.
