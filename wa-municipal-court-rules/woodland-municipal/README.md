---
name: wa-woodland-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Woodland Municipal Court local court rules. Triggers on local-rule citations attached to Woodland (Cowlitz County). NOTE: Woodland Municipal Court shares its rules document with Cowlitz County District Court (and 4 other municipal courts: Castle Rock, Kalama, Kelso, Longview). Do NOT use for other WA jurisdictions outside this shared set, state-level rules, RCW, or WAC.
---

# Woodland Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/08/DIS/LCR_Cowlitz_DIS.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Shared rules document

Woodland Municipal Court does not publish a municipal-specific local rules document. AOC routes Woodland Municipal Court to the Cowlitz County District Court rules — the same PDF covers Castle Rock, Kalama, Kelso, Longview, Woodland. The content of `rules.md` is that shared document verbatim.

## Files

```
woodland-municipal/
├── README.md   ← you are here
└── rules.md    ← shared Cowlitz County District Court rules
```

## Looking up a rule

```bash
grep -n -A 60 -E 'LCR ?[0-9]+' rules.md
```

## Citation format

- `LCrRLJ 2.1 (as applied to Woodland Municipal Court via Cowlitz County District Court rules)`
- Citation prefixes used in the shared document: LGR / LCRLJ / LCrRLJ / LIRLJ

## Caveats

- **Shared document.** This file is the Cowlitz County District Court rules. The rules apply identically to Woodland Municipal Court via AOC routing.
- None observed in spot-check.
