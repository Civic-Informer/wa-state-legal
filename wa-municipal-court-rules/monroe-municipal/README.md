---
name: wa-monroe-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Monroe Municipal Court local court rules. Triggers on MMCLGR, MMCLR, MMCLIR citations attached to Monroe. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Monroe Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/31/MUN/Monroe/LCR_Monroe_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Body text and rule numbering preserved verbatim.

## Files

```
monroe-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (7 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'MMCLGR ?[0-9]+' rules.md
grep -n -A 60 -E 'MMCLR ?[0-9]+' rules.md
grep -n -A 60 -E 'MMCLIR ?[0-9]+' rules.md
```

## Citation format

- `Monroe MMCLR 3.4`

## Caveats

- None observed in spot-check.
