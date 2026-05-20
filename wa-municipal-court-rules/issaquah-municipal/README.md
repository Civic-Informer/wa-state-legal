---
name: wa-issaquah-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Issaquah Municipal Court local court rules. Triggers on `IMC`, `IMC-CRLJ`, `IMC-IRLJ` citations attached to Issaquah. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Issaquah Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/17/MUN/Issaquah/LCR_Issaquah_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Files

```
issaquah-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (24 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '(IMC|IMC\-CRLJ|IMC\-IRLJ) ?[0-9]+' rules.md
```

## Citation format

- `IMC 7`

## Caveats

- None observed in spot-check.
