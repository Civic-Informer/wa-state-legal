---
name: wa-yakima-county-local-rules
description: Use when the user asks about Yakima County (Washington) Superior Court local rules — the Yakima-seated court. Yakima uses bare LCR / LCrR / LFLR / LGR / LAR / LCAR / LJuCR / LRALJ (no county prefix). Triggers on "Yakima" + any local-rule citation, motion-day question, or family-law / arbitration / juvenile procedural question.
---

# Yakima County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL. Source PDF was text-based; `pdftotext -layout` produced clean output. Cite directly from `local-rules.md`.

## Files

```
yakima/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body
```

## Rule sets covered

| Abbrev | Rule set |
|--------|----------|
| LAR    | Local Administrative Rules |
| LGR    | Local General Rules |
| LCR    | Local Civil Rules |
| LCAR   | Local Civil Arbitration Rules |
| LCrR   | Local Criminal Rules |
| LFLR   | Local Family Law Rules |
| LJuCR  | Local Juvenile Court Rules |
| LRALJ  | Local Rules for Appeal of Decisions of Courts of Limited Jurisdiction |

Citations are bare — no Yakima-specific prefix.

## Looking up a rule

```bash
# LCR 7 (motions)
grep -n -A 60 -E '^\s*LCR ?7\b' local-rules.md

# Family law rules
grep -niE '^\s*LFLR ?[0-9.]+' local-rules.md

# Civil arbitration
grep -niE '^\s*LCAR ?[0-9.]+' local-rules.md
```

## Citation format

- `Yakima County LCR 7(b)`
- `Yakima County LCrR 3.1`
- `Yakima County LFLR 10`

## Caveats

- **No state-rule text.** State CR / CrR / GR are referenced but not included.
