---
name: wa-spokane-county-local-rules
description: Use when the user asks about Spokane County (Washington) Superior Court local rules — the Spokane-seated court. Spokane uses bare LCR / LCrR / LGR / LAR / LJuCR / LSCCAR / LSPR / LRALJ (no county prefix). Triggers on "Spokane" + any local-rule citation, motion-day question, or arbitration / juvenile / family-law procedural question.
---

# Spokane County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL. Source PDF was text-based (hosted on spokanecounty.gov, not courts.wa.gov); `pdftotext -layout` produced clean output. Cite directly from `local-rules.md`.

## Files

```
spokane/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body
```

## Rule sets covered

| Abbrev   | Rule set |
|----------|----------|
| LAR      | Local Administrative Rules |
| LGR      | Local General Rules |
| LCR      | Local Civil Rules |
| LCrR     | Local Criminal Rules |
| LJuCR    | Local Juvenile Court Rules |
| LSCCAR   | Local Superior Court Civil Arbitration Rules |
| LSPR     | Local Special Proceedings Rules |
| LRALJ    | Local Rules for Appeal of Decisions of Courts of Limited Jurisdiction |

Citations are bare — no Spokane-specific prefix.

## Looking up a rule

```bash
# LCR 7 (motions)
grep -n -A 80 -E '^\s*LCR ?7\b' local-rules.md

# Civil arbitration (LSCCAR)
grep -niE '^\s*LSCCAR ?[0-9.]+' local-rules.md
```

## Citation format

- `Spokane County LCR 7(b)`
- `Spokane County LCrR 3.1`
- `Spokane County LSCCAR 1.1`

## Caveats

- **Source URL slug reads "2023" but document is the 2025 version** (per the patch index). The body confirms 2025 effective dates.
- **No state-rule text.** State CR / CrR / GR are referenced but not included.
