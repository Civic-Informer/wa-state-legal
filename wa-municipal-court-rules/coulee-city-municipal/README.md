---
name: wa-coulee-city-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Coulee City Municipal Court local court rules. Triggers on local-rule citations attached to Coulee City (Grant County). NOTE: Coulee City Municipal Court shares its rules document with Grant County District Court (and 10 other municipal courts: Electric City, Ephrata, George, Grand Coulee, Mattawa, Moses Lake, Quincy, Royal City, Soap Lake, Warden). Do NOT use for other WA jurisdictions outside this shared set, state-level rules, RCW, or WAC.
---

# Coulee City Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/13/DIS/LCR_Grant_DIS.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Shared rules document

Coulee City Municipal Court does not publish a municipal-specific local rules document. AOC routes Coulee City Municipal Court to the Grant County District Court rules — the same PDF covers Coulee City, Electric City, Ephrata, George, Grand Coulee, Mattawa, Moses Lake, Quincy, Royal City, Soap Lake, Warden. The content of `rules.md` is that shared document verbatim.

## Files

```
coulee-city-municipal/
├── README.md   ← you are here
└── rules.md    ← shared Grant County District Court rules
```

## Looking up a rule

```bash
grep -n -A 60 -E 'LCR ?[0-9]+' rules.md
```

## Citation format

- `LCRRLJ 3.3 (as applied to Coulee City Municipal Court via Grant County District Court rules)`
- Citation prefixes used in the shared document: LARLJ / LCRLJ / LCRRLJ / LIRLJ

## Caveats

- **Shared document.** This file is the Grant County District Court rules. The rules apply identically to Coulee City Municipal Court via AOC routing.
- None observed in spot-check.
