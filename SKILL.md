---
name: paperzh-reading
description: "Read and critically analyze research papers in Chinese using Flash batch comparison or Deep three-layer close reading, then deliver evidence-based DOCX reports with explicit method limits, scenario boundaries, quantification checks, and research-transfer priorities. Use when the user asks to read, compare, critique, or extract research value from one or more papers."
---

# Paperzh Reading Skill

## Purpose and non-negotiable outcome

Use this skill for scientific-paper reading, rapid literature screening, cross-paper comparison, and deep critical review. The skill has two genuinely different modes:

- **Flash**: fast, batch-friendly reading for screening and horizontal comparison.
- **Deep**: full three-layer close reading for important papers and research decisions.

For either mode, the final user-facing deliverable is a **`.docx` Word document**, not only chat text. Chat may contain a concise handoff, but the report is the authoritative deliverable. Unless the user explicitly asks otherwise, write the report in Chinese while preserving original English terminology, symbols, units, equations, figure labels, and paper quotations where needed.

Do not invent missing experimental conditions, equations, data, figure readings, citations, or author claims. Separate four states whenever evidence is incomplete: **paper explicitly states**, **directly observed from supplied material**, **reasonable inference**, and **cannot determine from the supplied material**.

## Mode selection

Choose the least expensive mode that can answer the request well. If the user names a mode, follow it. Otherwise:

| Situation | Default mode | Deliverable |
|---|---|---|
| Many papers, initial screening, literature map, quick comparison | Flash | One comparative DOCX; include per-paper cards and a ranked follow-up list |
| One important paper, thesis background, method replication, referee-style critique | Deep | One detailed DOCX per paper, or one combined DOCX if requested |
| Mixed batch with a few priority papers | Flash first, then Deep for selected papers | Flash comparison DOCX plus Deep DOCX for selected papers |

If the request is ambiguous but the number of papers is large, start with Flash and state that Deep review can follow for selected papers. Do not silently turn Flash into a truncated Deep report.

## Input and evidence handling

1. Identify every paper by title, authors, year, venue, DOI or stable identifier when available.
2. Prefer the supplied PDF/full text. If only an abstract, metadata, screenshot, or excerpt is available, limit claims to that evidence and say what is missing.
3. Read the abstract, introduction, methods, results, discussion/conclusion, captions, supplementary material, and references in proportion to the selected mode.
4. Preserve paper-local terminology. Explain a term in Chinese on first use, then retain the original English in parentheses when it prevents ambiguity.
5. Record evidence locations: section, page, figure/table/equation number, or a short searchable phrase. Page numbers may be approximate only when the source rendering makes them unreliable.
6. Distinguish the authors' stated limitations from limitations discovered during review. Do not label an omitted detail a flaw when the supplied paper does not establish whether it was controlled elsewhere.

## Shared analytical frame

Every report must reconstruct the paper as a chain:

`problem → gap/claim → research question or hypothesis → object/system → variables and controls → method/model → evidence → result → conclusion → validity boundary → transferable value`

At minimum, answer these questions:

- What problem is being solved, and why does it matter?
- What is the actual research object and scale?
- What did the authors do, not merely what did they say?
- Which variables, controls, baselines, and evaluation criteria carry the argument?
- What result supports each major conclusion?
- Which assumptions are explicit, hidden, or untested?
- Where can the conclusion be used, and where can it not be transferred?
- Which concepts are operationalized into measurable or computable quantities?
- What is the most valuable next research step?

Use calibrated judgments instead of a single unsupported score. When a summary table uses labels such as `高/中/低`, include the reason and evidence location.

## Flash mode — batch reading and horizontal comparison

Flash is not an abstract translation. It is a decision-oriented reading pass that lets the user explain each paper in roughly one or two minutes, compare papers on common dimensions, and decide which papers deserve Deep review.

For each paper, produce the following complete card.

### A. One-minute research card

1. **一句话结论** — the paper's actual contribution, not its topic.
2. **Why** — problem, context, and gap.
3. **What** — research object, system, material/working fluid, geometry, scale, or dataset.
4. **How** — experiment, simulation, theory, data analysis, or combination; name the key method/model.
5. **What was found** — 2–5 result statements with numbers when available.
6. **What is genuinely new** — distinguish novelty from routine application or parameter sweep.
7. **Usefulness** — what can be cited, reproduced, adapted, or ignored.

### B. Four mandatory critical checks

#### 1. Research gaps and vulnerabilities

Actively inspect beyond the authors' self-declared limitations:

- Is the research question answered by the chosen design?
- Are controls, baselines, mesh/time-step independence, uncertainty, repeatability, or statistical tests sufficient for the claim?
- Are key variables isolated, or do several mechanisms change together?
- Does correlation get described as causation?
- Do data and resolution support the level of mechanistic detail claimed?
- Are alternative explanations ruled out?
- Are model closure, boundary conditions, constitutive laws, contact angles, initial conditions, or fitting choices justified?
- Are comparisons fair in geometry, scale, operating condition, definition, and metric?
- Are negative or contradictory results omitted?
- Does the conclusion exceed the evidence?

Classify each finding as `confirmed flaw`, `material limitation`, `unverified assumption`, or `information not available`. State impact: affects mechanism, magnitude, reproducibility, or generalizability.

#### 2. Scenario limitations and validity boundaries

Create a standalone **工质—工况—边界条件适用性** section. Check at least:

- working fluid/material composition and properties;
- temperature, pressure, heat flux, Reynolds/Weber/Prandtl or other relevant dimensionless ranges;
- phase regime, flow regime, gravity/orientation, transient versus steady operation;
- geometry, surface condition, scale, roughness, confinement, and manufacturing tolerance;
- inlet/outlet, wall, initial, symmetry, periodic, and interface boundary conditions;
- sensor or imaging field of view, sampling rate, resolution, and data-processing window;
- numerical domain, discretization, solver, closure, convergence, and validation range;
- whether a conclusion is local, parameter-range-specific, device-specific, or plausibly general.

End with three explicit statements: **可直接适用**, **需要验证后适用**, and **不能直接外推**. For every non-transferable result, explain the physical or methodological reason.

#### 3. Core concepts: operationalization and quantification

Check whether concepts such as stability, enhancement, dominant mechanism, coupling, transition, interface evolution, or significant influence are operationally defined. For each important concept, fill this chain:

`概念定义 → 物理量/指标 → 数学表达式 → 测量或计算方法 → 阈值/判据 → 证据 → 是否可复现`

If the paper uses persuasive language without a measurable indicator or testable criterion, say explicitly: **概念已提出，但尚未形成可操作、可验证的量化判据**. Do not demand a single scalar when a validated multi-indicator or qualitative criterion is appropriate; judge whether the operational definition is clear and falsifiable.

#### 4. Research value and next action

Give a compact recommendation:

- methods worth borrowing;
- conclusions safe to cite and the boundary that must accompany the citation;
- weaknesses that could become a research question;
- whether the paper merits Deep review;
- the single highest-value next check or experiment/simulation.

### C. Batch comparison

For two or more papers, normalize terminology before comparing. Include a comparison matrix with at least:

`paper | question/gap | object/system | method | key variables | baseline/control | main result | evidence strength | scenario boundary | quantification maturity | main vulnerability | transferable value | Deep priority`.

Do not rank papers by journal prestige or citation count unless the user asks. Rank by relevance to the user's question, evidence quality, transferability, and unresolved value. Explain incomparable metrics instead of forcing a numeric ranking.

See [references/flash-mode.md](references/flash-mode.md) for the required card and comparison schema.

## Deep mode — three-layer close reading

Deep preserves the rigor of a full paper review. It must not omit figures, tables, formulas, evidence links, or transfer analysis simply because the report is long.

### Layer 1: orientation and argument reconstruction

Build a precise overview:

- research context, problem, gap, question, and hypothesis;
- object/system and why it is an appropriate representation;
- paper contribution in the authors' terms and in an independent assessment;
- full method map from inputs to outputs;
- definitions of all central variables and evaluation metrics;
- a concise argument diagram in prose or table form.

Then write an executive summary that a technically literate reader can use without reading the full report.

### Layer 2: structural, method, and evidence reading

Trace the paper section by section and connect each claim to evidence.

- **Introduction:** Is the gap real, specific, and logically connected to the work?
- **Methods/model:** Identify assumptions, governing equations, constitutive/closure choices, parameter values, initial and boundary conditions, numerical or experimental controls, uncertainty, and validation.
- **Results:** Read all key figures/tables, not only the text summary. For each, state what changes, what is held fixed, scale/trend, uncertainty, and which claim it supports.
- **Discussion:** Test whether the proposed mechanism is distinguished from alternatives and whether evidence supports causality.
- **Conclusion:** Map each conclusion to the minimum evidence needed and check overreach.

For formulas, explain only what improves understanding but do not skip key equations. Capture equation number, meaning of symbols and units, assumptions, limiting behavior, and how the equation is used in the reported result. If a derivation is not shown, say so.

For figures and tables, record: `编号/标题 → purpose → axes/units/legend → variables and controls → main pattern → uncertainty or resolution → evidence supported → caveat`. Reproduce or embed original figures only when legally and technically appropriate; otherwise describe them accurately and cite their location.

### Layer 3: critical appraisal and research transfer

Assess the complete evidence chain:

`claim → required evidence → supplied evidence → missing evidence → alternative explanation → confidence → boundary`.

Cover:

- internal validity and design adequacy;
- measurement, numerical, statistical, and reproducibility risks;
- mechanism versus association;
- sensitivity to material properties, working fluid, operating condition, geometry, scale, and boundary condition;
- concept operationalization and quantification maturity;
- external validity and scale-up/scale-out risks;
- what the authors acknowledge versus what they do not;
- how the study compares with cited and competing work when the supplied references support it.

Convert the critique into a research-transfer plan. Each proposed gap must specify:

`problem/gap | why it matters | hypothesis | variable(s) | controlled factors | method | validation criterion | expected decision | priority | effort/risk`.

Prioritize with `P0` (blocks validity or changes the conclusion), `P1` (high-value generalization or mechanism test), and `P2` (incremental refinement). Do not call a gap novel without checking the supplied literature; label it `candidate gap` when that check is incomplete.

See [references/deep-mode.md](references/deep-mode.md) for the deep-review evidence matrix and figure/formula protocol.

## DOCX deliverable requirements

Create the report as a real editable `.docx`. Use the document-generation capability available in the environment; load workspace document dependencies when needed. Do not merely rename Markdown or PDF files to `.docx`.

### Typography and layout

- Chinese headings: **SimHei (黑体)**.
- Chinese body text: **SimSun (宋体)**.
- English text, Latin characters, and numbers: **Times New Roman**.
- Apply fonts at the run/style level so mixed Chinese/English/numbers are rendered predictably; do not assume a single East Asia font setting is sufficient.
- Use a clean hierarchy: title, metadata, executive summary, numbered sections, tables, figure/table captions, notes, and references.
- Use readable margins, consistent paragraph spacing, restrained color, and page numbers. Avoid decorative elements that reduce printability.
- Keep tables within page width; repeat header rows and allow row breaks only when readable.
- Put source locations in notes or evidence columns. Preserve units and significant figures.

### Table alignment and visual hierarchy

Treat table alignment as part of the information design, not as a global left-align default.

- Center header cells horizontally and vertically.
- Center the first column when it contains categories, priorities, statuses, labels, short item names, or other classification values; keep long explanatory first-column text left-aligned.
- Center short body values when the cell is a compact label, number, unit, date, status, score, or one short phrase. “Short” is a judgment based on fit and readability; a practical default is roughly one line or at most 12 Chinese characters/words.
- Keep narrative, evidence, caveat, method, and recommendation cells left-aligned and vertically centered unless top alignment is clearly better for a very long multi-line cell.
- Vertical centering is the default for all cells. Do not leave short labels pinned to the upper-left corner.
- Use deliberate column widths: compact columns for item number, type, status, priority, and result; wider columns for evidence and interpretation. Do not use equal-width columns when the content roles differ.
- Add cell padding and light gray borders. Use a consistent header fill and restrained alternating row shading. Do not merge cells merely to force a visual center; merge only when a grouped header has a clear semantic meaning.
- When a table mixes short labels and long explanations, align each cell by role rather than aligning the entire row uniformly. The goal is that short labels occupy the visual center of their cells while evidence remains easy to scan.

### Required report packaging

For one paper, create one report named `Paperzh_<short-title>_<mode>.docx`.

For a batch, create at least one master report named `Paperzh_batch_<topic>_flash.docx` containing the comparison matrix, per-paper cards, cross-paper synthesis, and Deep-priority queue. If the user asks for individual files, add one DOCX per paper; do not replace the master report with separate files only.

Every report must include:

1. source metadata and review mode;
2. evidence scope and missing-material note;
3. executive summary;
4. mode-specific analysis;
5. explicit vulnerabilities;
6. explicit scenario boundaries;
7. explicit concept-quantification check;
8. research value and next actions;
9. references/evidence locations;
10. a short quality note stating what was and was not independently verified.

See [references/docx-spec.md](references/docx-spec.md) for a compact style and verification checklist.

## Quality control before handoff

Run a final checklist before claiming completion:

- The selected mode is clearly stated and the report contains all required sections for that mode.
- Every major conclusion has a source location or is labeled as inference.
- Flash reports answer: what the author did, vulnerabilities, scenario limits, quantification, and next value.
- Deep reports include the three layers, key figures/tables/formulas, evidence chain, critique, and prioritized transfer plan.
- Working fluid, operating conditions, geometry, scale, and boundary conditions are not silently omitted when relevant.
- Conceptual claims are checked for definition, metric, computation/measurement, criterion, and evidence.
- Unknowns are not presented as facts; author limitations and reviewer findings are separated.
- The DOCX opens successfully, has the required fonts/styles, readable tables, stable page breaks, and no placeholder text.
- Batch comparisons use normalized terms and identify non-comparable metrics.
- The final response links to the generated DOCX file(s) and briefly states the mode, evidence scope, and any remaining limitation.

## Supporting references

Read only the references relevant to the current task:

- [references/flash-mode.md](references/flash-mode.md) — Flash card, comparison matrix, and fast triage procedure.
- [references/deep-mode.md](references/deep-mode.md) — Deep evidence chain, figure/table/formula reading, and research-transfer schema.
- [references/docx-spec.md](references/docx-spec.md) — DOCX structure, typography, naming, and verification requirements.


