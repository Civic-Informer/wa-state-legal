---
name: wa-sunnyside-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Sunnyside Municipal Court local court rules. Triggers on SUMCLR, SUM citations attached to Sunnyside. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Sunnyside Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/39/MUN/Sunnyside/LCR_Sunnyside_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. OCR-derived from image-only PDF. Rule labels and body text survive; OCR has compressed many 'SUMCLR' tokens to 'SUM' in the table of contents and joined some whitespace. Body sections read cleanly.

## Files

```
sunnyside-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (16 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'SUMCLR ?[0-9]+' rules.md
grep -n -A 60 -E 'SUM ?[0-9]+' rules.md
```

## Citation format

- `Sunnyside SUMCLR 3.2`

## Caveats

- OCR-derived from image-only PDF; verify exact wording against the source PDF. The OCR has truncated some rule prefixes (e.g., 'SUMCLR' rendered as 'SUM' in headings).
