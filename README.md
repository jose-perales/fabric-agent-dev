---
title: Fabric delivery skills
description: First-draft skills for taking a data opportunity through architecture, specifications, implementation, and Fabric delivery.
---

## Status

Six draft skills follow a practical Fabric delivery workflow. They provide
instructions and lightweight templates, not a deployment platform or a guarantee
that a business solution has been verified.

## Skills

### Layer 1: Value and setup

* [data-value-frame](.apm/skills/data-value-frame/SKILL.md) connects a data
  opportunity to measurable business value and feasible sources.
* [repo-fabric-setup](.apm/skills/repo-fabric-setup/SKILL.md) prepares repository
  conventions and establishes explicit Fabric environment readiness.

### Layer 2: Solution architecture

* [solution-arch-docs](.apm/skills/solution-arch-docs/SKILL.md) documents a justified
  architecture, data design, alternatives, and unresolved constraints.

### Layer 3: Build and delivery

* [build-fabric-specs](.apm/skills/build-fabric-specs/SKILL.md) creates, refines, or
  reviews bounded specs with testable acceptance criteria.
* [implement-fabric-specs](.apm/skills/implement-fabric-specs/SKILL.md) implements
  ready specs and reports criterion-level verification results.
* [build-fabric-cicd-gitops](.apm/skills/build-fabric-cicd-gitops/SKILL.md) builds
  validation and controlled delivery for the selected provider and Fabric items.

The initial `review-spec` skill is replaced by the read-only review mode in
`build-fabric-specs`.

## Use

### Install in another repository

With [Agent Package Manager](https://github.com/microsoft/apm) installed, open your
new project directory and run:

```bash
apm init --yes --target copilot
apm install jose-perales/fabric-agent-dev
```

For an existing APM project, skip initialization and install the dependency.
Use the Copilot target to materialize the skills in the project's
`.agents/skills/` directory. No Fabric credentials are needed to install them.

The install records the dependency in the consumer's `apm.yml` and pins its
resolved revision in `apm.lock.yaml`. Commit both files to reproduce the install;
use `apm install --frozen` to restore the locked dependency.

Open the consumer project in VS Code and start a new Copilot chat. If the skills
do not appear in the slash-command picker, reload the VS Code window.

### Try a skill

Invoke a skill with its slash command and the relevant context, for example:

```text
/data-value-frame Frame the opportunity to reduce late order reporting.
/repo-fabric-setup Inspect this repository and identify Fabric setup gaps.
/solution-arch-docs Draft architecture from the agreed value frame.
/build-fabric-specs Specify the first daily order-ingestion slice.
/build-fabric-specs Review the attached spec without modifying it.
/implement-fabric-specs Implement the ready order-ingestion spec.
/build-fabric-cicd-gitops Build CI/CD for the implemented slice.
```

Framing and setup can start independently. Existing projects can supply equivalent
documents and enter at the relevant skill. Workload, provider, authentication,
and live targets are chosen from project context, not fixed by these drafts.

Document work needs no Fabric connection. Implementation and delivery require
the selected workload tools and explicitly authorized access for live actions.
No external workload skills, runtimes, or MCP servers are bundled by this package;
each skill checks the capabilities available in the consuming environment.

## Develop

Edit the source packages in [.apm/skills/](.apm/skills/). Each contains its workflow
and a template loaded only when needed. APM materializes the Copilot copies in
[.agents/skills/](.agents/skills/) and records them in
[apm.lock.yaml](apm.lock.yaml). Do not edit those copies as the source of truth.

After changing source packages:

```bash
apm install
apm audit --ci
```

These checks do not prove agent behavior or a live Fabric release. Exercise the
drafts on one bounded reference scenario, including an ambiguous requirement and
a failed acceptance check, before treating the workflow as proven.

Generalized policy frameworks, factory evaluations, managed upgrades, universal
adapters, and resumable agent coordination remain outside this iteration.
