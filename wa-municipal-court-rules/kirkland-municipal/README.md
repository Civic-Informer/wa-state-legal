---
name: wa-kirkland-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Kirkland Municipal Court local court rules. Triggers on `KMCLR`, `KMCLIR`, `KMCLGR` citations attached to Kirkland. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Kirkland Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/17/MUN/Kirkland/LCR_Kirkland_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Files

```
kirkland-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (20 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '(KMCLR|KMCLIR|KMCLGR) ?[0-9]+' rules.md
```

## Citation format

- `KMCLR 7`

## Caveats

- None observed in spot-check.
