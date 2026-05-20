---
name: wa-pierce-county-local-rules
description: Use when the user asks about Pierce County (Washington) Superior Court local rules — the Tacoma-seated court. Triggers on any "Pierce" + local rule abbreviation. Pierce uses county-prefixed abbreviations — PCLR (civil), PCLSCCAR (arbitration), PCLSPR (special proceedings), PCLCRR (criminal), PCLGR (general), PCLAPR (probate/adoption). Pierce does NOT use the bare "LCR" form — always use the PCL- prefix when citing.
---

# Pierce County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Body text, subsection lettering, page-limit and timing rules, citations, and amendment dates are preserved verbatim. Appendix forms with tabular fill-in layouts (Forms O and P in particular) are flattened to inline text — field labels survive, visual structure does not. If the user needs the visual layout of a specific form, this corpus cannot reproduce it.

## Files

```
pierce/
├── README.md         ← you are here
└── local-rules.md    ← consolidated local rules (long — corresponds to ~111 PDF pages)
```

This is the largest single-county document in the corpus. Plan on multiple grep passes with generous context windows (80-120 lines) rather than a single broad search.

## Pierce's prefix convention

Pierce **exclusively uses PCL- prefixes**. Do not search or cite as "LCR" alone — that won't match Pierce's text and is the wrong citation form.

| Pierce prefix | State equivalent | Domain                                |
|---------------|------------------|---------------------------------------|
| PCLR          | CR               | Civil rules                           |
| PCLSCCAR      | SCCAR            | Superior Court Civil Arbitration      |
| PCLSPR        | SPR              | Special Proceedings                   |
| PCLCRR        | CrR              | Criminal                              |
| PCLGR         | GR               | General Rules                         |
| PCLAPR        | APR              | Probate / Adoption                    |
| PCLFLR        | FLR              | Family Law                            |
| PCLJuCR       | JuCR             | Juvenile                              |

State-rule references (CR, SCCAR, GR, RAP) also appear in the document — these are state-rule citations, not Pierce local rules. The markdown preserves the distinction correctly.

## Looking up a rule

```bash
# Pierce PCLR 7 (motions) — search for PCL- form
grep -n -A 80 -E 'PCLR ?7\b' local-rules.md

# Family law
grep -niE 'PCLFLR ?[0-9]+' local-rules.md

# Criminal
grep -niE 'PCLCRR ?[0-9.]+' local-rules.md

# Arbitration
grep -niE 'PCLSCCAR ?[0-9.]+' local-rules.md
```

## Citation format

- `Pierce County PCLR 7(b)(4)` — civil
- `Pierce County PCLFLR 10` — family law
- `Pierce County PCLCRR 3.1` — criminal
- `Pierce County PCLSCCAR 4.2(b)` — arbitration

## Caveats

- **Size.** ~111 PDF pages of rule text. Multi-step grep with context is more reliable than one broad search.
- **Appendix Forms O and P (Guardianship/Conservatorship boilerplate) are flattened.** Field labels and content survive, but the visual table layout (Person/Guardian columns, checkbox rows, signature blocks) is linearized into inline text. Do not quote these forms for visual fidelity.
- The source PDF preserves a typo ("GUARDIANSHIP/CONSERVATORHIP" missing the "s") in Form O; the markdown reproduces it. That's PDF-accurate.
- Hyperlinks in the PDF render as bold text rather than links — expected.
