---
title: Fabric project setup
description: Repository conventions, environment context, readiness checks, and pending setup actions.
status: draft
---

## Repository

* Project and Git provider: {{name and provider; unresolved choices stay open}}
* Existing instructions and conventions: {{references}}
* Architecture, spec, artifact, and test locations: {{actual agreed locations}}
* Validation entry points: {{commands or explicit missing checks}}
* Applied changes: {{requested changes and preserved existing content}}

## Environment inventory

Repeat for each relevant environment. Store references, not credentials.

* Environment name and purpose: {{development, test, or other agreed purpose}}
* Tenant and workspace: {{confirmed identifiers or unresolved}}
* Capacity context: {{known assignment, requirements, or pending verification}}
* Identity and authentication: {{method, role needs, and secret-store references}}
* Configuration and ownership: {{where non-secret bindings live and who owns them}}
* Authorized operations: {{scope, authorizing owner, and actual authorization}}

## Readiness checks

Repeat for each relevant tool, connection, permission, or configuration check.

* Check: {{what readiness claim is being tested}}
* Command or operation and target: {{non-secret details}}
* Status: {{verified, failed, blocked, or not checked}}
* Result and date: {{observed result, not an inferred capability}}
* Gap, owner, and next action: {{what is needed to proceed}}

## Safe setup and reruns

* Existing files and resources reused: {{references}}
* Conflicts: {{unresolved collisions and required decisions}}
* Rerun behavior: {{how existing state is detected and duplicates are avoided}}
* Live changes performed: {{operation, exact target, and observed result, or none}}
* Architecture-dependent needs: {{items intentionally not decided yet}}

## Handoff

* Ready for repository-only work: {{scope and limitations}}
* Ready for live Fabric work: {{verified scope or blockers}}
* Setup instructions still required: {{steps, owner, and prerequisites}}
* Next design or delivery action: {{bounded next step}}
