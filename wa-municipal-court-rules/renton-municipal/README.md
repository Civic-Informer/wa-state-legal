---
name: wa-renton-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Renton Municipal Court local court rules. Triggers on RMCGR, RMCLR citations attached to Renton. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Renton Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/17/MUN/Renton/LCR_Renton_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule labels, amendment dates, and body text preserved verbatim.

## Files

```
renton-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (26 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'RMCGR ?[0-9]+' rules.md
grep -n -A 60 -E 'RMCLR ?[0-9]+' rules.md
```

## Citation format

- `Renton RMCLR 3.2`

## Caveats

- None observed in spot-check.
