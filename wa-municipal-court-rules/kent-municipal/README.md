---
name: wa-kent-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Kent Municipal Court local court rules. Triggers on `KMC-GR`, `KMC-CRLJ`, `KMC-CrRLJ`, `KMC-IRLJ` citations attached to Kent. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Kent Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/17/MUN/Kent/LCR_Kent_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Files

```
kent-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (16 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '(KMC\-GR|KMC\-CRLJ|KMC\-CrRLJ|KMC\-IRLJ) ?[0-9]+' rules.md
```

## Citation format

- `KMC-GR 7`

## Caveats

- None observed in spot-check.
