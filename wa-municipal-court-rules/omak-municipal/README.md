---
name: wa-omak-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Omak Municipal Court local court rules. Triggers on OMLRGR, OMLRIRLJ citations attached to Omak. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Omak Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/24/MUN/Omak/LCR_Omak_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. OCR-derived from image-only PDF; rule labels and body text survive with minor OCR artifacts.

## Files

```
omak-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (2 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'OMLRGR ?[0-9]+' rules.md
grep -n -A 60 -E 'OMLRIRLJ ?[0-9]+' rules.md
```

## Citation format

- `Omak OMLRGR 7`

## Caveats

- OCR-derived from image-only PDF; verify exact wording against the source PDF.
