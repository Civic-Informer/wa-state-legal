---
name: rcw-title-50a
description: Use when the user asks about, cites, quotes, or compares Title 50A RCW — Washington Paid Family and Medical Leave. Triggers on citations like `RCW 50A.`, chapter cites within Title 50A, and subject keywords drawn from the chapter list inside `rules.md`. Do NOT use for: WAC regulations, court rules, federal law, or matters governed by other RCW Titles.
---

# Title 50A RCW — FAMILY AND MEDICAL LEAVE

**Effective date of this snapshot:** 2026-05-20 (Washington State Legislature
2025 RCW Archive; individual chapters certified by the legislature on the
dates that appear in the source PDF page footers, typically mid-2024 to
mid-2025).

**Fidelity verdict:** FAITHFUL. Spot-check confirmed body statute text, subsection lettering, and history-note brackets are preserved cleanly from the source PDF.

## Files

```
50A-family-and-medical-leave/
├── README.md   ← you are here
└── rules.md    ← consolidated text of every chapter in Title 50A (11 chapters, 243,359 bytes)
```

## Looking up a chapter or section

```bash
# Jump to a specific chapter heading
grep -n -E '^## RCW 50A\.' rules.md

# Pull a specific section's body (typically 30-90 lines)
grep -n -A 60 -E 'RCW\s+50A\.[0-9]+[A-Z]?[.-][0-9]+' rules.md | head -80

# Search for a term within this Title only
grep -ni 'KEYWORD' rules.md
```

## Citation format

- Chapter: `RCW 50A.NN`
- Section: `RCW 50A.NN.MMM`
- History note: appears in brackets after each section, e.g.
  `[2022 c 268 s 32; 2021 c 215 s 89; 1996 c 134 s 7; ...]`

## Caveats

- **Body source is the combined Title PDF**, not the per-chapter HTML.
  The Legislature's per-chapter HTML pages contain only section TOCs and
  chapter notes — the actual statute body lives only in the combined PDFs.
- `pdftotext -layout` preserves columns and indentation, but does not
  produce pipe-tables. Wherever the source has tabular data, the converted
  form is space-aligned text.
- Per-page footers (`Certified on M/D/YYYY  Combined Chapter X.NN RCW
  Page N`) have been stripped during cleanup. The certification date for
  each chapter is recoverable from the source PDF if needed.
- Hyphenated line-breaks have been re-joined (`docu-\nment` → `document`);
  intentional hyphens (`long-term`, `quasi-municipal`) are preserved.
- Em-dashes appear as the literal Unicode character `—`, not as `--`.
- This snapshot does not include WAC implementing regulations or court
  decisions interpreting the statutes; those are out of scope.
