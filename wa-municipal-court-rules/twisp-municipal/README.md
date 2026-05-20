---
name: wa-twisp-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Twisp Municipal Court local court rules. Triggers on TMLRGR, TMLRIRLJ, TMLRGER citations attached to Twisp. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Twisp Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/24/MUN/Twisp/LCR_Twisp_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. OCR-derived from image-only PDF; rule labels (TMLRGR/TMLRIRLJ) and body text survive. Document is short (2 pages).

## Files

```
twisp-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (2 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'TMLRGR ?[0-9]+' rules.md
grep -n -A 60 -E 'TMLRIRLJ ?[0-9]+' rules.md
grep -n -A 60 -E 'TMLRGER ?[0-9]+' rules.md
```

## Citation format

- `Twisp TMLRGR 30`

## Caveats

- OCR-derived from image-only PDF; verify exact wording against the source PDF. The document also shows an OCR variant 'TMLRGER' for 'TMLRGR 7' — treat as same rule.
