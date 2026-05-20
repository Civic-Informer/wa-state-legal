---
name: wa-thurston-county-local-rules
description: Use when the user asks about Thurston County (Washington) Superior Court local rules — the Olympia-seated court. Triggers on any "Thurston" + local rule abbreviation (LGR, LCR, LFLR, LCrR, LJuCR, LGAL, LMAR / LCAR, LSPR, LRALJ).
---

# Thurston County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL. Body text, multi-level subsections, case-law citations, court-rule cross-references (e.g., CR 56, KCLAR), and form-name references (FL All Family 131, 140) are preserved verbatim. Cite directly from `local-rules.md`.

## Files

```
thurston/
├── README.md         ← you are here
└── local-rules.md
```

## Looking up a rule

```bash
# Thurston LCR 56 (summary judgment)
grep -n -A 60 -E 'LCR ?56\b' local-rules.md

# Thurston LGR 30 (electronic filing)
grep -n -A 80 -E 'LGR ?30\b' local-rules.md

# Thurston LSPR 94.03 (family law / trials)
grep -niE 'LSPR ?94\.03' local-rules.md
```

## Citation format

- `Thurston County LCR 7(b)`
- `Thurston County LFLR 10`
- `Thurston County LCrR 3.1`
- `Thurston County LSPR 94.03E(e)`

## Caveats

- **Running footers preserved inline.** Page footers like "Thurston County Superior Court Local Rules – 2025 / Page N" appear between paragraphs in some places. Strip them when quoting body text.
- **LGR 29 layout quirk.** The rule jumps from subsection (a)(1)(A) directly to (g) — that's the source PDF's structure, not a markdown defect.
- LCR 79(g) references an externally-maintained schedule of clerk charges; no fee table is embedded.
