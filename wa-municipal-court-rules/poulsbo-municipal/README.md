---
name: wa-poulsbo-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Poulsbo Municipal Court local court rules. Triggers on LCrRLJ, LIRLJ, LCRRLJ, LARLJ citations attached to Poulsbo. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Poulsbo Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/18/MUN/Poulsbo/LCR_Poulsbo_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Body text and rule labels preserved verbatim.

## Files

```
poulsbo-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (14 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'LCrRLJ ?[0-9]+' rules.md
grep -n -A 60 -E 'LIRLJ ?[0-9]+' rules.md
grep -n -A 60 -E 'LCRRLJ ?[0-9]+' rules.md
```

## Citation format

- `Poulsbo LCrRLJ 3.2.2`

## Caveats

- Rules cite bare state-rule prefixes (LCrRLJ, LIRLJ, LARLJ) with no Poulsbo-specific abbreviation; the prefix alone does not distinguish Poulsbo from other municipal courts using the same form. Always cite as 'Poulsbo LCrRLJ X.Y'.
