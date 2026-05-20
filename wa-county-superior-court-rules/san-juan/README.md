---
name: wa-san-juan-county-local-rules
description: Use when the user asks about San Juan County (Washington) Superior Court local rules — the Friday Harbor-seated court. San Juan uses bare LCR / LCrR / LGR / LJuCR (no county prefix). Triggers on "San Juan" + any local-rule citation, motion-day question, or juvenile / family-law procedural question.
---

# San Juan County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Source PDF was text-based; `pdftotext -layout` produced clean output. Cite directly from `local-rules.md`.

## Files

```
san-juan/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body
```

## Rule sets covered

| Abbrev | Rule set |
|--------|----------|
| LGR    | Local General Rules |
| LCR    | Local Civil Rules |
| LCrR   | Local Criminal Rules |
| LJuCR  | Local Juvenile Court Rules |

Citations are bare — no San Juan-specific prefix.

## Looking up a rule

```bash
# LCR 43 (testimony)
grep -n -A 30 -E '^\s*LCR ?43\b' local-rules.md

# All LCR headings
grep -niE '^\s*LCR ?[0-9.]+' local-rules.md

# Juvenile court rules
grep -niE '^\s*LJuCR ?[0-9.]+' local-rules.md
```

## Citation format

- `San Juan County LCR 7(b)`
- `San Juan County LCrR 3.1`
- `San Juan County LJuCR 1.7`

## Caveats

- **No state-rule text.** State CR / CrR / GR are referenced but not included.
