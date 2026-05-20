---
name: wa-port-orchard-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Port Orchard Municipal Court local court rules. Triggers on LCrRLJ, LIRLJ, LCRRLJ citations attached to Port Orchard. Do NOT use for other WA municipal courts, state-level rules (CRLJ, CrRLJ, GR, ER), Superior Court local rules, RCW, or WAC.
---

# Port Orchard Municipal Court Local Court Rules

**Source:** https://storage.googleapis.com/proudcity/portorchardwa/uploads/2020/09/Muni-Court-Local-Court-Rules.pdf
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. OCR-derived from image-only PDF (city-hosted, not AOC). Rule structure and body text survive; minor OCR artifacts visible in the table of contents (dot leaders rendered as garbled fill).

## Files

```
port-orchard-municipal/
├── README.md   ← you are here
└── rules.md    ← consolidated local court rules (10 PDF pages)
```

## Looking up a rule

```bash
grep -n -A 60 -E 'LCrRLJ ?[0-9]+' rules.md
grep -n -A 60 -E 'LIRLJ ?[0-9]+' rules.md
grep -n -A 60 -E 'LCRRLJ ?[0-9]+' rules.md
```

## Citation format

- `Port Orchard LCrRLJ 3.2.2`

## Caveats

- Source PDF is hosted by the City of Port Orchard at storage.googleapis.com (per portorchardwa.gov), not by the Washington State AOC. OCR-derived — verify wording against the source PDF.
