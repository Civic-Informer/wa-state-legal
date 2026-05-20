---
name: wa-lake-forest-park-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Lake Forest Park Municipal Court local court rules including emergency-rule supplement. Triggers on LFPMC- (LFPMCGR, LFPMCLR, etc.) citations attached to Lake Forest Park. Do NOT use for other WA municipal courts, state-level rules, Superior Court local rules, RCW, or WAC.
---

# Lake Forest Park Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/?fa=court_rules.localmunbycrt&lmun=s17&lcrt=Lake_Forest_Park  
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. The base rules PDF is image-only and was OCR'd before consolidation; expect minor recognition noise in the base section. ER01 is text-native and clean.

## Files

```
lake-forest-park-municipal/
├── README.md   ← you are here
└── rules.md    ← base rules + 1 emergency rule supplement
```

## Emergency rules — read carefully

This court's `rules.md` is a stack: base rules followed by 1 emergency rule supplement in chronological order (ER01 first). **Supplement(s) override or supplement the base** — when answering a question, check whether a later ER addresses the same rule before relying on the base text.

## Looking up a rule

```bash
# Find the rule in the base section
grep -n -A 60 -E 'LFPMC ?[0-9]' rules.md
# See whether any ER touches the same rule
grep -niE 'emergency.*rule|ER0[0-9]|LFPMC ?30' rules.md
```

## Citation format

- Base rule: `Lake Forest Park Municipal Court LFPMCLR 4`
- Emergency rule: `Lake Forest Park Municipal Court LFPMCGR 30 (Emergency Rule 01, effective July 1, 2026)`

## Caveats

- Base rules PDF is scanned (image-only); the base text in `rules.md` is OCR output and may contain stray characters or slight layout breaks. ER01 adopts LFPMCGR 30 (mandatory eFiling effective July 1, 2026).
