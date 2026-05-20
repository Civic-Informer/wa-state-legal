---
name: wa-yakima-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Yakima Municipal Court local court rules. Triggers on YMLAR, YMLCrR, YMLIR citations attached to Yakima. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Yakima Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/39/MUN/Yakima/LCR_Yakima_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule labels and body text preserved verbatim.

## Files

```
yakima-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (31 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'YMLAR ?[0-9]+' rules.md
grep -n -A 60 -E 'YMLCrR ?[0-9]+' rules.md
grep -n -A 60 -E 'YMLIR ?[0-9]+' rules.md
```

## Citation format

- `Yakima YMLCrR 3.2`

## Caveats

- None observed in spot-check.
