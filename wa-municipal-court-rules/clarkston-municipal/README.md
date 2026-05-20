---
name: wa-clarkston-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Clarkston Municipal Court local court rules. Triggers on `LCRLJ`, `LCrRLJ`, `LIRLJ`, `LARLJ`, `LGRLJ` citations attached to Clarkston. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Clarkston Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/02/DIS/LCR_Asotin_DIS.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Files

```
clarkston-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (8 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '(LCRLJ|LCrRLJ|LIRLJ|LARLJ|LGRLJ) ?[0-9]+' rules.md
```

## Citation format

- `LCRLJ 7`

## Caveats

- None observed in spot-check.
