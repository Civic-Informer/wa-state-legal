---
name: wa-kittitas-county-local-rules
description: Use when the user asks about Kittitas County (Washington) Superior Court local rules — the Ellensburg-seated court. Kittitas uses bare LCR / LCrR / LGR / LMAR / LGALR / LSPR (no county prefix). The General Rules are labeled either "LGR" or "GLR" in the source PDF (likely scanning-induced character ambiguity — see Caveats). Triggers on "Kittitas" + any local-rule citation, motion-day question, or family-law / arbitration procedural question.
---

# Kittitas County Superior Court — Local Court Rules

**Effective date of this snapshot:** **September 1, 2023.** (The order on page 20 reads "THESE LOCAL RULES SHALL BE EFFECTIVE ON SEPTEMBER 1, 2023." The courts.wa.gov index lists Kittitas as "Sep 1, 2025" but the hosted PDF is the 2023 order.)

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Source PDF was scanned (image-only, PaperPort 12); body text was produced by OCR. Spot-check across pages 1, 10, 20, and 28 found the rule body text faithful — rule headings (LMAR 8.5, LMAR 8.6), subsection lettering ((a)/(b)/(i)/(ii)…), $1,000.00 dollar figures, CR cross-references, and amendment dates all preserved.

Observed OCR error patterns:

- **Page 1 / TOC has the heaviest noise** — e.g. `repéals` for `repeals`, `Bytransmitting` (lost space), `KittitasCounty`, `iin` for `in`, `1rules` (digit prepended). The body of each rule is cleaner.
- **`GLR` vs `LGR` ambiguity.** The General Rules family is titled "LOCAL GENERAL RULES (LGR)" but the individual rule labels OCR as "GLR 1", "GLR 2", "GLR 3". This is almost certainly OCR misreading bold-underlined "LGR" as "GLR" (one downstream `LGR 29` survives correctly). Grep both forms when looking for General Rules.
- **Exhibit D (final pages) is line-numbered pleading paper.** The line numbers in the left gutter (1-29) interleave with body text in the OCR output, mid-paragraph. Body content survives; expect stray digits.
- **Right-edge scan dust** captured as trailing periods/commas.

For substantive lookup, use the converted text. For verbatim quotation in briefs, spot-verify against the official source PDF on courts.wa.gov.

## Files

```
kittitas/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body (OCR'd, 2023 snapshot)
```

## Rule sets covered

| Abbrev | Rule set |
|--------|----------|
| LGR (also OCR'd as GLR) | Local General Rules |
| LCR    | Local Civil Rules |
| LCrR   | Local Criminal Rules |
| LMAR   | Local Mandatory Arbitration Rules |
| LGALR  | Local Guardian Ad Litem Rules |
| LSPR   | Local Special Proceedings Rules |

Citations are bare — no Kittitas-specific prefix.

## Looking up a rule

```bash
# General Rules — grep both spellings
grep -niE '^\s*(LGR|GLR) ?[0-9]+' local-rules.md

# LMAR 8 (arbitration administration / compensation)
grep -n -A 20 -E 'LMAR ?8' local-rules.md

# All LCR rule headings
grep -niE '^\s*LCR ?[0-9.]+' local-rules.md

# Family-law domestic relations (Exhibit D)
grep -n -A 30 'TEMPORARY ORDERS FOR PARTIES WITH MINOR' local-rules.md
```

## Citation format

- `Kittitas County LCR 7(b) (eff. Sept. 1, 2023)`
- `Kittitas County LCrR 3.1 (eff. Sept. 1, 2023)`
- `Kittitas County LMAR 8.5 (eff. Sept. 1, 2023)`
- `Kittitas County LGR 1` (the source spelling is ambiguous between LGR and GLR; "LGR" matches the family-title convention)

Always include the **2023** effective-date qualifier — the published snapshot is older than the patch index implies.

## Caveats

- **2023 snapshot.** Despite the courts.wa.gov listing implying 2025, the PDF is the September 1, 2023 order. Flag staleness if the user expects post-2023 amendments.
- **OCR-derived.** TOC and form pages noisier; rule body cleaner. See verdict above for specifics.
- **GLR/LGR ambiguity.** Grep both forms when searching the General Rules family.
- **Exhibit D pleading-paper layout** interleaves gutter line numbers with body text.
- **No state-rule text.** State CR / CrR / GR / MAR are referenced but not included.
