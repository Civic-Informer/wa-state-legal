---
name: wa-black-diamond-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Black Diamond Municipal Court local court rules. Triggers on `BDMCLR`, `BDMCLC-IRLJ` citations attached to Black Diamond. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Black Diamond Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/17/MUN/Black_Diamond/LCR_Black_Diamond_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Source PDF is a scanned image; text reconstructed via tesseract OCR. Rule numbering and headings preserved; expect occasional character-level OCR errors.

## Files

```
black-diamond-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (20 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '(BDMCLR|BDMCLC\-IRLJ) ?[0-9]+' rules.md
```

## Citation format

- `BDMCLR 7`

## Caveats

- Source PDF is image-only (scanned) — text recovered via tesseract OCR.
- Sporadic OCR transcription errors are possible; quote with the source PDF open for critical text.
