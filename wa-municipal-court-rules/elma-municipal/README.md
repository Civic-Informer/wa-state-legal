---
name: wa-elma-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Elma Municipal Court local court rules. Triggers on local-rule references for Elma where rules are numbered without a citation prefix (e.g. "Rule 7" or "Local Rule 3" attached to Elma). Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Elma Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/14/MUN/Elma/LCR_Elma_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Files

```
elma-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (7 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'Rule ?[0-9]+' rules.md
```

## Citation format

- `Elma Municipal Court Local Rule 7`

## Caveats

- None observed in spot-check.
