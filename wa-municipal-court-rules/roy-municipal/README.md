---
name: wa-roy-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Roy Municipal Court local court rules. Triggers on RMCLR citations attached to Roy. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Roy Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/27/MUN/Roy/LCR_Roy_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule numbering (1.1, 1.2, ...) and body text preserved verbatim.

## Files

```
roy-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (3 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'RMCLR ?[0-9]+' rules.md
```

## Citation format

- `Roy RMCLR 1.2`

## Caveats

- The RMCLR prefix is shared with Renton Municipal Court — both abbreviate to 'RMCLR'. Always disambiguate by city ('Roy RMCLR' vs 'Renton RMCLR').
