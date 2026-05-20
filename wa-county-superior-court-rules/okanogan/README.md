---
name: wa-okanogan-county-local-rules
description: Use when the user asks about Okanogan County (Washington) Superior Court local rules — the Okanogan-seated court. Okanogan uses bare LCR / LCrR / LMAR / LGALR / LSPR (no county prefix). Triggers on "Okanogan" + any local-rule citation, motion-day question, or arbitration / family-law procedural question.
---

# Okanogan County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL. Source PDF was text-based; `pdftotext -layout` produced clean output. Cite directly from `local-rules.md`.

## Files

```
okanogan/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body
```

## Rule sets covered

| Abbrev | Rule set |
|--------|----------|
| LCR    | Local Civil Rules |
| LCrR   | Local Criminal Rules |
| LMAR   | Local Mandatory Arbitration Rules |
| LGALR  | Local Guardian Ad Litem Rules |
| LSPR   | Local Special Proceedings Rules |

Citations are bare — no Okanogan-specific prefix.

## Looking up a rule

```bash
# LCrR rules
grep -niE '^\s*LCrR ?[0-9.]+' local-rules.md

# LMAR (arbitration)
grep -niE '^\s*LMAR ?[0-9.]+' local-rules.md
```

## Citation format

- `Okanogan County LCR 7(b)`
- `Okanogan County LCrR 3.1`
- `Okanogan County LMAR 1.2`

## Caveats

- **No state-rule text.** State CR / CrR / MAR are referenced but not included.
