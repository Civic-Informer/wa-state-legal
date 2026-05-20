---
name: wa-westport-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Westport Municipal Court local court rules. Triggers on Rule citations attached to Westport. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Westport Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/14/MUN/Westport/LCR_Westport_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rules use 'Rule 1, Rule 2, ...' sequential numbering; body text preserved.

## Files

```
westport-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (7 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '^[[:space:]]*Rule [0-9]+' rules.md
```

## Citation format

- `Westport Municipal Court Rule 5`

## Caveats

- Local rules use bare 'Rule N' numbering — no abbreviated prefix to grep for.
