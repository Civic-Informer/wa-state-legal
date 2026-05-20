---
name: wa-mason-county-local-rules
description: Use when the user asks about Mason County (Washington) Superior Court local rules, or cites a rule prefixed "Mason" with any of these abbreviations — LGR, LCR, LSCCAR, LSPR, LGAL, LCrR, LJuCR, LRALJ. Covers civil, family/probate (LSPR 94.04), criminal, juvenile, GAL, civil-arbitration, and limited-jurisdiction appeal procedures for Mason County Superior Court.
---

# Mason County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2023.

**Fidelity verdict:** FAITHFUL. Body text, subsection lettering, dollar figures, dates, and citation references are preserved verbatim against the source PDF. Cite directly from `local-rules.md`.

## Files

```
mason/
├── README.md         ← you are here
└── local-rules.md    ← consolidated local rules, markdown
```

## Rule sets covered

Mason consolidates all rule families in one document. Sections present:

| Abbreviation | Rule set                                                                 |
|--------------|--------------------------------------------------------------------------|
| LGR          | Local General Rules (only LGR 29 — presiding judge)                      |
| LCR          | Local Civil Rules (7, 16, 40, 53.2, 56, 65)                              |
| LSCCAR       | Local Superior Court Civil Arbitration Rules (1.1–8.6)                   |
| LSPR         | Local Special Proceedings (94.04 family/probate/GAL/adoption; 95.01 Torrens [Rescinded]; 96.01 civil contempt; 97.01 motions; 98.01 ex parte) |
| LGAL         | Local Guardian Ad Litem (LGAL 5 registry; LGAL 7 grievance)              |
| LCrR         | Local Criminal (3.1 right to counsel; 3.4 presence; 4.2 commissioners)   |
| LJuCR        | Local Juvenile Court (LJuCR 9.2 right to lawyer)                         |
| LRALJ        | Limited-jurisdiction appeal rules (LRALJ 6.3.1 transcript)               |

## Looking up a rule

```bash
# Mason LCR 7 (motions)
grep -n -A 60 -E '^\*?\*?LCR 7\b' local-rules.md

# Mason LSPR 94.04 (family law / probate / guardianship)
grep -n -A 120 -E 'LSPR 94\.04' local-rules.md
```

Headings render as `## **LCR 7 MOTIONS**` and `## **LSPR 94.04 ...**`. If grep misses, broaden the pattern.

## Citation format

- `Mason County LCR 7(b)(3)`
- `Mason County LSPR 94.04(c)`
- `Mason County LGAL 7`

## Caveats

- **LSPR 95.01 (Torrens Act) is rescinded.** If the user asks about Torrens petitions in Mason, the local rule is no longer in force.
- **TOC at top of file.** Rule text begins after the second top-level heading "MASON COUNTY SUPERIOR COURT LOCAL COURT RULES" — the first block is just the table of contents and renders as a slightly degraded markdown table. Skip it when reading body text.
- **Older snapshot than peers.** Sept 1, 2023 — most other counties here are Sept 1, 2025. Flag this to the user if currency could matter.
