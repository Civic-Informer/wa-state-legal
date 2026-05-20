---
name: wa-sumas-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Sumas Municipal Court local court rules. Triggers on SMMGR, SMMCrRLJ, SMMIRLJ citations attached to Sumas. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Sumas Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/37/MUN/Sumas/LCR_Sumas_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule labels, numbering, and body text preserved verbatim.

## Files

```
sumas-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (6 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'SMMGR ?[0-9]+' rules.md
grep -n -A 60 -E 'SMMCrRLJ ?[0-9]+' rules.md
grep -n -A 60 -E 'SMMIRLJ ?[0-9]+' rules.md
```

## Citation format

- `Sumas SMMGR 30(d)`

## Caveats

- None observed in spot-check.
