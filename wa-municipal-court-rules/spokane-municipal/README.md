---
name: wa-spokane-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Spokane Municipal Court local court rules. Triggers on SPMGR, SPMCrRLJ, SPMIRLJ citations attached to Spokane. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Spokane Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/32/MUN/Spokane/LCR_Spokane_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. OCR-derived from image-only PDF (42 pages). Rule structure and body text preserved; occasional OCR artifacts (SPMCrRLIJ vs SPMCrRLJ, joined whitespace). Body text reads cleanly.

## Files

```
spokane-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (42 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'SPMGR ?[0-9]+' rules.md
grep -n -A 60 -E 'SPMCrRLJ ?[0-9]+' rules.md
grep -n -A 60 -E 'SPMIRLJ ?[0-9]+' rules.md
```

## Citation format

- `Spokane SPMCrRLJ 3.3`

## Caveats

- OCR-derived from image-only PDF; verify exact wording against the source PDF. Largest document in this cluster; use multi-step grep with generous context windows.
