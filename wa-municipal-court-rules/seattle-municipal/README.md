---
name: wa-seattle-municipal-court-rules
description: Use when the user asks about Seattle Municipal Court rules (SMCLR / SMCLIR). Source is HTML embedded on seattle.gov, not PDF. Includes monetary penalty schedules (SMCLIR 6.2(a) infractions and 6.2(b) parking) and General Administrative Orders (GAO 2020-12, 2020-14, 2023-01 in full, plus an index of rescinded/active GAOs). Citation forms: SMCLR (criminal/civil) and SMCLIR (infractions).
---

# Seattle Municipal Court — Local Court Rules and GAOs

**Effective date of this snapshot:** 2026-05-20.

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Rule body text, subsection lettering, and effective-date stamps survive the HTML-to-markdown conversion. Penalty-schedule tables retain row order and dollar amounts. GAO PDFs are reproduced as `pdftotext -layout` blocks (signature blocks and stamps drop out). A small amount of seattle.gov page-template wording (e.g., "Click here for General Administrative Orders") sits at the top of each HTML-derived section.

## Files

```
seattle-municipal/
├── README.md
└── rules.md     ← consolidated rules + penalty schedules + GAOs + proposed-rules page
```

`rules.md` is built by concatenating eight source files (HTML + DOCX + PDF) in this order:

1. **Local Court Rules (SMCLR + SMCLIR)** — from `local-court-rules.html`
2. **Monetary Penalty Schedules**
   - **SMCLIR 6.2(a) — Selected Infractions** — from `SMCLIR_6_A_updated_9-2023.docx`
   - **SMCLIR 6.2(b) — Selected Parking Infractions** — from `SCLRIR6.2bparking.docx`
3. **General Administrative Orders**
   - Index (rescinded + active GAOs) — from `general-administrative-orders.html`
   - Full text of GAO 2020-12, GAO 2020-14, GAO 2023-01 — from the three PDFs
4. **Proposed Rules (for public comment)** — from `proposed-rules-for-public-comment.html` (currently: "Nothing at this time")

## Citation forms

| Prefix  | Domain                            |
|---------|-----------------------------------|
| SMCLR   | Seattle Municipal Court Local Rules (criminal/general) |
| SMCLIR  | Seattle Municipal Court Local Infraction Rules |
| GAO     | General Administrative Order (Presiding Judge directive, not a local rule) |

Examples:
- `Seattle SMCLR 3.2(o)` — release of accused / bail
- `Seattle SMCLIR 6.2(a)` — selected infractions penalty schedule
- `Seattle SMCLIR 6.2(b)` — selected parking infractions penalty schedule
- `Seattle GAO 2020-12` — PR-OK warrant order

## Looking up a rule

```bash
# Any SMCLR / SMCLIR rule by number
grep -n -A 40 -E '##  SMCLR ?3\.2' rules.md
grep -n -A 40 -E '##  SMCLIR ?6\.2' rules.md

# A specific GAO (note: the GAO index has summaries; full text only for 2020-12, 2020-14, 2023-01)
grep -n -A 30 -iE 'GAO ?2020-12' rules.md
grep -n -A 60 -iE 'GAO 2023 ?- ?01' rules.md

# A penalty for a specific SMC code
grep -n '12A.14.071' rules.md
```

## Caveats

- **GAO scope.** Only three GAO PDFs (2020-12, 2020-14, 2023-01) exist as standalone documents in the source bundle and are reproduced in full. All other GAOs appear only as summary entries in the index converted from `general-administrative-orders.html` — they are **not** the full GAO text.
- **Proposed rules section.** Reflects what seattle.gov shows as of the snapshot date ("Nothing at this time"). This section will become stale if SMC posts new proposals; it is *not* the adopted-rules section.
- **Penalty schedules are DOCX-sourced.** Effective dates appear at the bottom of each penalty schedule (e.g., parking effective Jan 1, 2025). Dollar amounts include assessments per the source.
- **Some hyperlinks survive as markdown links** (RCW citations, links to other court rules) — they came through pandoc cleanly. They are not refetched at runtime.
- **HTML page chrome.** A short navigation line ("Click here for General Administrative Orders") sits at the top of the LCR section. This is page-template, not rule text — ignore for citation purposes.
- **Offline-only.** Do not refetch from seattle.gov to "verify" — work from the snapshot. If the snapshot is stale, raise that with the user.
