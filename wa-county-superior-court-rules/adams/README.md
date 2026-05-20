---
name: wa-adams-county-local-rules
description: Use when the user asks about Adams County (Washington) Superior Court local rules — the Ritzville-seated court. Adams uses an unusual flat rule set cited as **ACLR** ("Adams County Local Rules"), numbered Rule 1 through Rule N (no LCR / LFLR / LCrR families). Triggers on "Adams County" + any local rule citation, motion-day question, or procedural question tied to the Adams Superior Court.
---

# Adams County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL. Source PDF was text-based; `pdftotext -layout` produced clean output. Cite directly from `local-rules.md`.

## Files

```
adams/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body (single flat ACLR rule set)
```

## Rule set

Adams uses a **single combined rule set**, cited as **ACLR** ("Adams County Local Rules"), numbered Rule 1, Rule 2, Rule 3 … Each rule has lettered subsections (A, B, C, …) and numeric sub-subsections. Adams does **not** use the LCR / LFLR / LCrR / LGR family that most other Washington counties use.

## Looking up a rule

```bash
# All occurrences of "Rule N"
grep -niE '^RULE [0-9]+' local-rules.md

# Sub-section A of Rule 1 (scheduling)
grep -n -A 40 'RULE 1: SCHEDULING' local-rules.md

# Civil motion docket references
grep -ni 'civil motion docket' local-rules.md
```

## Citation format

- `Adams County ACLR 1(C)` (Civil Motion Docket)
- `Adams County ACLR 7(B)` etc.
- Adams County refers to its rules collectively as ACLR.

## Caveats

- **Flat numbering.** Because Adams uses one combined ACLR set rather than the LCR / LFLR / LCrR families, a question framed as "Adams LCR 7" should be re-mapped to ACLR — the topical match is in `local-rules.md` under whichever ACLR rule covers motions or scheduling.
- **References to state rules.** Adams ACLR cross-references state CrR 3.5 / 3.6, RCW chapters, etc. Those state rules are not in this corpus.
