---
name: wa-sedro-woolley-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Sedro-Woolley Municipal Court local court rules. Triggers on SWMARLJ, SWMCrRLJ, SWMIRLJ citations attached to Sedro-Woolley. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Sedro-Woolley Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/29/MUN/Sedro_Woolley/LCR_SedroWoolley_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule labels and body text preserved verbatim.

## Files

```
sedro-woolley-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (4 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'SWMARLJ ?[0-9]+' rules.md
grep -n -A 60 -E 'SWMCrRLJ ?[0-9]+' rules.md
grep -n -A 60 -E 'SWMIRLJ ?[0-9]+' rules.md
```

## Citation format

- `Sedro-Woolley SWMARLJ 2`

## Caveats

- None observed in spot-check.
