---
name: wa-whitman-county-local-rules
description: Use when the user asks about Whitman County (Washington) Superior Court local rules — the Colfax-seated court. Whitman prepends a **WC-** prefix (WCLAR, WCLCR, WCLCrR, WCLFLR, WCLGALR). Triggers on "Whitman" + any local-rule citation. **Disambiguation:** Whitman's WC- prefix is similar to Whatcom's WCCR / WCAR — distinguish by which county the user named, and by the third letter (Whatcom uses WCC- / WCA-, Whitman uses WCL-).
---

# Whitman County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL. Source PDF was text-based; `pdftotext -layout` produced clean output. Cite directly from `local-rules.md`.

## Files

```
whitman/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body
```

## Rule sets covered (Whitman uses a WC- prefix)

| Abbrev   | Rule set |
|----------|----------|
| WCLAR    | Whitman Local Administrative Rules |
| WCLCR    | Whitman Local Civil Rules |
| WCLCrR   | Whitman Local Criminal Rules |
| WCLFLR   | Whitman Local Family Law Rules |
| WCLGALR  | Whitman Local Guardian Ad Litem Rules |

Citations always carry the **WC-** prefix.

## Looking up a rule

```bash
# WCLCR 1 (motions, responses, replies)
grep -n -A 40 -E 'WCLCR ?1\b' local-rules.md

# All WCLAR headings
grep -niE 'WCLAR ?[0-9.]+' local-rules.md

# Family law
grep -niE 'WCLFLR ?[0-9.]+' local-rules.md
```

## Citation format

- `Whitman County WCLCR 1(a)`
- `Whitman County WCLCrR 3.3`
- `Whitman County WCLAR 5`

## Caveats

- **Whitman vs Whatcom prefix confusion.** Whitman uses `WCLAR / WCLCR / WCLCrR / WCLFLR` (WC + L + ...). Whatcom uses `WCCR / WCAR` (Whatcom County Court Rules). They are easy to confuse because both begin with "WC." Always distinguish by the county name; the third letter is the strongest signal (Whitman: WCL-; Whatcom: WCC- / WCA-).
- **No state-rule text.** State CR / CrR are referenced but not included.
