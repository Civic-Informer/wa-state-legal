---
name: wa-puyallup-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Puyallup Municipal Court local court rules. Triggers on PUMCLR citations attached to Puyallup. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Puyallup Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/27/MUN/Puyallup/LCR_Puyallup_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule labels and body text preserved verbatim.

## Files

```
puyallup-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (7 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'PUMCLR ?[0-9]+' rules.md
```

## Citation format

- `Puyallup PUMCLR 3.1`

## Caveats

- None observed in spot-check.
