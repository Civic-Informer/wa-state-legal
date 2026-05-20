---
name: wa-clark-county-local-rules
description: Use when the user asks about Clark County (Washington) Superior Court local rules — the Vancouver-seated court. Clark uses bare LCR / LCrR / LCAR / LGALR / LSPR / LFLR (no county prefix). Triggers on "Clark" + any local-rule abbreviation, motion-day question, or family-law / arbitration procedural question. Do NOT use for Clark County, Nevada — this corpus is Washington only.
---

# Clark County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025. (Cover page confirms.)

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Source PDF was scanned (image-only, KONICA MINOLTA bizhub); body text was produced by OCR. Spot-check across pages 1, 20, 40, and 55 found the body text very faithful — rule headings (RULE 7, RULE 7.3, RULE 98.00), subsection lettering ((a)/(b)/(c)/(1)/(2)/(A)/(B)…), dollar figures, statutory citations (Title 11 RCW, GDN R 201–206), and amendment dates all preserved.

Observed OCR error patterns:

- **`(1)` → `()`** — the digit `1` inside the parenthesized list marker is sometimes dropped, leaving an empty `()`. Recoverable by context: the next item is `(2)`, so the prior must be `(1)`.
- **Lost word-internal spaces** — e.g. `Ifa subsequent`, `by ajudicial officer` — rare; reflow when quoting.
- **Page numbering offset** — the PDF prepends a cover page, so PDF page N = printed page N−2. Footer page numbers in the converted text follow the printed numbering.

Cite directly from `local-rules.md`. Spot-verify against the official source PDF on courts.wa.gov only for verbatim quotation.

## Files

```
clark/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body (OCR'd)
```

## Rule sets covered

| Abbrev | Rule set |
|--------|----------|
| LCR    | Local Civil Rules |
| LCrR   | Local Criminal Rules |
| LCAR   | Local Civil Arbitration Rules |
| LGALR  | Local Guardian Ad Litem Rules |
| LSPR   | Local Special Proceedings Rules |
| LFLR   | Local Family Law Rules (where present) |

Citations are bare — no Clark-specific prefix.

## Looking up a rule

```bash
# RULE 7 (pleadings / motions)
grep -n -A 60 -E '^\s*RULE\s+7\b' local-rules.md

# LCR 7 alternate heading style
grep -n -A 60 -E '^\s*LCR ?7\b' local-rules.md

# RULE 98.00 (estates / ex parte presentation)
grep -n -A 80 -E 'RULE\s+98\.00' local-rules.md

# Civil arbitration
grep -niE 'LCAR ?[0-9.]+' local-rules.md
```

## Citation format

- `Clark County LCR 7(b)(2)(A)`
- `Clark County LCrR 3.1`
- `Clark County LCAR 1.1`
- `Clark County Rule 98.00(a)(1)(A)` (this ruleset sometimes labels sections "RULE N" rather than "LCR N" — both refer to the same provisions)

## Caveats

- **OCR-derived.** Body text is reliable; the `(1)` → `()` substitution is the most consistent quirk. Verify dollar amounts and numbered list items against the official source PDF on courts.wa.gov when precision matters.
- **Disambiguation:** This is Clark County, **Washington** (Vancouver), not Clark County, Nevada or Ohio.
- **No state-rule text.** State CR / CrR are referenced but not included.
