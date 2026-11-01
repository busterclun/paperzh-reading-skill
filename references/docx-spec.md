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

## School-format overlay

For the user's graduation-design/thesis-formatted Word deliverables, apply [thesis-format-bit-mechanical-2022.md](thesis-format-bit-mechanical-2022.md). The key non-negotiable values are:

- A4 portrait; margins top 3.5 cm, bottom 2.6 cm, left 3.0 cm, right 2.6 cm.
- Header 2.4 cm, footer 2.0 cm, gutter 0.
- Header text `北京理工大学本科生毕业设计（论文）`, SimSun 14 pt, centered, character spacing +0.5 pt.
- Footer page number, SimSun 10.5 pt, centered.
- Chapter heading SimHei 16 pt bold centered; level 2 SimHei 14 pt bold left; level 3 SimHei 12 pt bold left.
- Body SimSun 12 pt with fixed 22 pt line spacing and no paragraph spacing before/after.
- Chapter-based numbering for figures, tables, and equations; captions/titles SimSun 10.5 pt centered; GB/T 7714—2015 references.

Do not invent a cover, task book, evaluation form, declaration, or other administrative page when producing a paper-reading report. Add those pages only when the user provides or explicitly requests the thesis package template.

## Table alignment rules

Tables should be visually hierarchical and role-aware:

- Header cells: horizontal center and vertical center.
- First-column category cells: horizontal center and vertical center when they are short labels, priorities, statuses, or item names.
- Short values: center them in both directions when they fit on one line or are otherwise compact.
- Long narrative cells: left-align horizontally and center vertically; use top alignment only when a long multi-line cell is easier to compare that way.
- Use compact widths for type, status, priority, year, number, and result columns; reserve wider columns for evidence and interpretation.
- Add readable cell padding, light gray borders, a consistent header fill, and restrained alternating row shading.
- Never force a centered appearance by merging unrelated cells. Merge only semantically grouped headers.

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
- inspect at least the first page, a dense table page, and the final page;
- check heading hierarchy, page numbers, table width, row splitting, figure captions, units, and equation readability;
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


