---
name: wa-centralia-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Centralia Municipal Court local court rules. Triggers on local-rule references for Centralia where rules are numbered without a citation prefix (e.g. "Rule 7" or "Local Rule 3" attached to Centralia). Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Centralia Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/21/MUN/Centralia/LCR_Centralia_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Source PDF is a scanned image; text reconstructed via tesseract OCR. Rule numbering and headings preserved; expect occasional character-level OCR errors.

## Files

```
centralia-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (1 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'Rule ?[0-9]+' rules.md
```

## Citation format

- `Centralia Municipal Court Local Rule 7`

## Caveats

- Source PDF is image-only (scanned) — text recovered via tesseract OCR.
- Sporadic OCR transcription errors are possible; quote with the source PDF open for critical text.
