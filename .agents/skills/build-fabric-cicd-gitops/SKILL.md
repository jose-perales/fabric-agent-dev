---
name: build-fabric-cicd-gitops
description: "Build Fabric CI/CD, Git integration, release workflows, and promotion checks. Use to automate controlled delivery of versioned Fabric artifacts"
---

# Build Fabric CI/CD and GitOps

## Overview

Build provider-specific validation and controlled delivery for the implemented
Fabric items. Keep Git synchronization, content deployment, environment binding,
and data migration distinct. This is a first-draft workflow, not a universal
deployment engine.

## Prerequisites

Use setup context, architecture, specs, implemented artifacts, and validation
commands. Workflow design can begin early, but a proved release needs a known
candidate, authorized target, and actual post-deployment checks.

Determine the provider and mechanisms from repository evidence. Ask when GitHub
versus Azure DevOps, the target, identity, or approval ownership is undecided.
No deployment tool or service connection is assumed available.

## Quick Start

Invoke `/build-fabric-cicd-gitops` with the implemented slice and target context.
Use the [delivery template](./assets/fabric-delivery.template.md) for the release
design, runbook, and results. Reuse project conventions or default to
`docs/fabric-delivery.md`.

Generate executable workflows for the chosen provider only after the necessary
decisions and supported item mechanisms are known. An unexercised draft is not a
successful delivery.

## Workflow

1. Inspect existing CI/CD, source-of-truth rules, repository protections, setup
   context, item definitions, dependencies, and spec checks. Preserve functioning
   delivery paths rather than creating a parallel deployment system.
2. Check current official support for each selected item type, Git operation,
   deployment mechanism, and identity. Build a small support matrix with evidence
   and limitations. Do not infer deployment support from Git support or assume
   definitions include data, permissions, credentials, or environment bindings.
3. Establish repository/workspace ownership, branches, environment targets,
   configuration, and drift/conflict handling. Ask for consequential decisions;
   do not overwrite workspace changes or connect a different branch by default.
4. Build CI using the implementation's actual validation commands and fixtures.
   Fail required checks on errors and preserve logs. Keep untrusted contribution
   validation separate from privileged release jobs and deployment secrets.
5. Build delivery from an explicit revision or immutable artifact. Resolve
   target-specific bindings, identity permissions, dependency order, preflight
   checks, and provider-enforced approvals. Use approved secret storage or
   federation, never embedded credentials or a developer's cached login.
6. Represent Git synchronization, provisioning if needed, content deployment,
   binding, and data migration as explicit operations. Reuse supported workload,
   Git-integration, or deployment-pipeline capabilities. Record manual steps with
   owners and stop when an unsupported step blocks safe delivery.
7. Validate workflow syntax and applicable local checks. Configure or execute
   live delivery only when authorized for the exact target and revision.
   Exercise development first; promote to another environment only when available
   and separately authorized. Do not push or enable a release merely to test it.
8. Check the deployed revision, target bindings, dependencies, and spec-defined
   behavior. Await asynchronous operations to a supported terminal result;
   accepted or queued does not mean deployed. Record partial or ambiguous outcomes.
9. Document rerun and reconciliation steps plus rollback or forward-fix decisions.
   Separate code rollback from restoration or reconciliation of changed data.
   Exercise a later revision when authorized before claiming repeatability.

## Output and completion

Produce the chosen provider's workflows, non-secret configuration examples,
support matrix, drift policy, release/failure runbook, and observed check results.

Check that:

* Required failing checks prevent release of the affected revision.
* Revision, destination, identity, and bindings are explicit.
* Missing access, missing approval, or unresolved drift stops the affected action.
* Post-deployment checks establish relevant behavior, not only API success.
* Partial deployment cannot be reported as a successful complete release.
* Manual steps and unexercised environments remain visible limitations.

Report workflow-authored, locally-validated, development-exercised, and
promotion-exercised states separately. Never claim a release was exercised from
generated workflow text alone.

## Troubleshooting

* If the provider or target is undecided, complete the design and open decisions
  without producing a success-shaped placeholder workflow.
* If required checks fail, stop promotion and return defects to implementation.
* If an operation times out or partially succeeds, inspect actual state before
  retrying; escalate data recovery to the accountable owner.

## Platform references

Consult current support and limitations rather than freezing an item list here:

* [Fabric Git integration](https://learn.microsoft.com/en-us/fabric/cicd/git-integration/intro-to-git-integration)
* [Fabric deployment pipelines](https://learn.microsoft.com/en-us/fabric/cicd/deployment-pipelines/intro-to-deployment-pipelines)
