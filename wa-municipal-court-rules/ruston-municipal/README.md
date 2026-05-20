---
name: wa-ruston-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Ruston Municipal Court local court rules. Triggers on Local Rule, RMCLR citations attached to Ruston. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Ruston Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/27/MUN/Ruston/LCR_Ruston_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule numbering and body text preserved verbatim.

## Files

```
ruston-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (5 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'Local Rule [0-9]+' rules.md
grep -n -A 60 -E 'RMCLR ?[0-9]+' rules.md
```

## Citation format

- `Ruston Municipal Court Local Rule 4.2`

## Caveats

- The Ruston rules use bare numeric labels (1.1, 1.2, 3.1, ...) for the most part and do not consistently prefix each rule; cite by section number and 'Ruston Municipal Court'.
