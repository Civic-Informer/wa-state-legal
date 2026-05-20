---
name: wa-maple-valley-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Maple Valley Municipal Court local court rules. Triggers on `MVMCLR`, `MVMCIRLJ` citations attached to Maple Valley. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Maple Valley Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/17/MUN/Maple_Valley/LCR_Maple_Valley_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Files

```
maple-valley-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (3 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '(MVMCLR|MVMCIRLJ) ?[0-9]+' rules.md
```

## Citation format

- `MVMCLR 7`

## Caveats

- None observed in spot-check.
