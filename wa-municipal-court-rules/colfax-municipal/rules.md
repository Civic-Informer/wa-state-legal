# Colfax Municipal Court — eFiling Local Rule (OCR'd)

**Court:** Colfax Municipal Court
**Source:** `_source/colfax-municipal/20240612083929.pdf` (a 2-page scanned image PDF with no embedded text layer)
**Snapshot date:** 2026-05-20
**Fidelity verdict:** **DEGRADED.** The source is a scanned-image PDF; this document was produced by rendering at 300 DPI (`pdftoppm`) and running Tesseract OCR (`-l eng`). OCR is inherently lossy and commonly mis-recognizes characters such as `0/O`, `1/I/l`, `5/S`, and `rn/m`. It also tends to mis-segment column or bullet labels (you may see stray `(1)` / `(2)` markers detached from their list items below). **Any quotation drawn from this document MUST be verified against the original PDF before being used in a citation, brief, or filing.**

## Source file consolidated into this document

| Source file | Format | Pages | Pipeline |
|---|---|---|---|
| `20240612083929.pdf` | Scanned-image PDF | 2 | `pdftoppm -r 300 → tesseract -l eng` |

The source PDF is a single document titled "Colfax Municipal Court — eFiling Court Rule" describing mandatory electronic filing for attorneys.

---

# Colfax Municipal Court — eFiling Court Rule (OCR transcription)

```
COLFAX MUNICIPAL COURT
EFILING COURT RULE

(a) Electronic filing (“eFile”) authorization, charges, exceptions, and waiver
[option: and non-compliance].

(1)

(2)

(3)

(4)

Mandatory Electronic Filing. Effective [30 days after go-live], attorneys shall
electronically file (eFile) all documents using the court’s designated eFiling
service, eFile & Serve, unless this rule provides otherwise. Non-attorneys or pro
se parties are not required to eFile, but are encouraged to do so.

Documents That Shall Not Be e-Filed. The following documents may not be

eFiled:

(a)

(b)

(c)

(d)

A criminal case initiation document (e.g., complaint, citation, or notice of
infraction) that is not submitted through the Statewide Electronic Collision
& Traffic Online Records (SECTOR) application per GR 30(d)(ii);

A document that is required by law to be filed in non-electronic format,
for example, original wills, certified records of proceedings for purposes
of appeal, negotiable instruments, and documents of foreign governments
under official seal;

Documents incapable of legible conversion to an electronic format by
scanning, imaging, or any other means;

Documents larger than permitted in the User Agreement.

Working Copies. Attorneys and other eFilers are not required to provide duplicate
paper pleadings as “working copies” for judicial officers.

Waiver of the Requirement to eFile for attorneys.

(a)

(b)

If an attorney is unable to eFile documents, the attorney may request a
waiver from the court. The attorney must make a showing of good
cause and explain why paper document(s) must be filed in that
particular case. The court will consider each application and provide a
written approval or denial to the attorney. Attorneys who receive a
waiver shall file a copy of the waiver in each case in which they file
documents. Attorneys who receive a waiver shall place the words
“Exempt from eFiling per waiver filed on (date)” in the caption of all
paper documents filed for the duration of the waiver.

Upon a showing of good cause the court may waive the requirement as
to a specific document or documents on a case by case basis.
(b) Electronic Service. Ifa party serves another party electronically or via email, that
party must likewise accept service from the other parties electronically or via email.

CLJ-CMS Project — eFiling Colfax Municipal Court
| Local Rule Requirements 04.27.2022 Page 2 of 2
```

---

## OCR provenance

- Tool: `tesseract 5.5.2` (`leptonica-1.87.0`)
- Language model: `eng`
- Render resolution: 300 DPI (`pdftoppm -r 300`)
- Confirmed no text layer in source PDF: `pdftotext -layout 20240612083929.pdf -` returned 2 bytes (whitespace only).
- All page output concatenated in order; no pages dropped or failed.
