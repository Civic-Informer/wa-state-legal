---
name: wa-federal-way-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Federal Way Municipal Court local court rules. Triggers on `FWMCLGR`, `FWMCLR`, `FWMCLIR`, `FWMCLAR` citations attached to Federal Way. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Federal Way Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/17/MUN/Federal_Way/LCR_Federal_Way_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Rule text, numbering, and headings preserved verbatim from source PDF.

## Files

```
federal-way-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (11 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E '(FWMCLGR|FWMCLR|FWMCLIR|FWMCLAR) ?[0-9]+' rules.md
```

## Citation format

- `FWMCLGR 7`

## Caveats

- None observed in spot-check.
