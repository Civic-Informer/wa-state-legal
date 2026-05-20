---
name: wa-olympia-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Olympia Municipal Court local court rules. Triggers on OMCLR citations attached to Olympia. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Olympia Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/34/MUN/Olympia/LCR_Olympia_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule labels, amendment dates, and body text preserved verbatim.

## Files

```
olympia-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (6 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'OMCLR ?[0-9]+' rules.md
```

## Citation format

- `Olympia OMCLR 3`

## Caveats

- None observed in spot-check.
