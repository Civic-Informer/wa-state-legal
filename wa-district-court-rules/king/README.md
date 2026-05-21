---
name: wa-king-district-court-rules
description: Use when the user asks about, cites, quotes, or compares King County District Court (Washington) local court rules — any LCRLJ / LIRLJ / LCrRLJ / LARLJ / LMAR / LGR rule attached to this court. Do NOT use for Superior Court LOCAL rules (sibling skill: wa-county-superior-court-rules/), municipal-court LOCAL rules (sibling skill: wa-municipal-court-rules/), the statewide CRLJ/IRLJ/CrRLJ/ARLJ/RALJ rules (sibling skill: wa-state-court-rules/), RCW (sibling skills: wa-rcw-1-50/ and wa-rcw-51-100/), or WAC (sibling skill: wa-administrative-code/).
---

# King County District Court — Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/17/DIS/LCR_King_DIS.pdf  (provenance only — do not refetch)
**Snapshot date:** 2026-05-20  
**Effective date of base rules:** 2025-09-01  

**Fidelity verdict:** FAITHFUL. Native-text PDF, clean conversion.

## Files

```
king/
├── README.md   ← you are here
└── rules.md    ← consolidated district court rules
```

## Looking up a rule

```bash
grep -n -E '^\s*(LARLJ|LCRLJ|LCrRLJ|LGR|LIRLJ) ?[0-9]' rules.md
```

## Citation examples

- `King County District Court LARLJ {rule number}`
- `King County District Court LCRLJ {rule number}`
- `King County District Court LCrRLJ {rule number}`
- `King County District Court LGR {rule number}`
- `King County District Court LIRLJ {rule number}`

## Caveats

- Includes Algona Municipal and Pacific Municipal Courts (under district court rules).
