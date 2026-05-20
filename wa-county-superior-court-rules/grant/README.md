---
name: wa-grant-county-local-rules
description: Use when the user asks about Grant County (Washington) Superior Court local rules — the Ephrata-seated court. Grant uses bare LCR / LCrR / LAR / LRALJ (no county prefix). Triggers on "Grant County" + any local-rule citation, motion-day question, or appeal-from-court-of-limited-jurisdiction question.
---

# Grant County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL. Source PDF was text-based; `pdftotext -layout` produced clean output. Cite directly from `local-rules.md`.

## Files

```
grant/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body
```

## Rule sets covered

| Abbrev | Rule set |
|--------|----------|
| LAR    | Local Administrative Rules |
| LCR    | Local Civil Rules |
| LCrR   | Local Criminal Rules |
| LRALJ  | Local Rules for Appeal of Decisions of Courts of Limited Jurisdiction |

Citations are bare — no Grant-specific prefix.

## Looking up a rule

```bash
# LCR 7 (motions)
grep -n -A 60 -E '^\s*LCR ?7\b' local-rules.md

# Criminal rules
grep -niE '^\s*LCrR ?[0-9.]+' local-rules.md
```

## Citation format

- `Grant County LCR 7(b)`
- `Grant County LCrR 3.1`
- `Grant County LAR 1`

## Caveats

- **No state-rule text.** State CR / CrR / GR / RALJ are referenced but not included in this corpus.
