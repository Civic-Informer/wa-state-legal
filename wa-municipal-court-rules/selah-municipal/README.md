---
name: wa-selah-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Selah Municipal Court local court rules. Triggers on SEMAR, SEMCrR, SEMIR citations attached to Selah. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Selah Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/39/MUN/Selah/LCR_Selah_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. OCR-derived from image-only PDF; rule headings and body text are present, but the table of contents has heavy whitespace artifacts and some character swaps. Rule body sections read cleanly.

## Files

```
selah-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (6 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'SEMAR ?[0-9]+' rules.md
grep -n -A 60 -E 'SEMCrR ?[0-9]+' rules.md
grep -n -A 60 -E 'SEMIR ?[0-9]+' rules.md
```

## Citation format

- `Selah SEMCrR 3.2`

## Caveats

- OCR-derived from image-only PDF; verify exact wording against the source PDF. Table-of-contents columns are visually disordered in the OCR output.
