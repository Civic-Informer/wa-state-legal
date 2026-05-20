---
name: wa-klickitat-skamania-local-rules
description: Use when the user asks about Klickitat or Skamania County (Washington) Superior Court local rules — the two-county combined court. The snapshot PDF is primarily court **forms** (notes for trial, certificates of readiness, statements of arbitrability) rather than full rule text. Triggers on "Klickitat" or "Skamania" + a procedural / forms question; the actual rule body for these two counties is sparse in this snapshot.
---

# Klickitat / Skamania Counties Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025.

**Fidelity verdict:** DEGRADED. The published PDF for the combined Klickitat/Skamania courts on courts.wa.gov is dominated by **fillable forms** (Note for Trial Setting / Certificate of Readiness / Statement of Arbitrability and similar) rather than narrative rule text. `pdftotext -layout` extracted the form labels and the limited rule body cleanly, but most queries about "Klickitat LCR 7" will not find substantive text here — the rules themselves are minimal in this snapshot.

## Files

```
klickitat-skamania/
├── README.md       ← you are here
└── local-rules.md  ← consolidated body (mostly forms, plus what little narrative rule text the PDF carries)
```

## What's in the snapshot

- **Forms:** Note for Trial Setting / Certificate of Readiness / Statement of Arbitrability (with LMAR cross-references), and adjacent procedural forms.
- **Narrative rule body:** sparse; LMAR (mandatory arbitration) is the most-cited rule set in the form text.

## Looking up a rule

```bash
# Anything mentioning LMAR (mandatory arbitration)
grep -niE 'LMAR ?[0-9.]+' local-rules.md

# The Note for Trial Setting form
grep -n -A 30 'NOTE FOR TRIAL SETTING' local-rules.md
```

## Citation format

- `Klickitat County LMAR 1.2`
- `Skamania County LMAR 1.2`
- Klickitat and Skamania share rule numbering for the published combined ruleset.

## Caveats

- **Forms-heavy PDF.** This is not a comprehensive rule book — the courts.wa.gov-hosted combined PDF leans heavily on procedural forms. For full Klickitat/Skamania civil or criminal rule text, the user should consult the courts.wa.gov source directly (outside this corpus) or each county clerk's office.
- **No state-rule text.** State CR / CrR / MAR are referenced in the forms but not included in this corpus.
