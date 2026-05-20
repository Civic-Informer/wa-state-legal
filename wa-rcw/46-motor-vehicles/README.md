---
name: rcw-title-46
description: Use when the user asks about, cites, quotes, or compares Title 46 RCW — motor vehicles — driver licensing, vehicle registration, rules of the road (RCW 46.61), traffic infractions, DUI. Triggers on citations like `RCW 46.`, chapter cites within Title 46, and subject keywords drawn from the chapter list inside `rules.md`. Do NOT use for: WAC regulations, court rules, federal law, or matters governed by other RCW Titles.
---

# Title 46 RCW — MOTOR VEHICLES

**Effective date of this snapshot:** 2026-05-20 (Washington State Legislature
2025 RCW Archive; individual chapters certified by the legislature on the
dates that appear in the source PDF page footers, typically mid-2024 to
mid-2025).

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Body statute text reads cleanly; tabular content (rate tables, fee schedules, multi-column listings) is preserved as space-aligned text rather than pipe-tables, so it is grep-able but not parseable as structured data.

## Files

```
46-motor-vehicles/
├── README.md   ← you are here
└── rules.md    ← consolidated text of every chapter in Title 46 (54 chapters, 3,549,830 bytes)
```

## Looking up a chapter or section

```bash
# Jump to a specific chapter heading
grep -n -E '^## RCW 46\.' rules.md

# Pull a specific section's body (typically 30-90 lines)
grep -n -A 60 -E 'RCW\s+46\.[0-9]+[A-Z]?[.-][0-9]+' rules.md | head -80

# Search for a term within this Title only
grep -ni 'KEYWORD' rules.md
```

## Citation format

- Chapter: `RCW 46.NN`
- Section: `RCW 46.NN.MMM`
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
