---
name: wac-262-housing-finance-commission
description: Use when the user asks about, cites, or quotes Title 262 of the Washington Administrative Code (HOUSING FINANCE COMMISSION). Triggers on: 'WAC 262', 'Title 262 WAC', 'chapter 262-NN', 'HOUSING FINANCE COMMISSION'. `rules.md` contains the full body text of every section in this Title, sourced from the 2025 archive's per-chapter `COMBINEDCHAPTER.pdf` files. Do NOT use for WAC titles other than 262, for RCW (Revised Code of Washington) statutes, or for federal regulations.
---

# Title 262 WAC — HOUSING FINANCE COMMISSION

**Effective date of this snapshot:** 2026-05-20.

**Fidelity verdict:** FAITHFUL. `rules.md` contains the full body text of every chapter in this Title, converted from the 2025 archive's per-chapter `COMBINEDCHAPTER.pdf` files via `pdftotext -layout` and cleaned (page footers stripped, end-of-line hyphenation rejoined). Spot-check before quoting fee tables or other tabular content — `pdftotext` preserves columns with whitespace alignment but cannot emit GFM tables, so wide tables may wrap awkwardly in the markdown view; the textual data is intact for grep.

## What this corpus contains

This is the on-disk archive of Title 262 WAC (HOUSING FINANCE COMMISSION) from the Washington State Legislature's 2025 WAC Archive. The consolidated `rules.md` contains the **full body text** of every section in every chapter of this Title, ordered by chapter cite.

Each `## WAC 262-NN — CHAPTER NAME` heading is followed by the cleaned plain-text body of that chapter's combined PDF (the same PDF the legislature publishes for download from each chapter's page). Section subheadings appear in the text as the original PDF presented them (e.g. `WAC 262-NN-NNN` followed by section title and body, with statutory-authority history brackets at the end of each section).

Use this corpus to:
- Read the full text of any WAC section in this Title.
- Find which sections exist in a given chapter.
- Trace repeal/recodification history (the disposition tables from each chapter are retained at the end of the chapter text).

## Files

```
262-housing-finance-commission/
├── README.md         <- you are here
├── rules.md          <- full body text of every section in Title 262 (3 chapters, 75,253 bytes)
└── rules.md.toc.bak  <- prior section-index-only `rules.md` (pre-patch) retained for cross-checking
```

## Looking up a chapter or section

```bash
# Jump to a specific chapter
grep -n -A 400 '^## WAC 262-NN ' rules.md  # replace NN with chapter number

# A specific section by full citation
grep -n -B 2 -A 80 'WAC 262-NN-NNN' rules.md  # replace NN-NNN

# All section short titles (cite + first line)
grep -nE '^WAC 262-[0-9A-Z]+-[0-9A-Z]+' rules.md
```

## Citation format

- Title: `Title 262 WAC`
- Chapter: `chapter 262-NN WAC` or `WAC 262-NN`
- Section: `WAC 262-NN-NNN`

## Caveats

- Fee tables, schedules, and other column-aligned tables are preserved as whitespace-aligned text, not as GFM tables. Columns are correct but may be visually offset; data is grep-able and quotable.
- Section subheadings inside chapters are inline with the body text (not separate `###` markdown headings) — they appear as `WAC 262-NN-NNN` lines followed by the section's title and body, as in the source PDF.
- End-of-line hyphenation has been rejoined for lowercase words (e.g. `informa-\ntion` → `information`); a rare compound hyphen broken at the line edge will also be rejoined — acceptable for grep but verify exact spelling against the PDF before block-quoting.
- Per-page `Certified on M/D/YYYY ... Page N` footers were stripped during conversion.
- Snapshot effective date: 2026-05-20. The WAC is amended continuously; for currency-sensitive use, re-verify against the official source.
- This corpus is offline-only. Never refetch from the web.
