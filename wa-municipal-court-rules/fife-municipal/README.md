---
name: wa-fife-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Fife Municipal Court local court rules. Triggers on `FMLGR`, `FMLAR`, `FMLIR` citations attached to Fife. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Fife Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/27/MUN/Fife/LCR_Fife_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Files

```
fife-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (5 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '(FMLGR|FMLAR|FMLIR) ?[0-9]+' rules.md
```

## Citation format

- `FMLGR 7`

## Caveats

- None observed in spot-check.
