---
name: wa-benton-franklin-local-rules
description: Use when the user asks about Benton or Franklin County (Washington) Superior Court local rules — the Kennewick / Pasco-seated court. Benton and Franklin share one combined ruleset and use bare abbreviations (LCR, LCAR, LCrR, LGR, LFLR, LSPR, LGALR — no county prefix). Triggers on either county name with a local-rule abbreviation, motion-deadline, or family-law procedural question.
---

# Benton / Franklin Counties Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2023.

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Source PDF was text-based; `pdftotext -layout` produced clean output. Multi-column passages and the table of contents are space-aligned (not pipe-tabled). Cite from `local-rules.md` after verifying wording.

## Files

```
benton-franklin/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body for both counties
```

## Rule sets covered

| Abbrev | Rule set |
|--------|----------|
| LGR    | Local General Rules |
| LCR    | Local Civil Rules |
| LCAR   | Local Civil Arbitration Rules |
| LCrR   | Local Criminal Rules |
| LFLR   | Local Family Law Rules |
| LJuCR  | Local Juvenile Court Rules |
| LSPR   | Local Special Proceedings Rules |
| LGALR  | Local Guardian Ad Litem Rules |

Citations are bare — no Benton- or Franklin-specific prefix.

## Looking up a rule

```bash
# All LCR rule headings
grep -niE '^\s*LCR ?[0-9]+' local-rules.md

# LCR 7 (motions)
grep -n -A 80 -E '^\s*LCR ?7\b' local-rules.md

# LCAR — civil arbitration
grep -niE '^\s*LCAR ?[0-9]+' local-rules.md
```

## Citation format

- `Benton/Franklin LCR 7(b)`
- `Benton County LCrR 3.1`
- `Franklin County LFLR 10`

## Caveats

- **2023 snapshot, not 2025.** Benton/Franklin's published copy on courts.wa.gov is still the 2023 effective version. If the user expects post-2023 amendments, flag the staleness.
- **The Benton County website's own link is broken** (per the patch index). This corpus relies on the courts.wa.gov hosted copy.
- **Two counties share one ruleset.** Cite the county whose case is at issue.
