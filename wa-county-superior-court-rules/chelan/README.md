---
name: wa-chelan-county-local-rules
description: Use when the user asks about Chelan County (Washington) Superior Court local rules — the Wenatchee-seated court. Chelan uses bare LCR / LCrR / LGR / LMAR / LGALR / LAR (no county prefix). Triggers on "Chelan" + any local-rule abbreviation, motion-day question, or family-law / arbitration procedural question.
---

# Chelan County Superior Court — Local Court Rules

**Effective date of this snapshot:** **September 1, 2022.** (The courts.wa.gov index lists Chelan as "Sep 1, 2025" but the hosted PDF is the 2022 order, last republished without further amendment. Always include the 2022 effective date qualifier when citing Chelan.)

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Source PDF was scanned (image-only, RICOH MP 3054); body text was produced by OCR. Spot-check across pages 1, 35, 70, and 100 found the body text essentially perfect — rule headings, subsection lettering, dollar figures, CR / LMAR / LCrR cross-references, and dates all preserved. The PDF presents one rule per page with large whitespace margins, which gave OCR excellent conditions.

- **Handwritten signature/date fields** on the front-matter order page (page 1) OCR'd as `_|` / `Tuy` (for "1st day of July") — that is signature scribble being interpreted as ASCII. The substantive rule text is unaffected.

Cite directly from `local-rules.md`. Verify only if quoting unusual punctuation or numbers verbatim in a brief.

## Files

```
chelan/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body (OCR'd, 2022 snapshot)
```

## Rule sets covered

| Abbrev | Rule set |
|--------|----------|
| LAR    | Local Administrative Rules |
| LGR    | Local General Rules |
| LCR    | Local Civil Rules |
| LCrR   | Local Criminal Rules |
| LMAR   | Local Mandatory Arbitration Rules |
| LGALR  | Local Guardian Ad Litem Rules |

Citations are bare — no Chelan-specific prefix.

## Looking up a rule

```bash
# LCR 65 (injunctions)
grep -n -A 30 -E '^\s*LCR ?65\b' local-rules.md

# Mandatory arbitration (LMAR)
grep -niE '^\s*LMAR ?[0-9.]+' local-rules.md

# LCrR 3.4 (presence of defendant)
grep -n -A 20 -E 'LCrR ?3\.4\b' local-rules.md
```

## Citation format

- `Chelan County LCR 7(b)(4) (eff. Sept. 1, 2022)`
- `Chelan County LCrR 3.1 (eff. Sept. 1, 2022)`
- `Chelan County LMAR 6.2 (eff. Sept. 1, 2022)`

Always include the **2022** effective-date qualifier when citing Chelan — the published snapshot is older than the patch index implies.

## Caveats

- **2022 snapshot.** Despite the courts.wa.gov listing implying 2025, the PDF itself is the September 1, 2022 order. Flag staleness if the user expects post-2022 amendments.
- **OCR-derived.** Body text is reliable across the 107-page document. Verify only when quoting verbatim.
- **No state-rule text.** State CR / CrR / GR / MAR are referenced but not included.
