---
name: wa-lynnwood-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Lynnwood Municipal Court local court rules. Triggers on `LIRLJ`, `LGR` citations attached to Lynnwood. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Lynnwood Municipal Court Local Court Rules

**Source:** https://www.lynnwoodwa.gov/files/sharedassets/public/municipal-court/lmclocalcourtrule.revised2019.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Files

```
lynnwood-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (7 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '(LIRLJ|LGR) ?[0-9]+' rules.md
```

## Citation format

- `LIRLJ 7`

## Caveats

- Hosted by city of Lynnwood, not WA AOC.
