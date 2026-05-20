---
name: wa-shelton-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Shelton Municipal Court local court rules. Triggers on SHMGR, SHMCrRLJ, SHMIRLJ citations attached to Shelton. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Shelton Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/23/MUN/Shelton/LCR_Shelton_MUN.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. OCR-derived from image-only PDF; rule labels and body text survive. Minor OCR artifacts (occasional 'I' for 'I', '!' for 'I' in section headers).

## Files

```
shelton-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (17 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'SHMGR ?[0-9]+' rules.md
grep -n -A 60 -E 'SHMCrRLJ ?[0-9]+' rules.md
grep -n -A 60 -E 'SHMIRLJ ?[0-9]+' rules.md
```

## Citation format

- `Shelton SHMCrRLJ 3.3`

## Caveats

- OCR-derived from image-only PDF; verify exact wording against the source PDF.
