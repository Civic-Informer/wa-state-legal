---
name: wa-ferry-pend-oreille-stevens-local-rules
description: Use when the user asks about Ferry, Pend Oreille, or Stevens County (Washington) Superior Court local rules. These three counties share a combined ruleset and use bare LCR / LCrR / LAR / LJuCR / LRALJ (no county prefix). Triggers on any of those three county names plus a local-rule citation, motion-day question, or appeal-from-court-of-limited-jurisdiction question.
---

# Ferry / Pend Oreille / Stevens Counties Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL. Source PDF was text-based; `pdftotext -layout` produced clean output. Cite directly from `local-rules.md`.

## Files

```
ferry-pend-oreille-stevens/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body for all three counties
```

## Rule sets covered

| Abbrev | Rule set |
|--------|----------|
| LAR    | Local Administrative Rules |
| LCR    | Local Civil Rules |
| LCrR   | Local Criminal Rules |
| LJuCR  | Local Juvenile Court Rules |
| LRALJ  | Local Rules for Appeal of Decisions of Courts of Limited Jurisdiction |

Citations are bare. The three counties share rules.

## Looking up a rule

```bash
# LCR 5 (service / filing)
grep -n -A 30 -E '^\s*LCR ?5\b' local-rules.md

# LRALJ headings
grep -niE '^\s*LRALJ ?[0-9.]+' local-rules.md
```

## Citation format

- `Ferry/Pend Oreille/Stevens LCR 7(b)`
- `Stevens County LCrR 3.1`
- `Pend Oreille County LJuCR 1.7`

## Caveats

- **Tri-county shared text.** A rule applies to all three counties unless the rule body names one explicitly.
- **No state-rule text.** State CR / CrR / GR / RALJ are referenced but not included in this corpus.
