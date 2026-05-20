---
name: wa-lakewood-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Lakewood Municipal Court local court rules. Triggers on local-rule citations attached to Lakewood (Pierce County). NOTE: Lakewood Municipal Court's rules document is shared with DuPont and Steilacoom municipal courts. Do NOT use for other WA jurisdictions outside this shared set, state-level rules, RCW, or WAC.
---

# Lakewood Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/27/MUN/Lakewood/LCR_Lakewood_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL-WITH-OCR-ARTIFACTS. Source PDF was produced by a Canon scanner with embedded OCR; the PDF text layer contains occasional character substitutions baked in at scan time (e.g. `rABLE OF CONTENTS`, `LI\4CLR` for `LMCLR`, `t.2` for `1.2`, `Defin itio n s`). Rule numbering, structure, and substantive text are preserved; quote with care.

## Shared rules document

Lakewood Municipal Court is the originating court for this rules document. DuPont and Steilacoom municipal courts also operate under these same rules via AOC routing. The content of `rules.md` is the Lakewood Municipal Court local rules verbatim.

## Files

```
lakewood-municipal/
├── README.md   ← you are here
└── rules.md    ← shared Pierce County Lakewood Municipal Court rules
```

## Looking up a rule

```bash
grep -n -A 60 -E 'LCR ?[0-9]+' rules.md
```

## Citation format

- `LMCLR GR 1.1 (Lakewood Municipal Court Local Rules, as applied to Lakewood Municipal Court)`
- Citation prefixes used in the shared document: LMCLR (Lakewood Municipal Court Local Rules)

## Caveats

- **Shared document.** This file is the Pierce County's Lakewood Municipal Court rules. The rules apply identically to Lakewood Municipal Court via AOC routing.
- OCR artifacts in the source PDF text layer survive into rules.md (e.g. `LI\4CLR`/`LMCLR`, `t` substituted for `1` in some rule numbers, spaced-out letters within words). Cross-check against the source PDF before quoting verbatim. The PDF itself does not mention DuPont or Steilacoom; the shared-document relationship is established by AOC routing, not by the document text.
