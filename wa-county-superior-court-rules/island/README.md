---
name: wa-island-county-local-rules
description: Use when the user asks about Island County (Washington) Superior Court local rules — the Oak Harbor / Coupeville-seated court covering Whidbey and Camano. Triggers on any "Island" + local rule abbreviation (LGR, LCR, LFLR, LCrR, LJuCR, LGAL, LCAR/LSCCAR, LMAR, LRALJ, LSPR).
---

# Island County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL. Body text, subsection lettering, motion deadlines, and amendment-history brackets are preserved verbatim. Cite directly from `local-rules.md`.

## Files

```
island/
├── README.md         ← you are here
└── local-rules.md
```

## Looking up a rule

```bash
# Island LCR 6 (motion deadlines)
grep -n -A 80 -E '^\*?\*?LCR ?6\b' local-rules.md

# Island LFLR (family law)
grep -niE 'LFLR ?[0-9]+' local-rules.md
```

If a first-pass grep misses, drop the rule-set prefix and search the bare number.

## Citation format

- `Island County LCR 6(d)(1)(A)`
- `Island County LFLR 10`
- `Island County LCrR 3.1`

## Caveats

- Island County covers both Whidbey and Camano; the rules apply to both venues — no separate per-island rule set.
- **LCR 79(d)(1) references an externally-maintained Clerk fee schedule** — not embedded in this document. If the user asks for actual fee amounts, this corpus cannot answer.
- The source PDF preserved a few idiosyncratic typos (e.g., "scheduled  hearing. unless", "(6) six calendar days") which appear in the markdown verbatim; those are PDF-accurate, not MD errors.
