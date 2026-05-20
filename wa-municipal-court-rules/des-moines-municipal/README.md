---
name: wa-des-moines-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Des Moines Municipal Court local court rules. Triggers on `DMMCLGR`, `DMMCLR`, `DMMCLIR` citations attached to Des Moines. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Des Moines Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/17/MUN/Des_Moines/LCR_Des_Moines_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Files

```
des-moines-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (18 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '(DMMCLGR|DMMCLR|DMMCLIR) ?[0-9]+' rules.md
```

## Citation format

- `DMMCLGR 7`

## Caveats

- None observed in spot-check.
