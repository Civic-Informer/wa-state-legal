---
name: wa-grays-harbor-county-local-rules
description: Use when the user asks about Grays Harbor County (Washington) Superior Court local rules — the Montesano-seated court. Grays Harbor uses bare LCR / LCrR / LGR / LGALR / LMAR / LRALJ / LJuCR (no county prefix). Triggers on "Grays Harbor" + any local-rule citation, motion-day question, or arbitration / juvenile procedural question.
---

# Grays Harbor County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL. Source PDF was text-based; `pdftotext -layout` produced clean output. Cite directly from `local-rules.md`.

## Files

```
grays-harbor/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body
```

## Rule sets covered

| Abbrev | Rule set |
|--------|----------|
| LGR    | Local General Rules |
| LCR    | Local Civil Rules |
| LCrR   | Local Criminal Rules |
| LMAR   | Local Mandatory Arbitration Rules |
| LJuCR  | Local Juvenile Court Rules |
| LGALR  | Local Guardian Ad Litem Rules |
| LRALJ  | Local Rules for Appeal of Decisions of Courts of Limited Jurisdiction |

Citations are bare — no Grays Harbor-specific prefix.

## Looking up a rule

```bash
# LCR 7 (motions)
grep -n -A 60 -E '^\s*LCR ?7\b' local-rules.md

# Mandatory arbitration
grep -niE '^\s*LMAR ?[0-9.]+' local-rules.md
```

## Citation format

- `Grays Harbor County LCR 7(b)`
- `Grays Harbor County LCrR 3.1`
- `Grays Harbor County LMAR 1.2`

## Caveats

- **No state-rule text.** State CR / CrR / GR / MAR are referenced but not included.
