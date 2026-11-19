---
name: solution-arch-docs
description: "Create or update Fabric solution architecture, data design, and decision records. Use to turn a value frame into a justified technical design"
---

# Solution Architecture Documents

## Overview

Document the simplest supported Fabric design that satisfies the business
outcome. Connect sources, data meaning, component responsibilities, and consumer
needs before implementation details obscure the decisions. This is a first-draft
workflow.

## Prerequisites

Use the value frame, source evidence, repository setup context, and existing
designs, or equivalent supplied information. Ask for missing business definitions
that materially change the design.

Live Fabric access is not required for document work. Consequential capability
claims require current official documentation or authorized observations.
Unverified claims remain assumptions with validation actions.

## Quick Start

Invoke `/solution-arch-docs` with the value frame and known environment constraints.
Use the [architecture template](./assets/solution-architecture.template.md) for a
new design. Reuse existing document locations; otherwise default to
`docs/architecture/solution-architecture.md`.

## Workflow

1. Read the value frame, setup context, directly relevant source evidence, and
   existing architecture. Identify the first slice, agreed success measures,
   material unknowns, and constraints.
2. Translate the outcome into functional and relevant nonfunctional requirements.
   Make freshness, correctness, access, cost, recovery, and ownership expectations
   explicit without inventing numerical targets.
3. Compare viable designs against those requirements. Do not presume medallion
   layers, Spark, a warehouse, real-time processing, or a particular workspace
   topology. Record why the selected design is simpler or better suited.
4. Define boundaries, sources, ingestion, storage, transformation, orchestration,
   serving, and consumer interfaces only where needed. Show context and
   source-to-consumer flows with consistent component names.
5. Define grain, keys, relationships, history, metric semantics, source-to-target
   mappings, quality rules, and applicable incremental, delete, late-arrival,
   deduplication, and schema-change behavior. Mark irrelevant concerns as such
   with a reason; do not add components to satisfy a template.
6. Describe identities, access boundaries, environment bindings, deployment
   dependencies, operational signals, and recovery needs at design level.
   Feed concrete missing prerequisites back into repository setup.
7. Validate consequential workload and automation assumptions using current
   official sources and available workload expertise. Cite the source and date.
   Propose separately authorized experiments when documentation is insufficient;
   do not provision resources as part of writing the design.
8. Review requirements, views, mappings, and decisions for consistency. Identify
   the scope ready for specification and the specific decisions blocking the rest.

## Output and completion

Produce the architecture, needed data/interface detail, component inventory, and
short decision records. Keep minor decisions inline; split documents only when
their size or ownership warrants it.

Before handing off to `build-fabric-specs`, check that:

* Each component supports an outcome or constraint.
* The design connects identified sources to the business-facing output.
* Grain, metric meaning, and consequential data behavior are unambiguous.
* Alternatives and trade-offs explain the significant choices.
* Platform claims have support or explicit validation actions.
* Unresolved decisions block only the dependent scope and have owners.

Do not report stakeholder approval unless it was actually given. Do not write
implementation code or choose unsupported features to make the design appear
complete.

## Troubleshooting

* If sources or platform behavior are uncertain, distinguish the proposed design
  from the validated design and identify the required investigation.
* If documents disagree, resolve the material conflict before declaring the
  affected slice ready for specs.
* For a small change, update affected decisions and views rather than recreating
  the entire architecture package.

## Platform reference

Use the [Fabric overview](https://learn.microsoft.com/en-us/fabric/fundamentals/microsoft-fabric-overview)
to locate workload documentation, then verify the specific capability and limits.
An overview alone is not evidence that an item supports a particular operation.
