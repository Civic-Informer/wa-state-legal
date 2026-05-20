---
name: wa-moses-lake-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Moses Lake Municipal Court local court rules. Triggers on local-rule citations attached to Moses Lake (Grant County). NOTE: Moses Lake Municipal Court shares its rules document with Grant County District Court (and 10 other municipal courts: Coulee City, Electric City, Ephrata, George, Grand Coulee, Mattawa, Quincy, Royal City, Soap Lake, Warden). Do NOT use for other WA jurisdictions outside this shared set, state-level rules, RCW, or WAC.
---

# Moses Lake Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/13/DIS/LCR_Grant_DIS.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Shared rules document

Moses Lake Municipal Court does not publish a municipal-specific local rules document. AOC routes Moses Lake Municipal Court to the Grant County District Court rules — the same PDF covers Coulee City, Electric City, Ephrata, George, Grand Coulee, Mattawa, Moses Lake, Quincy, Royal City, Soap Lake, Warden. The content of `rules.md` is that shared document verbatim.

## Files

```
moses-lake-municipal/
├── README.md   ← you are here
└── rules.md    ← shared Grant County District Court rules
```

## Looking up a rule

```bash
grep -n -A 60 -E 'LCR ?[0-9]+' rules.md
```

## Citation format

- `LCRRLJ 3.3 (as applied to Moses Lake Municipal Court via Grant County District Court rules)`
- Citation prefixes used in the shared document: LARLJ / LCRLJ / LCRRLJ / LIRLJ

## Caveats

- **Shared document.** This file is the Grant County District Court rules. The rules apply identically to Moses Lake Municipal Court via AOC routing.
- None observed in spot-check.
