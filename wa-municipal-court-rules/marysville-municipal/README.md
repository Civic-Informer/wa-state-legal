---
name: wa-marysville-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Marysville Municipal Court local court rules. Triggers on `MMCLCR`, `MMCLIR` citations attached to Marysville. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Marysville Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/31/MUN/Marysville/LCR_Marysville_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Files

```
marysville-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (13 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '(MMCLCR|MMCLIR) ?[0-9]+' rules.md
```

## Citation format

- `MMCLCR 7`

## Caveats

- None observed in spot-check.
