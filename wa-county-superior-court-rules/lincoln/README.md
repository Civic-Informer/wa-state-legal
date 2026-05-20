---
name: wa-lincoln-county-local-rules
description: Use when the user asks about Lincoln County (Washington) Superior Court local rules — the Davenport-seated court. Lincoln uses bare LCR / LCrR / LAR (no county prefix). Triggers on "Lincoln County" + any local-rule citation or motion-day question.
---

# Lincoln County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL. Source PDF was text-based; `pdftotext -layout` produced clean output. Cite directly from `local-rules.md`.

## Files

```
lincoln/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body
```

## Rule sets covered

| Abbrev | Rule set |
|--------|----------|
| LAR    | Local Administrative Rules |
| LCR    | Local Civil Rules |
| LCrR   | Local Criminal Rules |

Citations are bare — no Lincoln-specific prefix.

## Looking up a rule

```bash
# LCR 7 (motions)
grep -n -A 60 -E '^\s*LCR ?7\b' local-rules.md

# Criminal rules
grep -niE '^\s*LCrR ?[0-9.]+' local-rules.md
```

## Citation format

- `Lincoln County LCR 7(b)`
- `Lincoln County LCrR 3.1`

## Caveats

- **Disambiguation:** This is Lincoln County, **Washington**, not Lincoln County, Nebraska / Oregon / etc.
- **No state-rule text.** State CR / CrR are referenced but not included.
