---
name: wa-whatcom-county-local-rules
description: Use when the user asks about Whatcom County (Washington) Superior Court local rules — the Bellingham-seated court. Whatcom uses WC-prefixed abbreviations — WCCR (civil), WCAR (arbitration), WCFLR (family law), WCCRR (criminal). Whatcom does NOT use the bare "LCR" form — always use the WC- prefix when citing.
---

# Whatcom County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 2025.

**Fidelity verdict:** FAITHFUL. Body text, all-caps notice blocks, numeric thresholds (e.g., "by noon nine (9) court days prior"), RCW citations, and amendment-history brackets are preserved verbatim. Cite directly from `local-rules.md`.

## Files

```
whatcom/
├── README.md         ← you are here
└── local-rules.md
```

## Whatcom's prefix convention

Whatcom uses **WC- prefixes** throughout. Examples in the document:

| Whatcom prefix | Domain                                |
|----------------|---------------------------------------|
| WCCR           | Civil rules                           |
| WCAR           | Arbitration                           |
| WCFLR          | Family law                            |
| WCCRR          | Criminal                              |
| WCJuCR         | Juvenile                              |

State-rule references (CR, RCW citations) appear as such — the markdown preserves the distinction.

## Looking up a rule

```bash
# Whatcom WCCR 7 (motions)
grep -n -A 60 -E 'WCCR ?7\b' local-rules.md

# Whatcom WCAR (arbitration rule numbering uses decimals — e.g., WCAR 0.3)
grep -niE 'WCAR ?[0-9.]+' local-rules.md

# Whatcom family law
grep -niE 'WCFLR ?[0-9]+' local-rules.md
```

## Citation format

- `Whatcom County WCCR 7.2(b)`
- `Whatcom County WCAR 0.3(c)`
- `Whatcom County WCFLR 10`

## Caveats

- **TOC at top of file is malformed** (lines ~7-135 are stray markdown table fragments with `<br>` tags). The TOC isn't normative — skip it when answering. Rule text starts after the TOC.
- **Page-footer page numbers** (e.g., "4", "5", "14") appear inline as orphan lines between paragraphs in body text. Strip these when quoting; they're PDF page artifacts, not rule content.
- No fee schedules or monetary tables are embedded in the document.
