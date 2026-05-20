---
name: wa-airway-heights-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Airway Heights Municipal Court local court rules. Triggers on `AWHGR`, `AWHCR`, `AWHCRLJ`, `AWHIRLJ` citations attached to Airway Heights. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Airway Heights Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/32/MUN/Airway_Heights/LCR_Airway_Heights_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Files

```
airway-heights-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (38 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '(AWHGR|AWHCR|AWHCRLJ|AWHIRLJ) ?[0-9]+' rules.md
```

## Citation format

- `AWHGR 7`

## Caveats

- None observed in spot-check.
