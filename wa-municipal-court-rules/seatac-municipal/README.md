---
name: wa-seatac-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares SeaTac Municipal Court local court rules. Triggers on STMCLR citations attached to SeaTac. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# SeaTac Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/17/MUN/Seatac/LCR_SeaTac_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule labels, rescission notes, and body text preserved verbatim.

## Files

```
seatac-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (13 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'STMCLR ?[0-9]+' rules.md
```

## Citation format

- `SeaTac STMCLR 3.2`

## Caveats

- Several listed rules are marked 'Rescinded' in the document; preserved as-is.
