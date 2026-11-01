# DOCX specification reference

## Required styles

Create or reuse named styles so the document remains editable:

| Style role | Chinese font | Latin/numbers | Suggested use |
|---|---|---|---|
| Title/Heading | SimHei | Times New Roman | Report title and section headings |
| Body | SimSun | Times New Roman | Chinese prose, notes, evidence explanations |
| Table text | SimSun | Times New Roman | Comparison matrices and evidence tables |
| Caption | SimSun | Times New Roman | Figure/table captions |
| Equation/technical | SimSun or a compatible math font | Times New Roman for variables | Equations and symbol explanations |

When a run contains mixed scripts, set East Asia and ASCII font properties explicitly if the document library supports them. Check the rendered result rather than trusting the style name.

## Default report profile

Use the original Paperzh research-report layout by default. It is a clean blue-gray analytical report, not a graduation thesis, school template, journal template, or institutional archive package.

- Use A4 portrait unless wide comparison tables clearly require a different page orientation for selected sections.
- Choose readable, balanced margins rather than fixed school-specific values.
- Use a white page, dark blue-gray title/heading hierarchy, light blue-gray table headers and callout boxes, restrained borders, and ample whitespace.
- Start the cover directly with the report identity, title, mode, source metadata, and evidence scope. The cover must not contain a running header or any school/institution/thesis header above the title.
- On content pages only, a small right-aligned running header such as `PAPERZH READING | DEEP MODE` or `PAPERZH READING | FLASH MODE` may be used when it matches the layout; omit it if it makes the page busier.
- Use a simple centered page number and compact section transitions. Do not create thesis-style chapter-opening blank space.
- Use page numbers and stable section breaks when the report length benefits from them.
- Number figures, tables, and equations consistently within the report; use chapter-based numbering only when the requested document structure actually has chapters.
- Preserve the requested Chinese and Latin fonts while allowing Word's mathematics font for native equation structures.

Never add school names, institutional thesis headers, thesis margins, administrative pages, or archive structure unless the user explicitly requests that exact template for the current deliverable. If the user supplies a template, apply it as a task-specific override; do not turn that one-off template into the skill's permanent default.

## Table alignment rules

Tables should be visually hierarchical and role-aware:

- Header cells: horizontal center and vertical center.
- First-column category cells: horizontal center and vertical center when they are short labels, priorities, statuses, or item names.
- Short values: center them in both directions when they fit on one line or are otherwise compact.
- Long narrative cells: left-align horizontally and center vertically; use top alignment only when a long multi-line cell is easier to compare that way.
- Use compact widths for type, status, priority, year, number, and result columns; reserve wider columns for evidence and interpretation.
- Add readable cell padding, light gray borders, a consistent header fill, and restrained alternating row shading.
- Never force a centered appearance by merging unrelated cells. Merge only semantically grouped headers.

## Equation formatting rules

Read [equation-format.md](equation-format.md) before authoring or revising any report that contains equations or formula-definition tables.

- Display equations, formula-only cells, and mathematical relationships embedded in prose, bullets, captions, or mixed-content cells must use native editable Word math (OMML) in Professional layout when they contain fractions, roots, scripts, vectors, absolute values, or chained relations.
- Use stacked fractions for true mathematical division, including inline formulas. Plain slash notation is reserved for units, URLs/DOIs, ordinary prose separators, and explicit lists; rewrite ambiguous list shorthand rather than formatting it as a fraction.
- Use structured radicals, superscripts, subscripts, delimiters, Greek symbols, vectors, and matrices rather than linear-text approximations.
- Center formula-only cells horizontally and vertically, preserve comfortable padding, and allow rows to grow.
- Keep equation numbers at the right margin under the active numbering profile. For wrapped equations, put the number on the final line.
- Run a residual linear-math audit over paragraphs and all table cells, then verify both structure and rendering: confirm native math objects remain in the DOCX and inspect every equation-bearing page for clipping, flattening, missing glyphs, incorrect scripts, and insufficient inline line height.

## Minimal document structure

1. Title and review mode.
2. Source metadata and evidence scope.
3. Executive summary.
4. Main analysis (Flash card/comparison or Deep three layers).
5. Vulnerabilities and scenario limits.
6. Concept quantification.
7. Research transfer and priorities.
8. References/evidence locations.
9. Quality note and unresolved unknowns.

## Verification

Before handoff:

- confirm the file is a valid `.docx` package and opens;
- confirm no `[TODO]`, placeholder, or empty required section remains;
- inspect every page for final delivery, with particular attention to the first page, dense tables, every equation-bearing page, and the final page;
- check heading hierarchy, page numbers, table width, row splitting, figure captions, units, equation readability, native editability, and Professional fraction/root/script layout;
- verify Chinese headings/body and English/numbers use the requested fonts;
- ensure the filename identifies paper/topic and mode;
- keep the source PDF/HTML separate from the final DOCX unless the user requested an appendix.

## Suggested metadata block

```text
阅读模式：Flash / Deep
论文数量：
证据范围：全文 / 摘要 / 截取内容 / 多源材料
审阅日期：YYYY-MM-DD
证据限制：
```


