---
name: wa-bainbridge-island-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Bainbridge Island Municipal Court local court rules. Triggers on `LARLJ`, `LIRLJ`, `LCrRLJ` citations attached to Bainbridge Island. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Bainbridge Island Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/18/MUN/Bainbridge_Island/LCR_Bainbridge_Island_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Files

```
bainbridge-island-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (4 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '(LARLJ|LIRLJ|LCrRLJ) ?[0-9]+' rules.md
```

## Citation format

- `LARLJ 7`

## Caveats

- None observed in spot-check.
