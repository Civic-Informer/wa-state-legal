---
name: wa-winlock-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Winlock Municipal Court local court rules. Triggers on WMLARLJ citations attached to Winlock. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Winlock Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/21/MUN/Winlock/LCR_Winlock_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Body text, rule numbers, and effective dates preserved.

## Files

```
winlock-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (10 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'WMLARLJ ?[0-9]+' rules.md
```

## Citation format

- `Winlock WMLARLJ 4`

## Caveats

- The WML- prefix family is shared with Wapato Municipal Court (which uses WMLAR). Always disambiguate by city.
