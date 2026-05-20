---
name: wa-castle-rock-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Castle Rock Municipal Court local court rules. Triggers on local-rule citations attached to Castle Rock (Cowlitz County). NOTE: Castle Rock Municipal Court shares its rules document with Cowlitz County District Court (and 4 other municipal courts: Kalama, Kelso, Longview, Woodland). Do NOT use for other WA jurisdictions outside this shared set, state-level rules, RCW, or WAC.
---

# Castle Rock Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/08/DIS/LCR_Cowlitz_DIS.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Shared rules document

Castle Rock Municipal Court does not publish a municipal-specific local rules document. AOC routes Castle Rock Municipal Court to the Cowlitz County District Court rules — the same PDF covers Castle Rock, Kalama, Kelso, Longview, Woodland. The content of `rules.md` is that shared document verbatim.

## Files

```
castle-rock-municipal/
├── README.md   ← you are here
└── rules.md    ← shared Cowlitz County District Court rules
```

## Looking up a rule

```bash
grep -n -A 60 -E 'LCR ?[0-9]+' rules.md
```

## Citation format

- `LCrRLJ 2.1 (as applied to Castle Rock Municipal Court via Cowlitz County District Court rules)`
- Citation prefixes used in the shared document: LGR / LCRLJ / LCrRLJ / LIRLJ

## Caveats

- **Shared document.** This file is the Cowlitz County District Court rules. The rules apply identically to Castle Rock Municipal Court via AOC routing.
- None observed in spot-check.
