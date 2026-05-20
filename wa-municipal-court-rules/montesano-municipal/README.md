---
name: wa-montesano-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Montesano Municipal Court local court rules. Triggers on Rule citations attached to Montesano. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Montesano Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/14/MUN/Montesano/LCR_Montesano_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rules use simple sequential numbering (Rule 1, Rule 2, ...) with no court-specific prefix; numbering and body text preserved.

## Files

```
montesano-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (11 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '^[[:space:]]*Rule [0-9]+' rules.md
```

## Citation format

- `Montesano Municipal Court Local Rule 8`

## Caveats

- Local rules use bare 'Rule N' numbering — no abbreviated prefix to grep for. Search by rule number or topic keyword.
