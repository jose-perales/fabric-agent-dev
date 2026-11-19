---
name: data-value-frame
description: "Frame a data opportunity, business value, success measures, and source feasibility. Use for data discovery or scoping a Fabric initiative"
---

# Data Value Frame

## Overview

Turn a proposed data initiative into an agreed problem, measurable outcomes, and
a feasible first slice. Start with the decision or process to improve, not a
preferred Fabric workload. This is a first-draft workflow.

## Prerequisites

Use the user's business context, existing documents, and any authorized source
descriptions or samples. A repository, Fabric connection, and finished solution
design are not required.

Ask for missing information that changes the opportunity or first-slice scope.
Carry lesser unknowns as questions with owners. Never request secrets or copy
sensitive source records into the frame.

## Quick Start

Invoke `/data-value-frame` with the opportunity, intended users, and any known
data sources. Use the [value-frame template](./assets/value-frame.template.md)
when a new document is needed.

Reuse the project's document convention. Otherwise save the frame as
`docs/value-frame.md` in the consuming repository. Update existing work rather
than creating a competing frame.

## Workflow

1. Establish who needs to make which decision, what happens today, and what is
   costly, slow, unreliable, or unavailable. Separate the requested deliverable
   from its underlying business value.
2. Define scope, exclusions, business terminology, and priority. Ask the business
   owner to resolve conflicting metric definitions rather than choosing one.
3. Define each success measure's meaning, baseline, target, assessment window,
   assessment method, and accountable owner. Mark missing values as unknown;
   do not invent a baseline, benefit estimate, or stakeholder agreement.
4. Inventory candidate sources, owners, access routes, grain, keys, available
   history, freshness, and known limitations. Label claims as observed,
   stakeholder-reported, or assumed, with a source and date where available.
5. Inspect only the documentation or samples needed to assess feasibility.
   Record sample scope and limitations; a small sample does not establish
   production-wide data quality. Do not imply inaccessible data was inspected.
6. Propose the smallest slice connecting an available source to a useful business
   result. Include a worked example with the expected result and why it matters.
7. Review value, feasibility, constraints, and open questions together. Recommend
   proceeding to architecture, investigating named gaps, or stopping. Capture
   actual owner acceptance separately from the agent's recommendation.

## Output and completion

Produce a value frame containing the problem, users, business definitions,
success measures, source assessment, first slice, and open decisions with owners.
Record relevant access, governance, budget, freshness, and delivery constraints.

Before handing off to `solution-arch-docs`, check that:

* Each proposed capability supports an identified decision or outcome.
* Measures have assessment methods; missing targets and baselines are explicit.
* A worked example distinguishes correct from incorrect business behavior.
* Material source-feasibility gaps and unresolved definitions are visible.
* Proceeding does not depend on invented data facts or approvals.

Summarize what is ready, what is blocked, and which questions need an owner.
Do not select a detailed architecture or provision resources during framing.

## Troubleshooting

* If the request is only a technology choice, elicit the business decision and
  constraints before recommending a solution.
* If sources cannot be inspected, produce a provisional frame with a concrete
  investigation action, not an asserted feasibility result.
* If no owner can resolve a material definition, block the dependent scope while
  preserving useful agreed findings.
