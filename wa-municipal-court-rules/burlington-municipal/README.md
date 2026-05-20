---
name: wa-burlington-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Burlington Municipal Court local court rules. Triggers on local-rule citations attached to Burlington (Skagit County). NOTE: Burlington Municipal Court shares its rules document with Skagit County District Court (and 2 other municipal courts: Anacortes, Mount Vernon). Do NOT use for other WA jurisdictions outside this shared set, state-level rules, RCW, or WAC.
---

# Burlington Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/29/DIS/LCR_Skagit_DIS.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Shared rules document

Burlington Municipal Court does not publish a municipal-specific local rules document. AOC routes Burlington Municipal Court to the Skagit County District Court rules — the same PDF covers Anacortes, Burlington, Mount Vernon. The content of `rules.md` is that shared document verbatim.

## Files

```
burlington-municipal/
├── README.md   ← you are here
└── rules.md    ← shared Skagit County District Court rules
```

## Looking up a rule

```bash
grep -n -A 60 -E 'LCR ?[0-9]+' rules.md
```

## Citation format

- `SLARLJ 3 (as applied to Burlington Municipal Court via Skagit County District Court rules)`
- Citation prefixes used in the shared document: SLARLJ / SLCRLJ / SLCrRLJ / SLIRLJ

## Caveats

- **Shared document.** This file is the Skagit County District Court rules. The rules apply identically to Burlington Municipal Court via AOC routing.
- None observed in spot-check.
