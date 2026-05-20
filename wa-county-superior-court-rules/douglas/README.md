---
name: wa-douglas-county-local-rules
description: Use when the user asks about Douglas County (Washington) Superior Court local rules — the Waterville-seated court. Douglas uses an unusual bare **LR** for its civil rules (rather than "LCR"), plus LCrR for criminal and LSPR for special proceedings. Triggers on "Douglas County" + any local-rule citation or motion-day question.
---

# Douglas County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL. Short ruleset; `pdftotext -layout` produced clean output. Cite directly from `local-rules.md`.

## Files

```
douglas/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body
```

## Rule sets covered

| Abbrev | Rule set |
|--------|----------|
| LR     | Local Rules (Douglas uses the bare "LR" for civil — not "LCR") |
| LCrR   | Local Criminal Rules |
| LSPR   | Local Special Proceedings Rules |

The civil/probate/guardianship rules are presented as numbered sections (LR 5, LR 7, LR 56, LR 77, LR 94.04, LR 98.04, etc.) under the bare "LR" heading.

## Looking up a rule

```bash
# LR 56 (summary judgment)
grep -n -A 40 -E '^\s*LR ?56\b' local-rules.md

# LCrR 3.1 (right to counsel)
grep -n -A 20 -E 'LCrR ?3\.1\b' local-rules.md

# LSPR 94.04 (family law)
grep -n -A 30 -E 'LSPR ?94\.04\b' local-rules.md
```

## Citation format

- `Douglas County LR 56(j)` (civil — note: **LR**, not LCR)
- `Douglas County LCrR 3.1`
- `Douglas County LSPR 94.04`

## Caveats

- **"LR" not "LCR" for civil.** A user who types "Douglas LCR 56" is asking about Douglas LR 56 — re-map and pull from `local-rules.md`.
- **Short ruleset.** Many state-CR-numbered topics are absent because Douglas hasn't adopted a local supplement on that topic. Absence ≠ disagreement with the state rule.
- **Preface lists 2021 amendment order.** The published PDF includes the 2021 ORDER amending LR 56(j), LR 77, and adding LSPR 94.04 — that order is reproduced in the snapshot for context but is not itself a rule.
