---
name: wa-bothell-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Bothell Municipal Court local court rules. Triggers on `BMCLR`, `BMCLIR` citations attached to Bothell. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Bothell Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/17/MUN/Bothell/LCR_Bothell_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Source PDF is a scanned image; text reconstructed via tesseract OCR. Rule numbering and headings preserved; expect occasional character-level OCR errors.

## Files

```
bothell-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (18 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '(BMCLR|BMCLIR) ?[0-9]+' rules.md
```

## Citation format

- `BMCLR 7`

## Caveats

- Source PDF is image-only (scanned) — text recovered via tesseract OCR.
- Sporadic OCR transcription errors are possible; quote with the source PDF open for critical text.
