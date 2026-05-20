---
name: wa-algona-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Algona Municipal Court local court rules. Triggers on local-rule citations attached to Algona (King County). NOTE: Algona Municipal Court shares its rules document with King County District Court (and 1 other municipal court: Pacific). Do NOT use for other WA jurisdictions outside this shared set, state-level rules, RCW, or WAC.
---

# Algona Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/17/DIS/LCR_King_DIS.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Shared rules document

Algona Municipal Court does not publish a municipal-specific local rules document. AOC routes Algona Municipal Court to the King County District Court rules — the same PDF covers Algona, Pacific. The content of `rules.md` is that shared document verbatim.

## Files

```
algona-municipal/
├── README.md   ← you are here
└── rules.md    ← shared King County District Court rules
```

## Looking up a rule

```bash
grep -n -A 60 -E 'LCR ?[0-9]+' rules.md
```

## Citation format

- `LARLJ 0.1 (as applied to Algona Municipal Court via King County District Court rules)`
- Citation prefixes used in the shared document: LARLJ / LCRLJ / LCrRLJ / LIRLJ

## Caveats

- **Shared document.** This file is the King County District Court rules. The rules apply identically to Algona Municipal Court via AOC routing.
- None observed in spot-check beyond ordinary line-wrap from PDF text extraction.
