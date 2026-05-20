---
name: wa-jefferson-county-local-rules
description: Use when the user asks about Jefferson County (Washington) Superior Court local rules — the Port Townsend-seated court. Jefferson uses bare LCR / LCrR / LFLR / LGR / LCAR / LRALJ / LSPR (no county prefix). Triggers on "Jefferson" + any local-rule citation, motion-day question, family-law procedural question, or arbitration question.
---

# Jefferson County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Source PDF was text-based; `pdftotext -layout` produced clean output. Cite directly from `local-rules.md`.

## Files

```
jefferson/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body
```

## Rule sets covered

| Abbrev | Rule set |
|--------|----------|
| LGR    | Local General Rules |
| LCR    | Local Civil Rules |
| LCAR   | Local Civil Arbitration Rules |
| LCrR   | Local Criminal Rules |
| LFLR   | Local Family Law Rules |
| LSPR   | Local Special Proceedings Rules |
| LRALJ  | Local Rules for Appeal of Decisions of Courts of Limited Jurisdiction |

Citations are bare — no Jefferson-specific prefix.

## Looking up a rule

```bash
# LCR 16 (pretrial procedure)
grep -n -A 40 -E '^\s*LCR ?16\b' local-rules.md

# LFLR rules
grep -niE '^\s*LFLR ?[0-9.]+' local-rules.md
```

## Citation format

- `Jefferson County LCR 16(a)`
- `Jefferson County LCrR 3.1`
- `Jefferson County LFLR 10`

## Caveats

- **No state-rule text.** State CR / CrR / GR are referenced but not included.
