---
name: wa-milton-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Milton Municipal Court local court rules. Triggers on LAR, LGR, LCrRLJ, LIRLJ citations attached to Milton. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Milton Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/27/MUN/Milton/LCR_Milton_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Body text, rule numbers, and amendment dates preserved verbatim.

## Files

```
milton-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (13 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'LAR ?[0-9]+' rules.md
grep -n -A 60 -E 'LGR ?[0-9]+' rules.md
grep -n -A 60 -E 'LCrRLJ ?[0-9]+' rules.md
```

## Citation format

- `Milton LCrRLJ 3.1`

## Caveats

- None observed in spot-check.
