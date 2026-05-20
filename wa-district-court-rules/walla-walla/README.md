---
name: wa-walla-walla-district-court-rules
description: Use when the user asks about, cites, quotes, or compares Walla Walla County District Court (Washington) local court rules — any LCRLJ / LIRLJ / LCrRLJ / LARLJ / LMAR / LGR rule attached to this court. Do NOT use for Superior Court LOCAL rules (sibling skill: wa-county-superior-court-rules/), municipal-court LOCAL rules (sibling skill: wa-municipal-court-rules/), the statewide CRLJ/IRLJ/CrRLJ/ARLJ/RALJ rules (sibling skill: wa-state-court-rules/), RCW (sibling skill: wa-rcw/), or WAC (sibling skill: wa-administrative-code/).
---

# Walla Walla County District Court — Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/pdf/LCR/36/DIS/LCR_Walla_Walla_DIS.pdf  (provenance only — do not refetch)
**Snapshot date:** 2026-05-20  
**Effective date of base rules:** 2025-09-01  

**Fidelity verdict:** FAITHFUL. Native-text PDF, clean conversion.

## Files

```
walla-walla/
├── README.md   ← you are here
└── rules.md    ← consolidated district court rules
```

## Looking up a rule

```bash
grep -n -E '^\s*(WWDGR|WWDIR) ?[0-9]' rules.md
```

## Citation examples

- `Walla Walla County District Court WWDGR {rule number}`
- `Walla Walla County District Court WWDIR {rule number}`

## Caveats

- The initial dynamic URL on courts.wa.gov (`?ruleId=districtdiswaltable&pdf=1`) only returns a table-of-rules summary, not the rule bodies. The actual ruleset PDF is at the standard pattern path (`pdf/LCR/36/DIS/LCR_Walla_Walla_DIS.pdf`) — that's what's in this snapshot.
