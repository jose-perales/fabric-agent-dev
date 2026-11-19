---
title: Fabric delivery and release runbook
description: Provider workflows, supported operations, target bindings, checks, and release results.
status: draft
---

## Delivery decisions

* Slice, spec, and implementation: {{references}}
* Git provider and workflow files: {{chosen provider and actual locations}}
* Source of truth and branch policy: {{repository/workspace ownership}}
* Candidate identity: {{explicit revision or immutable artifact reference}}
* Approval owners and enforcement: {{provider/environment controls}}
* Open decisions: {{question, dependent scope, owner, and next action}}

## Item support

Repeat for each selected item type.

* Item type and serialization: {{actual supported artifact format}}
* Git support: {{supported operation or limitation}}
* Deployment and identity support: {{chosen mechanism and limitations}}
* Binding, data, and permission behavior: {{what is and is not included}}
* Evidence: {{current official source or observed check, date, and scope}}
* Manual step or blocker: {{action and accountable owner}}

## Environment configuration

Repeat for each intended target; never store secret values.

* Environment, tenant, and workspace: {{explicit non-secret identifiers}}
* Deployment identity and required roles: {{identity and access scope}}
* Configuration and secret references: {{provider-approved locations}}
* Bindings and dependencies: {{connections, item references, and ordering}}
* Authorization and gates: {{required approvals and actual configuration}}
* Drift/conflict handling: {{detection, stop condition, and resolution owner}}

## Workflow

* CI: {{triggers, actual validation commands, fixtures, and required gates}}
* Trust boundary: {{untrusted validation versus privileged delivery}}
* Candidate selection: {{how the exact tested revision reaches delivery}}
* Preflight: {{access, approval, target, drift, and dependency checks}}
* Synchronization: {{explicit Git operation, or not used with reason}}
* Deployment: {{content mechanism and order}}
* Provisioning, binding, and migration: {{separate required operations or none}}
* Post-deployment checks: {{spec criteria, expected results, and target context}}

## Failure and rerun runbook

* Partial or ambiguous result: {{inspection and reconciliation procedure}}
* Safe rerun: {{idempotent steps, unsafe repeats, and checkpoints}}
* Rollback or forward fix: {{decision owner, procedure, and preconditions}}
* Data recovery: {{separate reconciliation/restoration obligations and owner}}
* Manual escalation: {{action and accountable owner}}

## Exercise results

Repeat for each actual release attempt. Do not pre-populate passing results.

* Revision, target, authorization, and date: {{actual execution context}}
* Operation/run reference: {{durable reference}}
* Status: {{passed, failed, blocked, or not run}}
* Observed checks: {{criterion, expected result, actual result, and reference}}
* Remaining work: {{manual or unexercised steps, blockers, and owners}}

## Readiness summary

* Workflow authored: {{status}}
* Locally validated: {{checks and actual results}}
* Development exercised: {{result or not run}}
* Promotion exercised: {{result or not run}}
* Repeat release exercised: {{later revision result or not run}}
