---
name: wa-east-wenatchee-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares East Wenatchee Municipal Court local court rules. Triggers on `EWMCLGR`, `EWMCLR`, `EWMCLIR` citations attached to East Wenatchee. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# East Wenatchee Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/09/MUN/EastWenatchee/LCR_East_Wenatchee_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Rule text and headings preserved verbatim; minor layout flattening only.

## Files

```
east-wenatchee-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (15 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '(EWMCLGR|EWMCLR|EWMCLIR) ?[0-9]+' rules.md
```

## Citation format

- `EWMCLGR 7`

## Caveats

- Tabular/columnar layouts (calendars, signature blocks) are flattened to plain text.
