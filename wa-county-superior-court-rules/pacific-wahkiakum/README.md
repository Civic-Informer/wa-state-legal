---
name: wa-pacific-wahkiakum-local-rules
description: Use when the user asks about Pacific or Wahkiakum County (Washington) Superior Court local rules. These two counties share a combined ruleset and use bare LCR / LCrR / LGR / LGALR / LAR (no county prefix). Triggers on either county name plus a local-rule citation or motion-day question.
---

# Pacific / Wahkiakum Counties Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL. Source PDF was text-based; `pdftotext -layout` produced clean output. Cite directly from `local-rules.md`.

## Files

```
pacific-wahkiakum/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body for both counties
```

## Rule sets covered

| Abbrev | Rule set |
|--------|----------|
| LAR    | Local Administrative Rules |
| LGR    | Local General Rules |
| LCR    | Local Civil Rules |
| LCrR   | Local Criminal Rules |
| LGALR  | Local Guardian Ad Litem Rules |

Citations are bare. The two counties share rules.

## Looking up a rule

```bash
# LCR 7 (motions)
grep -n -A 60 -E '^\s*LCR ?7\b' local-rules.md

# Criminal rules
grep -niE '^\s*LCrR ?[0-9.]+' local-rules.md
```

## Citation format

- `Pacific County LCR 7(b)` or `Wahkiakum County LCR 7(b)`
- `Pacific/Wahkiakum LCrR 3.1`

## Caveats

- **Two counties share text.** A rule applies to both counties unless the rule body names one explicitly.
- **No state-rule text.** State CR / CrR / GR are referenced but not included.
