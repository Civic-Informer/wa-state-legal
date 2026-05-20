---
name: wa-wapato-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Wapato Municipal Court local court rules. Triggers on WMLAR, WMLCrR, WMLIR citations attached to Wapato. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Wapato Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/39/MUN/Wapato/LCR_Wapato_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule labels and body text preserved verbatim.

## Files

```
wapato-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (8 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'WMLAR ?[0-9]+' rules.md
grep -n -A 60 -E 'WMLCrR ?[0-9]+' rules.md
grep -n -A 60 -E 'WMLIR ?[0-9]+' rules.md
```

## Citation format

- `Wapato WMLAR 1.3`

## Caveats

- The WML- prefix family is shared with Winlock Municipal Court (which uses WMLARLJ). Always disambiguate by city.
