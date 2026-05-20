---
name: wa-edmonds-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Edmonds Municipal Court local court rules. Triggers on `EDM-IRLJ` citations attached to Edmonds. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Edmonds Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/31/MUN/Edmonds/LCR_Edmonds_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Files

```
edmonds-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (21 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'EDM\-IRLJ ?[0-9]+' rules.md
```

## Citation format

- `EDM-IRLJ 7`

## Caveats

- None observed in spot-check.
