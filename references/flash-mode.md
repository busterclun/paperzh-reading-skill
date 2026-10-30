# Flash mode reference

## Purpose

Flash is a rapid, evidence-aware literature triage workflow. Its output must be useful for batch reading and horizontal comparison, not a shallow abstract paraphrase.

## Per-paper card

Use this order unless the user requests a different structure:

1. **Identification** — title, authors, year, venue, DOI/URL, source material available.
2. **One-sentence contribution** — what changed because of this paper.
3. **Research logic** — problem → gap → question/hypothesis → method → result → conclusion.
4. **What the author actually did** — object, method, variables, controls, data/model, validation.
5. **Key results** — numbers, trends, effect direction, and evidence location.
6. **Vulnerabilities** — finding, type, impact, evidence location, confidence.
7. **Scenario boundary** — working fluid/material, operating conditions, geometry/scale, flow/state, boundary/initial condition, model/measurement range.
8. **Concept quantification** — definition, metric, equation, measurement/computation, criterion, evidence, reproducibility.
9. **Research value** — cite, reproduce, adapt, or deprioritize; Deep priority.

## Vulnerability labels

| Label | Use when |
|---|---|
| Confirmed flaw | Supplied evidence shows an invalid inference, contradiction, or inadequate control |
| Material limitation | The design is valid within a narrower boundary than the headline conclusion suggests |
| Unverified assumption | A premise is necessary but not tested or justified in the supplied material |
| Missing information | The paper or supplied copy does not allow a reliable judgment |

Do not turn missing information into a confirmed flaw.

## Comparison matrix

Use one row per paper and keep the following columns whenever relevant:

| Paper | Question/gap | Object/system | Method | Key variables | Baseline/control | Main result | Evidence strength | Scenario boundary | Quantification maturity | Main vulnerability | Transferable value | Deep priority |
|---|---|---|---|---|---|---|---|---|---|---|---|---|

Use `High/Medium/Low` only with a one-line rationale. Add `Not comparable` when definitions, scales, or conditions differ materially.

## Fast triage decision

Recommend Deep review when at least one is true:

- the result is central to the user's research question;
- the mechanism claim is strong but evidence or controls are uncertain;
- the paper may supply a reusable method, validation case, or benchmark;
- scenario transfer is plausible but not demonstrated;
- the concept is important yet weakly quantified;
- the paper is a candidate source for a thesis, design decision, or replication.

## Flash anti-patterns

- Copying the abstract as the main answer.
- Ranking papers only by venue or citation count.
- Saying “limited applicability” without listing the exact boundary.
- Calling a concept “qualitative” without checking for an operational definition.
- Treating author-stated limitations as the complete critique.
- Providing a chat summary but no DOCX deliverable.

