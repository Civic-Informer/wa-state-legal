---
name: wa-tukwila-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Tukwila Municipal Court local court rules. Triggers on TMCGR, TMCLR, TMCIRLJ citations attached to Tukwila. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Tukwila Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/17/MUN/Tukwila/LCR_Tukwila_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule labels and body text preserved verbatim.

## Files

```
tukwila-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (39 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'TMCGR ?[0-9]+' rules.md
grep -n -A 60 -E 'TMCLR ?[0-9]+' rules.md
grep -n -A 60 -E 'TMCIRLJ ?[0-9]+' rules.md
```

## Citation format

- `Tukwila TMCLR 3.2`

## Caveats

- None observed in spot-check.
