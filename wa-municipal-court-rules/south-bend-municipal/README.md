---
name: wa-south-bend-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares South Bend Municipal Court local court rules including emergency-rule supplement. Triggers on South Bend Local Court Rule N (numbered 1–23, no letter prefix) citations attached to South Bend. Do NOT use for other WA municipal courts, state-level rules, Superior Court local rules, RCW, or WAC.
---

# South Bend Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/?fa=court_rules.localmunbycrt&lmun=s25&lcrt=SouthBend  
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Base rules PDF is text-native and faithful. ER01 is an image-only scan that was OCR'd and shows recognition noise (extra whitespace, broken letters); read the supplement carefully.

## Files

```
south-bend-municipal/
├── README.md   ← you are here
└── rules.md    ← base rules + 1 emergency rule supplement
```

## Emergency rules — read carefully

This court's `rules.md` is a stack: base rules followed by 1 emergency rule supplement in chronological order (ER01 first). **Supplement(s) override or supplement the base** — when answering a question, check whether a later ER addresses the same rule before relying on the base text.

## Looking up a rule

```bash
# Find the rule in the base section
grep -n -A 60 -E '^[[:space:]]*RULE ?7\b' rules.md
# See whether any ER touches the same rule
grep -niE 'emergency.*rule|amendment.*rule.*22|ER0[0-9]' rules.md
```

## Citation format

- Base rule: `South Bend Municipal Court Local Rule 7`
- Emergency rule: `South Bend Municipal Court Local Rule 22 (Emergency Amendment, 2026)`

## Caveats

- South Bend uses plain numbered rules (Rule 1 through Rule 23) rather than letter-prefixed citations. ER01 is a scanned/OCR'd emergency amendment to Local Rule 22 (Electronic Filing) and contains visible OCR noise — read carefully.
