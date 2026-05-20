---
name: wa-gig-harbor-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Gig Harbor Municipal Court local court rules. Triggers on `LGR`, `LAR`, `LIRLJ` citations attached to Gig Harbor. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Gig Harbor Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/27/MUN/Gig_Harbor/LCR_Gig_Harbor_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Files

```
gig-harbor-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (18 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '(LGR|LAR|LIRLJ) ?[0-9]+' rules.md
```

## Citation format

- `LGR 7`

## Caveats

- None observed in spot-check.
