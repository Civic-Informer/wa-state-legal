---
name: wa-enumclaw-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Enumclaw Municipal Court local court rules. Triggers on `EMCLGR`, `EMCAR`, `EMCIR` citations attached to Enumclaw. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Enumclaw Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/17/MUN/Enumclaw/LCR_Enumclaw_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Files

```
enumclaw-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (5 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '(EMCLGR|EMCAR|EMCIR) ?[0-9]+' rules.md
```

## Citation format

- `EMCLGR 7`

## Caveats

- None observed in spot-check.
