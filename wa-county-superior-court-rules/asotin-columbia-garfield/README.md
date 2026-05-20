---
name: wa-asotin-columbia-garfield-local-rules
description: Use when the user asks about Asotin, Columbia, or Garfield County (Washington) Superior Court local rules. These three counties share a single combined ruleset, cited with bare LCR / LCrR / LGR / LJuCR / LSPR / LGALR (no county prefix). Triggers on any of those three county names combined with a local-rule abbreviation, motion-day question, or family-law procedural question.
---

# Asotin / Garfield / Columbia Counties Superior Court — Local Court Rules

(Note: the published PDF orders the counties as "Asotin, Garfield, and Columbia"; the URL slug orders them differently. Either order names the same combined ruleset.)

**Effective date of this snapshot:** September 1, 2025 (per the courts.wa.gov index).

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Source PDF was scanned (image-only); body text was produced by OCR. Rule body, subsection lettering ((a)/(b)/(c)…), CR / LCR cross-references, dates, and amendment markers are all preserved. OCR error patterns confirmed by sampling pages 1, 12, 24, and 33 against the rendered PDF:

- **Table-of-contents abbreviation drift.** A few TOC entries show single-character substitution: e.g. `LER 3,1` for `LCR 3.1`, and `LOR 59` for `LCR 59`. The body text for those rules carries the correct abbreviation — trust the body.
- **Form pages have heavier noise.** Form pages (Plea Agreement, Notice of Digital Exhibit, etc.) capture checkbox glyphs ☐ as `LC]` / `LJ]`, and capital `I` is sometimes rendered as `|`. The rule-body pages are clean; the noise concentrates on the form-template pages near the back.

Use the converted text directly for navigation and substantive citation; for verbatim quotation in briefs, spot-verify against the official source PDF on courts.wa.gov.

## Files

```
asotin-columbia-garfield/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body for all three counties (OCR'd)
```

## Rule sets covered

The three counties share one combined ruleset. Citations are bare (no county prefix). Sets present include:

| Abbrev | Rule set |
|--------|----------|
| LCR    | Local Civil Rules |
| LCrR   | Local Criminal Rules |
| LGR    | Local General Rules |
| LJuCR  | Local Juvenile Court Rules |
| LSPR   | Local Special Proceedings Rules |
| LGALR  | Local Guardian Ad Litem Rules |

## Looking up a rule

```bash
# Headings — all LCR rules
grep -niE '^\s*LCR ?[0-9]+' local-rules.md

# LCR 7 (motions)
grep -n -A 60 -E '^\s*LCR ?7\b' local-rules.md

# LCR 53.2 (court commissioners — known OCR-clean body)
grep -n -A 40 -E 'LCR ?53\.2\b' local-rules.md

# Summary judgment-style searches
grep -ni 'summary judgment' local-rules.md
```

## Citation format

- `Asotin/Garfield/Columbia LCR 7(b)(4)` (the three counties share rules — name whichever county the case is in).
- `Asotin County LCrR 3.1` / `Columbia County LCrR 4.5` etc.

## Caveats

- **OCR-derived.** See fidelity verdict above for the specific error patterns observed during spot-check. Body text is reliable; TOC and form pages have isolated character substitutions.
- **Tri-county shared text.** A rule applies to all three counties unless the rule text itself names one of them explicitly.
- **No state-rule text.** State CR / CrR / GR / etc. are referenced but not included in this corpus.
