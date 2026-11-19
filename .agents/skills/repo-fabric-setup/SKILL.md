---
name: repo-fabric-setup
description: "Prepare a repository and check Fabric workspace, identity, tooling, and configuration readiness. Use to bootstrap or adopt a Fabric project"
---

# Repository and Fabric Setup

## Overview

Establish the minimum repository conventions and explicit Fabric context needed
to design and build a solution. Support empty and existing projects without
overwriting local work. This is a first-draft workflow, not an upgrade manager
or a CI/CD implementation.

## Prerequisites

Use the current repository and any supplied workspace, Git-provider, and identity
context. Setup can begin without a value frame or Fabric credentials.

Live checks need an available supported tool and authorized access. Live changes
also need an explicit tenant, workspace or resource target, and authorization for
the proposed operation. Never collect credentials in chat or commit them.

## Quick Start

Invoke `/repo-fabric-setup` with the repository and intended development context.
An inspection-only request produces findings without changing files or resources.

Use the [setup template](./assets/fabric-setup.template.md) for a new setup guide,
defaulting to `docs/fabric-setup.md` only when no project convention exists.

## Workflow

1. Inspect applicable repository instructions, worktree state, existing Fabric
   artifacts, manifests, tests, configuration, and document conventions. Identify
   conflicts before proposing changes; do not reset or stash unrelated work.
2. Identify the Git provider and intended development environment from evidence.
   Ask when a consequential choice remains ambiguous. Do not choose a tenant,
   capacity, workspace, or authentication method by guessing.
3. Propose the smallest setup change set. Reuse existing locations; when absent,
   suggest `docs/` for value/setup records, `docs/architecture/` for design,
   `specs/` for slices, `src/` for artifacts, and `tests/` for validation. Create
   only what is needed now, not a tree of empty placeholders.
4. Apply requested repository setup, preserving user-owned content. Document
   non-secret environment references, configuration ownership, authentication
   instructions, and available validation commands. Do not install tools merely
   because they might be useful.
5. Check relevant tooling and, when authorized, connectivity, workspace identity,
   capacity context, and required permissions. Use read-only checks first.
   Successful authentication alone does not establish all required permissions.
6. For requested live setup, resolve the exact target and inspect existing
   resources before creation. Confirm authorization for changes or cost-bearing
   actions. If the required tool or permission is missing, record the blocked
   action and owner instead of attempting an undocumented workaround.
7. Reconcile results against the proposed change set. Check that repeated setup
   reuses the same files and resources without duplicates or destructive edits.
   Report architecture-dependent setup still to be decided.

## Output and completion

Produce the setup guide, requested configuration changes, and a readiness report
showing each check as verified, failed, blocked, or not checked. Include the
command or operation, target, result, and next action without secret values.

Completion requires that:

* Repository locations and validation entry points are explicit.
* Live operations identify their actual target and authorization.
* Readiness claims are limited to checks actually performed.
* Conflicts and missing access are actionable rather than hidden by defaults.
* Existing work is preserved and reruns do not duplicate setup.

Hand design constraints to `solution-arch-docs`. Leave Git synchronization,
promotion, and automated delivery to `build-fabric-cicd-gitops`.

## Troubleshooting

* If Fabric access is unavailable, complete repository-only setup and identify
  which live checks remain blocked.
* If a destination already contains conflicting content, show the conflict and
  obtain a decision instead of overwriting it.
* If architecture changes environment needs, update the relevant setup records
  and resources under authorization; do not rerun unrelated bootstrap work.

## Platform reference

Consult the current [Fabric overview](https://learn.microsoft.com/en-us/fabric/fundamentals/microsoft-fabric-overview)
and the selected workload's official prerequisites before asserting readiness.
