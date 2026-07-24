# STE Rewrite — uW-Tools-Collab docs

**Source:** `unfoldingWord/uW-Tools-Collab` @ `main` (shallow clone)
**Scope:** the `docs/` tree (42 files) plus top-level `README.md` = **43 files**
**Method:** Each file was copied verbatim, then only connected **prose** was rewritten into ASD-STE100 Simplified Technical English (Issue 9) with the `ste-cleardoc` ruleset. Code blocks, YAML, USFM, TSV, tables, mermaid diagrams, headings, frontmatter, URLs, `rc://` links, and resource identifiers were left byte-for-byte unchanged.

## Correctness — structural integrity

An automated check compared every original file against its rewrite:

| Protected content | Files changed |
|---|---:|
| YAML frontmatter | 0 / 43 |
| Headings (TOC anchors) | 0 / 43 |
| Fenced code blocks | 0 / 43 |
| Tables | 0 / 43 |
| URLs + `rc://` links | 0 / 43 |
| Empty/truncated files | 0 / 43 |

**Every code sample, table, diagram, heading, and link is identical to the original.**

## Correctness — meaning fidelity

An independent reviewer diffed a 5-file sample (including the 2,122-line developer guide and the most heavily edited files) to check that no technical fact, number, condition, or instruction changed meaning. Result: facts preserved throughout. Two sentences where hedge-removal had shifted certainty were corrected:

- `1-why...mdx`: "cannot find" → "have difficulty to find" (restored: difficulty, not impossibility).
- `translation-questions...guide.mdx`: "do not apply" → "can be not applicable" (restored: possibility, not assertion).

## Completeness

All 43 target files are present, non-empty, and in their original directory structure. `docs/assets/frontmatter-schema.md` had no connected prose (schema + field list only) and is unchanged by design.

## Readability gain (prose only)

Same measurement pipeline applied before and after.

| Metric | Original | STE rewrite |
|---|---:|---:|
| Flesch Reading Ease | 12.1 | 22.1 |
| Flesch–Kincaid grade | 16.8 | 13.9 |
| Avg. sentence length (words) | 21.2 | 14.9 |

Readability improved in **every** file. Gains are largest in prose-dense guides (e.g. the Scripture Burrito and translation-support guides dropped from ~50-word to ~25-word average sentences) and smallest in heading/link-heavy index pages that contain little connected prose.

## Notes / judgment calls

- STE intensifier removal softened some emphasis words ("much more flexible" → "more flexible", "very natural" → "natural"). Meaning is preserved; degree wording is reduced. Revert individually if you want the emphasis back.
- Decorative words inside **bullet-list fragments** (e.g. "Enhanced …", "Comprehensive …" as list items) were left in place, because the pass targeted full-sentence prose. A second pass can convert those if wanted.
- No blocking `[FLAG]`s were raised by any rewrite pass.
