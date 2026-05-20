---
name: wa-chehalis-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Chehalis Municipal Court local court rules including emergency-rule supplement. Triggers on CML (CMLARLJ, CMLCrRLJ, CMLIRLJ, etc.) citations attached to Chehalis. Do NOT use for other WA municipal courts, state-level rules, Superior Court local rules, RCW, or WAC.
---

# Chehalis Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/?fa=court_rules.localmunbycrt&lmun=s21&lcrt=Chehalis  
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL. Body text, rule numbering, and lettered/numbered subsections are preserved verbatim from the AOC-published PDFs.

## Files

```
chehalis-municipal/
├── README.md   ← you are here
└── rules.md    ← base rules + 1 emergency rule supplement
```

## Emergency rules — read carefully

This court's `rules.md` is a stack: base rules followed by 1 emergency rule supplement in chronological order (ER01 first). **Supplement(s) override or supplement the base** — when answering a question, check whether a later ER addresses the same rule before relying on the base text.

## Looking up a rule

```bash
# Find the rule in the base section
grep -n -A 60 -E 'CMLARLJ ?[0-9]' rules.md
# See whether any ER touches the same rule
grep -niE 'emergency.*rule|ER0[0-9]|CMLARLJ ?30' rules.md
```

## Citation format

- Base rule: `Chehalis Municipal Court CMLARLJ 1`
- Emergency rule: `Chehalis Municipal Court LGR 30 (Emergency Rule 01, effective July 1, 2026)`

## Caveats

- Base rules use the CML- family of prefixes (CMLARLJ, CMLCrRLJ, CMLIRLJ). ER01 adopts a state-style LGR 30 (Electronic Filing and Service) as an emergency supplement.
