---
name: wa-winthrop-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Winthrop Municipal Court local court rules. Triggers on WMLRGR, WMLRIRLJ, WMLRGER citations attached to Winthrop. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Winthrop Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/24/MUN/Winthrop/LCR_Winthrop_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. OCR-derived from image-only PDF; rule labels and body text survive. Document is short (2 pages).

## Files

```
winthrop-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (2 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'WMLRGR ?[0-9]+' rules.md
grep -n -A 60 -E 'WMLRIRLJ ?[0-9]+' rules.md
grep -n -A 60 -E 'WMLRGER ?[0-9]+' rules.md
```

## Citation format

- `Winthrop WMLRGR 30`

## Caveats

- OCR-derived from image-only PDF; verify exact wording against the source PDF. OCR variant 'WMLRGER' appears alongside 'WMLRGR' for rule 7 — same rule.
