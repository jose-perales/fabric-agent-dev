---
title: Fabric slice specification
description: Bounded implementation scope, required behavior, and verifiable acceptance criteria.
status: draft
---

## Slice and references

* Slice identifier and outcome: {{name and useful business result}}
* Value frame, architecture, and setup: {{references or equivalent supplied facts}}
* In scope: {{behavior and artifacts}}
* Out of scope: {{explicit exclusions}}
* Preconditions and dependencies: {{design decisions, access, and upstream items}}

## Requirements and artifacts

Repeat for each requirement, using stable identifiers such as REQ-01.

* Requirement: {{identifier and observable behavior}}
* Artifact and Fabric item type: {{existing or proposed location and type}}
* Inputs and outputs: {{schema, grain, keys, and interfaces}}
* Rules and mappings: {{business definitions and transformations}}
* Configuration: {{non-secret parameters and target-binding requirements}}
* Dependencies and implementation order: {{prerequisite artifacts or decisions}}

## Edge cases and change safety

* Duplicates, missing values, and invalid records: {{expected behavior}}
* Late data, updates, and deletes: {{expected behavior}}
* Checkpoints, reruns, and partial failure: {{expected behavior}}
* Schema changes, migration, and recovery: {{applicable obligations}}
* Not applicable: {{concerns excluded with a reason}}

## Acceptance criteria

Repeat for each criterion, using stable identifiers such as AC-01.

* Criterion and requirement: {{identifier and linked REQ identifier}}
* Input or fixture: {{synthetic or approved example and location}}
* Expected result and threshold: {{independently known output and tolerances}}
* Test method: {{command or explicit procedure; do not invent unavailable tooling}}
* Execution context: {{local, named Fabric environment, or human acceptance}}
* Prerequisites and owner: {{access, setup, and accountable reviewer if needed}}

## Worked example

* Input and scenario: {{small deterministic case}}
* Expected result: {{business-correct result and derivation}}
* Incorrect result: {{what the check must reject}}

## Readiness review

* Recommendation: {{draft, ready, or blocked; scope and rationale}}
* Findings: {{severity, source, impact, and remedy; or no findings in stated scope}}
* Open decisions: {{question, dependent scope, owner, and next action}}
* Required owner acceptance: {{pending or actual decision, date, and reference}}
* Revision impact: {{changes that invalidate affected implementation or checks}}
