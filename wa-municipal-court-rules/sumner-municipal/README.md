---
name: wa-sumner-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Sumner Municipal Court local court rules. Triggers on Local Court General Rule, Local Court Rule citations attached to Sumner. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Sumner Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/27/MUN/Sumner/LCR_Sumner_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule headings and body text preserved verbatim.

## Files

```
sumner-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (9 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'Local Court General Rule [0-9]+' rules.md
grep -n -A 60 -E 'Local Court Rule [0-9]+' rules.md
```

## Citation format

- `Sumner Local Court General Rule 1`

## Caveats

- Sumner uses written-out labels ('Local Court General Rule 1', 'Local Court Rule 3', etc.) rather than an abbreviated prefix. Search by full phrase or rule number.
