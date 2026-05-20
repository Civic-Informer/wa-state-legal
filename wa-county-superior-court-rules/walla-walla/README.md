---
name: wa-walla-walla-county-local-rules
description: Use when the user asks about Walla Walla County (Washington) Superior Court local rules — the Walla Walla-seated court. Walla Walla prepends a **WW-** prefix (WWLAR, WWLGR, WWLCR, WWLCrR, WWLSPR, WWLJuCR, WWLGALR). Triggers on "Walla Walla" + any local-rule citation or any "WWLCR" / "WWLCrR" citation.
---

# Walla Walla County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025 (amended June 30, 2025).

**Fidelity verdict:** FAITHFUL. Source PDF was text-based; `pdftotext -layout` produced clean output. Cite directly from `local-rules.md`.

## Files

```
walla-walla/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body
```

## Rule sets covered (Walla Walla uses a WW- prefix)

| Abbrev   | Rule set |
|----------|----------|
| WWLAR    | Walla Walla Local Administrative Rules |
| WWLGR    | Walla Walla Local General Rules |
| WWLCR    | Walla Walla Local Civil Rules |
| WWLCrR   | Walla Walla Local Criminal Rules |
| WWLJuCR  | Walla Walla Local Juvenile Court Rules |
| WWLGALR  | Walla Walla Local Guardian Ad Litem Rules |
| WWLSPR   | Walla Walla Local Special Proceedings Rules |

Citations always carry the **WW-** prefix.

## Looking up a rule

```bash
# WWLCR 7 (motions)
grep -n -A 60 -E 'WWLCR ?7\b' local-rules.md

# All WWLCR headings
grep -niE 'WWLCR ?[0-9.]+' local-rules.md

# Walla Walla domestic relations (WWLSPR 90.04)
grep -n -A 60 -E 'WWLSPR ?90\.04' local-rules.md
```

## Citation format

- `Walla Walla County WWLCR 7(b)`
- `Walla Walla County WWLCrR 3.3`
- `Walla Walla County WWLSPR 90.04`

## Caveats

- **Use the WW- prefix.** A bare "LCR 7" is wrong for Walla Walla; the correct cite is "WWLCR 7."
- **No state-rule text.** State CR / CrR are referenced but not included.
