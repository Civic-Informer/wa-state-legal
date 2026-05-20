---
name: wa-langley-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Langley Municipal Court local court rules. Triggers on local-rule citations attached to Langley (Island County). NOTE: Langley Municipal Court shares its rules document with Island County District Court (and 2 other municipal courts: Coupeville, Oak Harbor). Do NOT use for other WA jurisdictions outside this shared set, state-level rules, RCW, or WAC.
---

# Langley Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/15/DIS/LCR_Island_DIS.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** OCR-RECONSTRUCTED. Source PDF was a scanned image with no embedded text; rules.md was produced via Tesseract OCR. Rule numbering, structure, and substantive text are preserved, but expect occasional OCR artifacts (misread punctuation, stray diacritics, the letter `l`/`1` confusions). Always confirm exact wording against the source PDF before quoting.

## Shared rules document

Langley Municipal Court does not publish a municipal-specific local rules document. AOC routes Langley Municipal Court to the Island County District Court rules — the same PDF covers Coupeville, Langley, Oak Harbor. The content of `rules.md` is that shared document verbatim.

## Files

```
langley-municipal/
├── README.md   ← you are here
└── rules.md    ← shared Island County District Court rules
```

## Looking up a rule

```bash
grep -n -A 60 -E 'LCR ?[0-9]+' rules.md
```

## Citation format

- `Island County LARLJ (as applied to Langley Municipal Court)`
- Citation prefixes used in the shared document: Island County District Court Local Rules (LARLJ / LCRLJ / LCrRLJ / LIRLJ)

## Caveats

- **Shared document.** This file is the Island County District Court rules. The rules apply identically to Langley Municipal Court via AOC routing.
- OCR-derived text. The cover page of the source PDF explicitly states the document `ALSO INCLUDES THE CITIES OF OAK HARBOR, COUPEVILLE, AND LANGLEY MUNICIPAL COURTS`, so the shared scope is confirmed in the document itself.
