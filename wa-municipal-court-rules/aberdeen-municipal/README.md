---
name: wa-aberdeen-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Aberdeen Municipal Court local court rules including emergency-rule supplement. Triggers on AMCLR / AMCLIR citations attached to Aberdeen. Do NOT use for other WA municipal courts, state-level rules, Superior Court local rules, RCW, or WAC.
---

# Aberdeen Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/?fa=court_rules.localmunbycrt&lmun=s14&lcrt=Aberdeen  
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Body text, rule numbering, and lettered/numbered subsections are preserved verbatim from the AOC-published PDFs.

## Files

```
aberdeen-municipal/
├── README.md   ← you are here
└── rules.md    ← base rules + 1 emergency rule supplement
```

## Emergency rules — read carefully

This court's `rules.md` is a stack: base rules followed by 1 emergency rule supplement in chronological order (ER01 first). **Supplement(s) override or supplement the base** — when answering a question, check whether a later ER addresses the same rule before relying on the base text.

## Looking up a rule

```bash
# Find the rule in the base section
grep -n -A 60 -E 'AMCLR ?[0-9]' rules.md
# See whether any ER touches the same rule
grep -niE 'emergency.*rule|ER0[0-9]|AMCLR ?30' rules.md
```

## Citation format

- Base rule: `Aberdeen Municipal Court AMCLR 4.1`
- Emergency rule: `Aberdeen Municipal Court AMCLR 30 (Emergency Rule 01, effective June 3, 2026)`

## Caveats

- Base rules cover criminal (AMCLR) and infraction (AMCLIR) practice; the lone ER01 adopts AMCLR 30 (mandatory eFiling) effective June 3, 2026.
