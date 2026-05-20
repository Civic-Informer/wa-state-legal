---
name: wa-pasco-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Pasco Municipal Court local court rules. Triggers on PMCLR, LIRLJ citations attached to Pasco. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Pasco Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/11/MUN/Pasco/LCR_Pasco_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. OCR-derived from image-only PDF. Rule headings and body text are present; minor OCR artifacts (occasional letter swaps, spacing) appear.

## Files

```
pasco-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (6 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'PMCLR ?[0-9]+' rules.md
grep -n -A 60 -E 'LIRLJ ?[0-9]+' rules.md
```

## Citation format

- `Pasco PMCLR 3.3`

## Caveats

- OCR-derived from image-only PDF; verify exact wording against the source PDF. Some rules cite the bare LIRLJ form (state infraction rule) rather than a Pasco-prefixed form.
