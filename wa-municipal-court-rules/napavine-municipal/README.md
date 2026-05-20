---
name: wa-napavine-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Napavine Municipal Court local court rules. Triggers on NMLARLJ citations attached to Napavine. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Napavine Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/21/MUN/Napavine/LCR_Napavine_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Body text, rule numbers, and effective dates preserved.

## Files

```
napavine-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (10 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'NMLARLJ ?[0-9]+' rules.md
```

## Citation format

- `Napavine NMLARLJ 4`

## Caveats

- None observed in spot-check.
