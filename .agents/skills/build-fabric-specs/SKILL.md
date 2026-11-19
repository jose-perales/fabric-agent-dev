---
name: build-fabric-specs
description: "Create, refine, or review Fabric specifications and acceptance criteria. Use for implementation-ready slices or a read-only spec readiness review"
---

# Build Fabric Specifications

## Overview

Translate agreed architecture into bounded specs with observable behavior and
independently checkable results. Review existing specs using the same readiness
checks. This first-draft workflow includes the former standalone spec-review use
case; it does not implement or deploy the solution.

## Prerequisites

Use the architecture, value definitions, setup context, and existing specs, or
equivalent user-supplied information. A finished document set is not mandatory
when the needed facts are available.

Ask for consequential missing business rules, expected results, or design
decisions. Missing live access can limit validation without preventing a draft.

## Quick Start

Invoke `/build-fabric-specs` with the slice and relevant design. For a review,
invoke `/build-fabric-specs Review this spec without modifying it`.

For authoring, use the [spec template](./assets/fabric-spec.template.md), preserving
project conventions or defaulting to `specs/<slice-name>.md`.

In review-only mode, read the supplied spec and relevant references, then return
findings and readiness. Do not edit files or generate a replacement spec unless
the user requests changes. Ask for the spec if none is supplied.

## Workflow

1. Establish whether the request is authoring, refinement, or read-only review.
   Read the relevant business definitions, design, setup constraints, and current
   spec. Preserve accepted decisions; flag conflicts instead of silently choosing.
2. Bound one useful end-to-end slice. Identify affected artifacts and item types,
   dependencies, inputs, outputs, exclusions, and preconditions.
3. Specify schemas, mappings, transformations, interfaces, non-secret bindings,
   and applicable duplicate, missing-value, late-data, delete, failure, and rerun
   behavior. Include migration or recovery needs when the change requires them.
4. Give requirements and acceptance criteria stable local identifiers. For each
   criterion state its requirement, test method, input/fixture, expected result,
   measurable threshold where relevant, and required execution context.
5. Include small synthetic or approved fixtures with independently known expected
   results. Separate local checks, live Fabric checks, and human acceptance.
   Do not derive the only test oracle from the implementation under test.
6. Review completeness, consistency, feasibility, and testability against the
   supplied design. Identify missing failure behavior, unsupported platform
   assumptions, and unmet authorization or environment prerequisites.
7. Report findings with severity, source location, impact, and a specific remedy.
   Use High for implementation or validation blockers, Medium for material gaps,
   and Low for minor ambiguities. Missing references are limitations, not evidence
   that the referenced requirements are satisfied.
8. In authoring/refinement mode, resolve findings within the agreed scope or
   record blockers with owners. Mark the slice ready only when material ambiguity
   is resolved and each requirement has an acceptance method and expected result.
   Record actual required owner acceptance separately from this recommendation.

## Output and completion

For authoring, produce the spec, fixtures or examples, implementation order, and
a readiness summary. For review, return findings, open questions, and readiness;
explicitly state when no findings were identified within the reviewed scope.

Check that:

* Each criterion has an expected result and a way to establish it.
* Consequential edge cases specify behavior rather than generic assurances.
* Artifact dependencies and execution prerequisites are explicit.
* Unsupported assumptions and unresolved definitions block dependent scope.
* A material spec revision identifies which prior tests, implementation, or
  acceptance decisions need to be revisited.

Hand a ready slice to `implement-fabric-specs`. A structurally complete template
or an agent's confidence is not a readiness decision.

## Troubleshooting

* If the slice is too broad to implement and check coherently, split it by useful
  end-to-end behavior, not arbitrary document or technology boundaries.
* If live checks are unavailable, specify them and record the missing access;
  never mark them passed.
* If business semantics conflict, return the decision to the business owner or
  architecture rather than repairing the ambiguity through implementation.
