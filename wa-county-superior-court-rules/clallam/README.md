---
name: wa-clallam-county-local-rules
description: Use when the user asks about Clallam County (Washington) Superior Court local rules — the Port Angeles-seated court. Clallam uses bare LCR / LCrR / LMAR / LGALR / LRALJ / LAR (no county prefix). Triggers on "Clallam" + any local-rule abbreviation, motion-day question, or procedural question tied to the Clallam Superior Court.
---

# Clallam County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Source PDF was text-based; `pdftotext -layout` produced clean output. Cite directly from `local-rules.md`.

## Files

```
clallam/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body
```

## Rule sets covered

| Abbrev | Rule set |
|--------|----------|
| LAR    | Local Administrative Rules |
| LCR    | Local Civil Rules |
| LCrR   | Local Criminal Rules |
| LMAR   | Local Mandatory Arbitration Rules |
| LGALR  | Local Guardian Ad Litem Rules |
| LRALJ  | Local Rules for Appeal of Decisions of Courts of Limited Jurisdiction |

Citations are bare — no Clallam-specific prefix.

## Looking up a rule

```bash
# LCR 7 (motions)
grep -n -A 60 -E '^\s*LCR ?7\b' local-rules.md

# All LCrR rules
grep -niE '^\s*LCrR ?[0-9.]+' local-rules.md

# Mandatory arbitration
grep -niE '^\s*LMAR ?[0-9.]+' local-rules.md
```

## Citation format

- `Clallam County LCR 7(b)`
- `Clallam County LCrR 3.1`
- `Clallam County LMAR 2.1`
- `Clallam County LRALJ 4`

## Caveats

- **Space-aligned tables.** Tables and indented lists came through pdftotext as space-aligned columns rather than pipe-tables. Reflow when quoting.
- **No state-rule text.** State CR / CrR / GR are referenced but not included in this corpus.
