---
name: wa-cowlitz-county-local-rules
description: Use when the user asks about Cowlitz County (Washington) Superior Court local rules — the Kelso-seated court. Cowlitz prepends a **CC-** prefix to every local rule (CCLGR, CCLAR, CCLCR, CCLCrR, CCLGALR, CCLSPR, CCSCCAR). Triggers on "Cowlitz" + any local-rule abbreviation, or any "CCLCR" / "CCLAR" / "CCLCrR" citation.
---

# Cowlitz County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Source PDF was text-based; `pdftotext -layout` produced clean output. Some non-ASCII spacing artifacts in the OCR'd table-of-contents block (e.g. `E ective`, `O icers` — fi-ligature dropped). Treat those as scan noise; cross-reference body text where the fi-ligature is intact.

## Files

```
cowlitz/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body
```

## Rule sets covered (Cowlitz uses a county prefix)

| Abbrev   | Rule set |
|----------|----------|
| CCLGR    | Cowlitz Local General Rules |
| CCLAR    | Cowlitz Local Administrative Rules |
| CCLCR    | Cowlitz Local Civil Rules |
| CCLCrR   | Cowlitz Local Criminal Rules |
| CCLGALR  | Cowlitz Local Guardian Ad Litem Rules |
| CCLSPR   | Cowlitz Local Special Proceedings Rules |
| CCSCCAR  | Cowlitz Superior Court Civil Arbitration Rules |

Citations always carry the **CC-** prefix.

## Looking up a rule

```bash
# CCLCR 40 (assignment of cases)
grep -n -A 40 -E 'CCLCR ?40\b' local-rules.md

# All CCLCR rule headings
grep -niE '^\s*CCLCR ?[0-9.]+' local-rules.md

# Cowlitz criminal rules
grep -niE 'CCLCrR ?[0-9.]+' local-rules.md
```

## Citation format

- `Cowlitz County CCLCR 40(b)`
- `Cowlitz County CCLCrR 3.1`
- `Cowlitz County CCLGR 17`

## Caveats

- **Use the CC- prefix in citations.** A bare "LCR 40" is wrong for Cowlitz; the correct cite is "CCLCR 40."
- **fi-ligature scan noise.** Words like "Effective" / "Officers" sometimes appear as "E ective" / "O icers" in the TOC because the fi-ligature glyph wasn't decoded. The body text is normally intact — quote from the body.
- **[Rescinded] entries.** Several CCLCR / CCLAR rules carry "(Rescinded)" markers — keep them out of citations.
