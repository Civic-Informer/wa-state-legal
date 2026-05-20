---
name: wa-ocean-shores-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Ocean Shores Municipal Court local court rules. Triggers on Rule citations attached to Ocean Shores. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Ocean Shores Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/14/MUN/Ocean_Shores/LCR_Ocean_Shores_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Body text and numbering preserved verbatim.

## Files

```
ocean-shores-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (11 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '^[[:space:]]*Rule [0-9]+' rules.md
```

## Citation format

- `Ocean Shores Municipal Court Rule 9`

## Caveats

- Local rules use bare 'Rule N' numbering — no abbreviated prefix to grep for.
