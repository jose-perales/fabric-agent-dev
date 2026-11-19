---
title: Fabric implementation record
description: Changed artifacts, acceptance results, and delivery handoff for a specified slice.
status: draft
---

## Scope and change context

* Spec and architecture: {{references}}
* Repository revision and local changes: {{identify what was actually tested}}
* Implemented scope: {{requirements and changed artifacts}}
* Exclusions and deviations: {{unimplemented scope and agreed spec changes}}

## Artifact handoff

Repeat for each relevant artifact.

* Artifact and item type: {{repository location and Fabric type}}
* Requirement: {{spec requirement identifier}}
* Dependencies and deployment order: {{upstream artifacts and constraints}}
* Configuration: {{non-secret bindings and external credential references}}
* Authoring capability: {{tool or supported format actually used}}

## Acceptance results

Repeat for every acceptance criterion, including checks not performed.

* Criterion: {{AC identifier and expected result}}
* Method and input: {{actual command/procedure and independent fixture}}
* Execution context: {{local, exact Fabric target, or human acceptance}}
* Status: {{passed, failed, blocked, or not run}}
* Actual result and reference: {{observation, date, and log/output reference}}
* Limitation or next action: {{gap, owner, and how to rerun}}

## Live actions

* Authorization and target: {{scope and non-secret identifiers, or none}}
* Mutations and observed outcome: {{changes actually performed, or none}}
* Partial or ambiguous outcomes: {{reconciliation status and required next step}}

## Delivery readiness

* Authoring and local validation: {{status and required remaining work}}
* Deployment and runtime verification: {{separate statuses}}
* Required failed or blocked checks: {{criteria preventing full verification}}
* CI/CD entry points: {{validation commands and runtime prerequisites}}
* Owner acceptance: {{pending or actual decision with reference}}
