---
name: wa-skagit-county-local-rules
description: Use when the user asks about Skagit County (Washington) Superior Court local rules — the Mount Vernon-seated court. Skagit prepends an **SCL-** prefix (SCLAR, SCLGR, SCLCR, SCLCrR, SCLFLR, SCLGALR, SCLSPR, SCLCAR). Triggers on "Skagit" + any local-rule citation. **Disambiguation:** the SCL- prefix is shared with Snohomish — distinguish by which county the user named.
---

# Skagit County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025 (2025-2026 ruleset).

**Fidelity verdict:** FAITHFUL. Source PDF was text-based; `pdftotext -layout` produced clean output. Cite directly from `local-rules.md`.

## Files

```
skagit/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body
```

## Rule sets covered (Skagit uses an SCL- prefix)

| Abbrev   | Rule set |
|----------|----------|
| SCLAR    | Skagit Local Administrative Rules |
| SCLGR    | Skagit Local General Rules |
| SCLCR    | Skagit Local Civil Rules |
| SCLCrR   | Skagit Local Criminal Rules |
| SCLFLR   | Skagit Local Family Law Rules |
| SCLGALR  | Skagit Local Guardian Ad Litem Rules |
| SCLSPR   | Skagit Local Special Proceedings Rules |
| SCLCAR   | Skagit Local Civil Arbitration Rules |

The PDF organizes the rules in PART I (administrative), PART II (general), PART III (civil), etc.

## Looking up a rule

```bash
# SCLCR rules
grep -niE 'SCLCR ?[0-9.]+' local-rules.md

# Rule 7 — Motions (under PART III civil)
grep -n -A 60 -E 'PART III\. CIVIL RULES' local-rules.md

# All "Rule N" headings
grep -niE '^\s*Rule\s+[0-9.]+' local-rules.md | head -40
```

## Citation format

- `Skagit County SCLCR 7(b)`
- `Skagit County SCLCrR 3.1`
- `Skagit County SCLGR 30` (electronic filing)

## Caveats

- **SCL- prefix is shared with Snohomish County.** Both counties prepend "SCL" (Skagit Local / Snohomish County Local). Always disambiguate by the county name the user gave. The rule numbering schemes differ — never carry a rule from one county to the other.
- **Part-organized layout.** The 2025-2026 PDF presents rules under PART I/II/III/etc. labels with internal "Rule N" subheadings rather than running headings like "SCLCR 7". When grepping for a specific rule, search both the abbreviation (SCLCR 7) and the bare "Rule 7" pattern within the appropriate PART.
- **No state-rule text.** State CR / CrR / GR are referenced but not included.
