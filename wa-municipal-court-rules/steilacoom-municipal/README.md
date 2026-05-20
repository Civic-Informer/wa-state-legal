---
name: wa-steilacoom-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Steilacoom Municipal Court local court rules. Triggers on local-rule citations attached to Steilacoom (Pierce County). NOTE: Steilacoom Municipal Court shares its rules document with Lakewood Municipal Court (and 1 other municipal court: DuPont). Do NOT use for other WA jurisdictions outside this shared set, state-level rules, RCW, or WAC.
---

# Steilacoom Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/27/MUN/Lakewood/LCR_Lakewood_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL-WITH-OCR-ARTIFACTS. Source PDF was produced by a Canon scanner with embedded OCR; the PDF text layer contains occasional character substitutions baked in at scan time (e.g. `rABLE OF CONTENTS`, `LI\4CLR` for `LMCLR`, `t.2` for `1.2`, `Defin itio n s`). Rule numbering, structure, and substantive text are preserved; quote with care.

## Shared rules document

Steilacoom Municipal Court does not publish a municipal-specific local rules document. AOC routes Steilacoom Municipal Court to the Lakewood Municipal Court rules — the same PDF covers DuPont, Lakewood, Steilacoom. The content of `rules.md` is that shared document verbatim.

## Files

```
steilacoom-municipal/
├── README.md   ← you are here
└── rules.md    ← shared Pierce County Lakewood Municipal Court rules
```

## Looking up a rule

```bash
grep -n -A 60 -E 'LCR ?[0-9]+' rules.md
```

## Citation format

- `LMCLR GR 1.1 (Lakewood Municipal Court Local Rules, as applied to Steilacoom Municipal Court)`
- Citation prefixes used in the shared document: LMCLR (Lakewood Municipal Court Local Rules)

## Caveats

- **Shared document.** This file is the Pierce County's Lakewood Municipal Court rules. The rules apply identically to Steilacoom Municipal Court via AOC routing.
- OCR artifacts in the source PDF text layer survive into rules.md (e.g. `LI\4CLR`/`LMCLR`, `t` substituted for `1` in some rule numbers, spaced-out letters within words). Cross-check against the source PDF before quoting verbatim. The PDF itself does not mention DuPont or Steilacoom; the shared-document relationship is established by AOC routing, not by the document text.
