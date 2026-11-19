---
name: implement-fabric-specs
description: "Implement ready Fabric specs, author solution artifacts, and verify acceptance criteria. Use to build a bounded specified slice, not to invent requirements"
---

# Implement Fabric Specifications

## Overview

Implement a ready spec as reviewable Fabric artifacts and test the required
behavior against independent expected results. Keep authoring, local validation,
deployment, and runtime verification distinct. This is a first-draft workflow.

## Prerequisites

Use a bounded spec with acceptance criteria, the relevant architecture, and
repository conventions. Confirm readiness from the actual contents, not only a
status label. Missing consequential semantics or test oracles block dependent work.

Use the consuming project's selected workload tools and installed authoring
skills. No particular CLI, MCP server, or external skill is bundled or guaranteed.
Live checks require explicit target context, prerequisites, and authorization.

## Quick Start

Invoke `/implement-fabric-specs` with a ready slice spec and requested scope.
Use the [implementation record](./assets/implementation-record.template.md) for
the handoff. Adapt it to an existing change record or the response; save a separate
report only when requested or required by project conventions.

## Workflow

1. Read the spec, design, applicable instructions, affected artifacts, worktree
   state, and existing tests. Identify each required change and acceptance check.
   Report material conflicts or missing readiness conditions before dependent edits.
2. Select the appropriate available workload authoring capability for the actual
   Fabric item types. Inspect existing patterns and current supported formats.
   Load relevant workload guidance before writing specialized code or definitions.
   If a required capability is unavailable, report the gap rather than fabricating
   tool commands or serialized item formats.
3. Implement the smallest coherent slice in dependency order. Preserve existing
   business semantics and unrelated edits. Keep environment bindings configurable
   and secrets external to source artifacts.
4. Implement specified data-quality, incremental, rerun, failure, and recovery
   behavior. Do not compensate for unresolved requirements by expanding scope or
   choosing convenient business rules.
5. Add or update focused tests using the spec's independent expected results,
   including applicable edge cases. Run existing structural validators and local
   checks first; do not add a new test framework without a demonstrated need.
6. Perform required live development checks only with authorized access and the
   exact intended workspace and items. Record what changed. Reconcile ambiguous
   or partial mutations before retrying; do not blindly rerun non-idempotent work.
7. Map every acceptance criterion to an observed result or explicit failed,
   blocked, or not-run check. Include the command or procedure, revision or change
   context, target, and relevant result. Mock results do not prove live integration.
8. Fix defects within the slice and rerun affected checks. Return necessary spec
   or design changes to their owner; identify the tests and prior acceptance
   affected by an agreed change.

## Output and completion

Produce the implementation, tests, and a concise acceptance/handoff record.
Include artifact dependencies, configuration needs, required runtime checks, and
known limitations for `build-fabric-cicd-gitops`.

Completion requires that:

* Changes trace to the spec and pass the required available local checks.
* Specified rerun, quality, and failure behavior has appropriate tests.
* Each acceptance criterion has an explicit status and supporting result.
* Runtime-verified claims name the actual target and observed behavior.
* Required failed or blocked checks prevent a fully verified claim.

Local completion can be reported separately when live checks are blocked. Do not
silently convert blocked checks to passing results, claim production readiness,
or create commits, push changes, or release to production without a request.

## Troubleshooting

* If the spec is not implementable, report the precise missing decision and
  affected scope; use `build-fabric-specs` to refine it.
* If a validator fails, determine whether the artifact or test is wrong against
  the spec. Do not weaken assertions to make generated output pass.
* If live access is unavailable, preserve locally validated work and provide the
  exact pending checks and prerequisites.
