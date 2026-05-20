---
name: rcw-title-28a
description: Use when the user asks about, cites, quotes, or compares Title 28A RCW — K-12 common schools — districts, school boards, certification, curriculum, levies, learning assistance, school safety. Triggers on citations like `RCW 28A.`, chapter cites within Title 28A, and subject keywords drawn from the chapter list inside `rules.md`. Do NOT use for: WAC regulations, court rules, federal law, or matters governed by other RCW Titles.
---

# Title 28A RCW — COMMON SCHOOL PROVISIONS

**Effective date of this snapshot:** 2026-05-20 (Washington State Legislature
2025 RCW Archive; individual chapters certified by the legislature on the
dates that appear in the source PDF page footers, typically mid-2024 to
mid-2025).

**Fidelity verdict:** FAITHFUL. Spot-check confirmed body statute text, subsection lettering, and history-note brackets are preserved cleanly from the source PDF.

## Files

```
28A-common-school-provisions/
├── README.md   ← you are here
└── rules.md    ← consolidated text of every chapter in Title 28A (76 chapters, 3,513,679 bytes)
```

## Looking up a chapter or section

```bash
# Jump to a specific chapter heading
grep -n -E '^## RCW 28A\.' rules.md

# Pull a specific section's body (typically 30-90 lines)
grep -n -A 60 -E 'RCW\s+28A\.[0-9]+[A-Z]?[.-][0-9]+' rules.md | head -80

# Search for a term within this Title only
grep -ni 'KEYWORD' rules.md
```

## Citation format

- Chapter: `RCW 28A.NN`
- Section: `RCW 28A.NN.MMM`
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
