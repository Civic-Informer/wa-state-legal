---
name: wa-colfax-municipal-court-rules
description: Use when asked about Colfax Municipal Court rules. NOTE: source is a scanned image PDF transcribed via OCR — citations require verification against the original PDF. The only available document is a 2-page "eFiling Court Rule" covering mandatory electronic filing for attorneys, exceptions, waiver procedure, and electronic-service reciprocity. No other Colfax Municipal Court rules are published online.
---

# Colfax Municipal Court — eFiling Local Rule (OCR'd)

**Effective date of this snapshot:** 2026-05-20. (Source document footer: 04.27.2022, "CLJ-CMS Project — eFiling Colfax Municipal Court — Local Rule Requirements".)

**Fidelity verdict:** DEGRADED. The source is a scanned-image PDF — no text layer existed (`pdftotext -layout` returned 2 bytes of whitespace). The transcription in `rules.md` was produced by rendering at 300 DPI with `pdftoppm` and running Tesseract 5.5.2 (`-l eng`). OCR is inherently lossy. **Any quotation must be verified against the original PDF before being used in a citation, brief, or filing.**

## Files

```
colfax-municipal/
├── README.md
└── rules.md     ← OCR'd text of the 2-page eFiling Court Rule
```

## What's in the corpus

A single 2-page document: **Colfax Municipal Court eFiling Court Rule**, organized as:

- **(a) Electronic filing authorization, charges, exceptions, and waiver**
  - (a)(1) Mandatory Electronic Filing (attorneys must eFile via the court's designated eFiling service)
  - (a)(2) Documents That Shall Not Be e-Filed (four subparts: SECTOR-routed initiation docs, non-electronic-required filings, unscannable docs, oversize docs)
  - (a)(3) Working Copies (no paper duplicates required)
  - (a)(4) Waiver of the Requirement to eFile for attorneys (two subparts: written waiver application with good cause; per-document waiver)
- **(b) Electronic Service** (electronic-service reciprocity: a party accepting electronic service must also serve electronically)

## Looking up the rule

```bash
# Find a specific subsection
grep -n -A 20 -iE 'Mandatory Electronic Filing' rules.md
grep -n -A 20 -iE 'Documents That Shall Not Be' rules.md
grep -n -A 20 -iE 'Waiver of the Requirement' rules.md
grep -n -A 10 -iE 'Electronic Service' rules.md
```

## Caveats

OCR-typical risks present in this transcription:

- **Number/letter confusion.** Tesseract may swap `0` ↔ `O`, `1` ↔ `I` ↔ `l`, `5` ↔ `S`, `8` ↔ `B`. If the rule references dollar amounts, dates, or numbered subsections, verify against the PDF.
- **Mis-segmented list markers.** The original document uses a heavy indented outline with stand-alone `(1) (2) (3) (4)` markers on the left side. OCR sometimes detaches these from the body text — in `rules.md` you may see a column of bare markers followed by the body paragraphs. The intent is preserved but the visual mapping is approximate.
- **Joined words.** Tesseract occasionally drops the space between adjacent words (e.g., "Ifa" instead of "If a" — already visible in the transcript at the start of subsection (b)).
- **Table / column layout loss.** The source uses an indented outline that approximates a 2-column layout (marker column + body column). OCR linearizes this. If structure matters, refer to the PDF.
- **Header/footer artifacts.** The page 2 footer ("CLJ-CMS Project — eFiling Colfax Municipal Court | Local Rule Requirements 04.27.2022 Page 2 of 2") is included; it is not rule text.
- **Scope.** This single 2-page document is the **only** Colfax Municipal Court rule in the corpus. Colfax does not publish any other local rules in any format. For rules outside the eFiling domain (e.g., motions practice, criminal procedure, infractions), Colfax presumably follows the state Court Rules for Courts of Limited Jurisdiction (CrRLJ / CRLJ / IRLJ) directly — but that is *not* documented in this corpus.
- **Offline-only.** Do not refetch the source PDF; work from the snapshot. If the user needs the visual original (to verify OCR-suspect glyphs), they should retrieve the PDF directly from the Colfax Municipal Court / Whitman County clerk.
