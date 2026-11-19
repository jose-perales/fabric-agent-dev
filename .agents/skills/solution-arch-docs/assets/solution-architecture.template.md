---
title: Solution architecture
description: Business-aligned Fabric components, data design, alternatives, and implementation constraints.
status: draft
---

## Outcome and scope

* Value frame and setup context: {{references}}
* First slice and consumers: {{bounded outcome and intended users}}
* Exclusions: {{what the design does not cover}}
* Requirements: {{identifiers, expected behavior, and relevant measurable targets}}
* Constraints and unknowns: {{business, source, platform, access, cost, and timing}}

## Context and flows

{{Show the system boundary, external actors, sources, and consumers. Describe or
diagram the source-to-consumer flow using the same names as the inventory below.}}

## Components

Repeat for each component.

* Name, responsibility, and Fabric item type: {{component}}
* Inputs, outputs, and dependencies: {{interfaces and ordering}}
* Requirement supported: {{business or technical need}}
* Environment and identity needs: {{non-secret bindings and access boundary}}
* Capability evidence: {{official source or observation, date, and limits}}

## Data and interface design

Repeat for each relevant dataset or interface.

* Grain, schema, keys, and relationships: {{definitions}}
* Source-to-target mapping: {{source field, transformation, target, and rule}}
* History and incremental behavior: {{checkpoints, updates, deletes, and reruns}}
* Late, duplicate, missing, or invalid data: {{expected handling}}
* Business metrics and examples: {{definitions and expected results}}
* Quality and freshness rules: {{checks and targets or unresolved decisions}}
* Compatibility and schema changes: {{assumptions and consumer impact}}

## Operational and delivery needs

* Configuration and secrets: {{binding locations and secret-store references}}
* Deployment dependencies: {{items, order, and unresolved automation limits}}
* Signals and ownership: {{failure/quality/freshness signals and accountable owner}}
* Recovery and cost constraints: {{required behavior and assumptions}}
* Setup actions: {{prerequisite, owner, and next step}}

## Design decisions

Repeat for each consequential choice; extract a separate record only if useful.

* Decision and status: {{proposed or accepted; actual owner decision if available}}
* Requirement or constraint: {{reason the decision is needed}}
* Options and trade-offs: {{viable alternatives and why rejected}}
* Selected design and consequences: {{rationale, limitations, and follow-up}}
* Supporting evidence: {{references and dates}}

## Readiness for specs

* Ready scope: {{slice with sufficient design detail}}
* Open decisions: {{question, dependent scope, owner, and next action}}
* Required validation: {{unverified capabilities and how they will be checked}}
* Review and acceptance: {{actual findings and owner acceptance, or pending}}
