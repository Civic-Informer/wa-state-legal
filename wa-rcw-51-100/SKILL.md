---
name: rcw-51-100
description: Use when the user asks about, cites, quotes, paraphrases, or compares Washington State statute law — the Revised Code of Washington (RCW) — for any Title numbered 51 through 91, or any lettered variant within that numeric range (62A, 70A, 71A, 79A). Triggers on citations like `RCW 51.32.030`, `RCW 59.18.030`, `RCW 62A.9A-313`, `Chapter 70A.205 RCW`, `RCW 82.04.220`, `RCW 90.03.250`, or subject-matter queries that map to a Title in this range (workers' comp / industrial insurance, fire / port / PUD / sanitary / water-sewer / diking / flood / irrigation / waterway districts, landlord-tenant, liens, foreclosure, UCC / secured transactions / sales / leases, personal and real property, recording, alcoholic beverage control, gambling, controlled substances / cannabis, public health and environment, behavioral health and ITA, developmental disabilities, state institutions / DOC, veterans, public assistance / TANF / Medicaid, forests, fish and wildlife, mines, public lands and state parks, public utilities / UTC, common carriers / railroads, B&O / sales / use / estate / property taxes, water rights / shorelines / SEPA, etc.). Routes the request to the relevant Title's `README.md` for grep-able statute text. Do NOT use for RCW Titles 1–50 or lettered variants 9A / 23B / 28A / 28B / 28C / 29A / 29B / 30A / 30B / 35A / 50A / 50B — those live in the sibling skill `rcw-1-50` at `../wa-rcw-1-50/`. Also do NOT use for WAC implementing regulations (sibling skill `wa-administrative-code` at `../wa-administrative-code/`), Washington court rules (sibling skills `wa-state-court-rules`, `wa-county-superior-court-rules`, `wa-district-court-rules`, `wa-municipal-court-rules`), federal statutes (out of scope), or case law interpreting the RCW (out of scope).
---

# Revised Code of Washington — Titles 51–91 — Skill-Routed Corpus

This skill answers questions from a curated, on-disk snapshot of the
**Washington State Legislature's 2025 RCW Archive** for **Titles 51
through 91** (plus lettered variants in that range), captured on
**2026-05-20**. The corpus is an offline, citable snapshot — its
contents are fixed as of the snapshot date. Do not attempt to refetch
from the web at runtime; the local files are authoritative.

The full RCW is split across two sibling skills:

- **Sibling skill (`rcw-1-50`)** at `../wa-rcw-1-50/` — Titles 1–50,
  including lettered variants 9A, 23B, 28A, 28B, 28C, 29A, 29B, 30A,
  30B, 35A, 50A, 50B.
- **This skill (`rcw-51-100`)** — Titles 51–91, including lettered
  variants 62A, 70A, 71A, 79A.

The split is purely a packaging convenience driven by directory size;
the underlying RCW is one body of law. If a citation's Title number is
≤ 50 (or is 9A / 23B / 28A-C / 29A-B / 30A-B / 35A / 50A-B), open the
sibling router instead.

This is the **router** for the second half. It is the only `SKILL.md`
in this bundle. Each RCW Title has its own subdirectory containing a
`README.md` (per-Title playbook this router instructs you to read) and
a `rules.md` (the consolidated statute body for that Title). Per-Title
`README.md` files are **not** separately registered skills — they are
documents this router tells you to open.

For any topic-specific question, follow the routing table below to the
Title's `README.md` first; that file lists the chapter cites inside its
`rules.md` and shows the grep patterns to extract specific sections.

## What this corpus contains

- **42 Titles** of the RCW (Titles 51–91 numeric plus lettered Titles
  62A, 70A, 71A, 79A).
- **891 chapters** consolidated from the Legislature's per-Title
  "Complete Title" PDFs.
- **~36 MB** of grep-able markdown across this half of the corpus.

The source body is the Legislature's combined per-Title PDF (one PDF per
Title, containing the full chapter-by-chapter text). The per-chapter HTML
pages from the Legislature's site contain only section TOCs and chapter
notes — **the actual statute body lives only in the PDFs**, so the PDFs
are the canonical source for `rules.md`.

## Title numbers absent from the archive (within range 51–91)

These Title numbers do not exist in the RCW and have no directory here:

- `56`, `62`, `75` — no longer assigned / reserved (Title 56 was the
  predecessor sewer-districts code, replaced by 57; Title 62 was the
  predecessor UCC, replaced by 62A; Title 75 was the predecessor fish-
  and-wildlife code, replaced by 77).

## Glossary — Title number → directory name

Directory names use plain-English kebab-case. The bare Title number is
what a lawyer types in citations; the directory name is what the file
tree shows. Both are useful.

### Labor / industrial insurance, utilities, transportation

| Title | Directory                                          | Scope                                                                |
|------:|----------------------------------------------------|----------------------------------------------------------------------|
| 51    | `51-industrial-insurance/`                         | Workers' compensation                                                |
| 80    | `80-public-utilities/`                             | UTC; electric/gas/telecom utilities                                  |
| 81    | `81-transportation/`                               | Common carriers; railroads; vessel pilotage                          |

### Special districts (utilities, fire, water)

| Title | Directory                          | Scope                          |
|------:|------------------------------------|--------------------------------|
| 52    | `52-fire-protection-districts/`    | Fire protection districts      |
| 53    | `53-port-districts/`               | Port districts                 |
| 54    | `54-public-utility-districts/`     | PUDs                           |
| 55    | `55-sanitary-districts/`           | Sanitary districts             |
| 57    | `57-water-sewer-districts/`        | Water-sewer districts          |
| 85    | `85-diking-and-drainage/`          | Diking; drainage districts     |
| 86    | `86-flood-control/`                | Flood control districts        |
| 87    | `87-irrigation/`                   | Irrigation districts           |
| 88    | `88-navigation-and-harbor-improvements/` | Pilotage; harbor lines      |
| 89    | `89-reclamation-soil-conservation-and-land-settlement/` | Conservation districts |
| 91    | `91-waterways/`                    | Waterways; dredging            |

### Property, real estate, recording, commerce

| Title | Directory                                                       | Scope                                                              |
|------:|-----------------------------------------------------------------|--------------------------------------------------------------------|
| 58    | `58-boundaries-and-plats/`                                      | Surveys; plats; subdivisions; condominiums                          |
| 59    | `59-landlord-and-tenant/`                                       | Residential Landlord-Tenant Act; unlawful detainer; mobile homes    |
| 60    | `60-liens/`                                                     | Mechanic's, materialman's, garage keeper's, agricultural liens      |
| 61    | `61-mortgages-deeds-of-trust-and-real-estate-contracts/`        | Foreclosure (judicial and nonjudicial)                              |
| 62A   | `62A-uniform-commercial-code/`                                  | UCC — sales, leases, negotiable instruments, secured transactions  |
| 63    | `63-personal-property/`                                         | Sales; replevin; unclaimed property; gift cards                     |
| 64    | `64-real-property-and-conveyances/`                             | Deeds; covenants; easements; condominiums                           |
| 65    | `65-recording-registration-and-legal-publication/`              | Auditor recording; real-estate excise tax                           |

### Taxes

| Title | Directory                | Scope                                                              |
|------:|--------------------------|--------------------------------------------------------------------|
| 82    | `82-excise-taxes/`       | B&O tax; sales/use tax; public utility tax; tax preferences         |
| 83    | `83-estate-taxation/`    | Washington estate tax                                               |
| 84    | `84-property-taxes/`     | Assessment; levy; exemptions; current-use valuation                 |

### Public health, safety, behavioral health, public assistance

| Title | Directory                                          | Scope                                                                  |
|------:|----------------------------------------------------|------------------------------------------------------------------------|
| 66    | `66-alcoholic-beverage-control/`                   | Liquor licensing; Liquor and Cannabis Board                            |
| 67    | `67-sports-and-recreation-convention-facilities/`  | Gambling; racing; convention facilities                                |
| 68    | `68-cemeteries-morgues-and-human-remains/`         | Cemeteries; anatomical gifts                                           |
| 69    | `69-food-drugs-cosmetics-and-poisons/`             | Controlled Substances Act; food safety; cannabis                       |
| 70    | `70-public-health-and-safety/`                     | Public health (legacy; see also 70A)                                   |
| 70A   | `70A-environmental-health-and-safety/`             | Environmental health; air/water quality; cleanup; climate              |
| 71    | `71-behavioral-health/`                            | Involuntary Treatment Act; civil commitment                            |
| 71A   | `71A-developmental-disabilities/`                  | Developmental disability services                                      |
| 72    | `72-state-institutions/`                           | DOC facilities; state hospitals; juvenile rehab                        |
| 73    | `73-veterans-and-veterans-affairs/`                | Veterans' homes and benefits                                           |
| 74    | `74-public-assistance/`                            | TANF; medical assistance; child welfare; adult protective services     |

### Natural resources, public lands, water

| Title | Directory                                | Scope                                                              |
|------:|------------------------------------------|--------------------------------------------------------------------|
| 76    | `76-forests-and-forest-products/`        | Forest Practices Act; state forest lands                           |
| 77    | `77-fish-and-wildlife/`                  | WDFW; hunting/fishing licenses; treaty rights                      |
| 78    | `78-mines-minerals-and-petroleum/`       | Mine safety; surface mining; oil and gas                           |
| 79    | `79-public-lands/`                       | State-owned lands; trust lands; aquatic lands                      |
| 79A   | `79A-public-recreational-lands/`         | State parks; scenic rivers                                         |
| 90    | `90-water-rights-environment/`           | Water rights; shorelines; State Environmental Policy Act           |

(For aeronautics — Title 14 — motor vehicles — 46 — public highways — 47 — insurance — 48 — labor regulations — 49 — unemployment compensation — 50 — paid family leave — 50A — and long-term care — 50B — see the sibling skill `rcw-1-50` at `../wa-rcw-1-50/`.)

## Directory layout

```
wa-rcw-51-100/
├── SKILL.md                                  ← you are here
├── .build_summary.json                       ← machine-readable per-Title stats
├── 51-industrial-insurance/
│   ├── README.md
│   └── rules.md
├── 52-fire-protection-districts/
│   ├── README.md
│   └── rules.md
... (one directory per Title, 42 total) ...
└── 91-waterways/
    ├── README.md
    └── rules.md
```

All paths in this skill are **relative** to this directory.

## Routing

For any RCW question in Titles 51–91, open the matching `README.md`
first. Each per-Title README has:

- A `description:` field with subject triggers, citation forms, and a
  "Do NOT use for" boundary.
- A **fidelity verdict** (FAITHFUL / FAITHFUL WITH MINOR CAVEATS).
- Grep patterns sized for that Title's `rules.md`.
- Citation conventions for that Title.

The glossary tables above are the routing index. If the user cites
`RCW {TT}.{NN}.{MMM}` where `{TT}` is 51–91 or one of the lettered
variants in this skill, open `{TT}-*/README.md` (use the table to find
the directory name). If `{TT}` is 1–50 or 9A/23B/28A-C/29A-B/30A-B/35A/50A-B,
route to the sibling skill `rcw-1-50` at `../wa-rcw-1-50/` instead.

## Cross-topic search

When you don't yet know which Title is relevant, grep across this half
of the corpus:

```bash
# A term anywhere in the 51–91 half
grep -rni 'unlawful detainer' --include='rules.md' .

# A specific statute cite (regex anchored to RCW citation form)
grep -rn -E 'RCW\s+59\.18\.030' --include='rules.md' .

# All chapter headings (every consolidated chapter in this half)
grep -rn -E '^## RCW ' --include='rules.md' . | head -40

# How many sections in this half reference a term
grep -rni 'water right' --include='rules.md' . | wc -l
```

If a subject-matter search returns nothing in this half, the topic may
live in Titles 1–50 — grep the sibling half at `../wa-rcw-1-50/`
(e.g. criminal code at 9A, probate at 11, K-12 at 28A, civil service
at 41, motor vehicles at 46, insurance at 48, paid leave at 50A).

Once you've narrowed the question to one Title, switch to that Title's
own `rules.md` for follow-up grep — it's much faster and the per-Title
README's grep patterns are tuned for it.

## Citation format

Standard RCW citation forms recognized inside `rules.md`:

- **Section**: `RCW 59.18.030` — Title 59, Chapter 18, Section 030.
- **Chapter**: `Chapter 59.18 RCW`.
- **Title**: `Title 59 RCW`.
- **UCC section** (Title 62A only): `RCW 62A.9A-313` — note the hyphen.
- **History note** (after each section body): `[2022 c 268 s 32; 2021 c
  215 s 89; 1996 c 134 s 7; ...]`.
- **Cross-references in notes**: appear in italic in the source PDF;
  in `rules.md` they appear as plain text on their own line.

Each chapter heading in `rules.md` is a Markdown H2 of the form
`## RCW {TT}.{NN} — {CHAPTER NAME}`. Section bodies appear underneath
with `RCW {TT}.{NN}.{MMM}` at the start of each section.

## Fidelity status

All 42 Titles in this half have either **FAITHFUL** or **FAITHFUL WITH
MINOR CAVEATS** verdicts; none required PDF-fallback rebuilds. Each
Title's per-README documents its own verdict.

- **FAITHFUL**: statute body, subsection lettering, and history-note
  brackets preserved cleanly. Cite directly.
- **FAITHFUL WITH MINOR CAVEATS** (Titles 51, 82, 84 in this half):
  body text is clean; tabular data (rate tables, fee schedules, multi-
  column listings) is preserved as space-aligned text rather than
  pipe-tables, so it is grep-able but not parseable as structured data.

No Title in this half is **DEGRADED**. The combined-Title PDF source
produces consistently clean `pdftotext -layout` output; the cleanup
pipeline (form-feed unification, page-footer strip, de-hyphenation,
blank-line collapse, chapter-heading injection) was identical across
all Titles.

**Title 62A quirk:** the Uniform Commercial Code uses hyphenated
section numbering (`RCW 62A.9A-313`). Source-PDF chapter boundaries
are `Article N`; these are normalized to `## RCW 62A.N` headings
during the build.

## Universal notes

- **Effective dates matter.** This snapshot is **2026-05-20**. Individual
  chapters were certified by the Legislature on dates printed in the
  source PDF page footers (typically mid-2024 through mid-2025) and
  those footers were stripped during cleanup. If a chapter's exact
  certification date is needed for evidentiary use, recover it from the
  Legislature's original Combined Title PDF (`RCW_Title_{NN[X]}_Complete.pdf`)
  at the provenance URL below.
- **Out-of-scope content lives in sibling skills**:
  - **RCW Titles 1–50 and lettered variants 9A / 23B / 28A–C / 29A–B
    / 30A–B / 35A / 50A–B** — sibling skill `rcw-1-50` at
    `../wa-rcw-1-50/`. Use that skill for general provisions, courts
    of record, civil procedure, evidence, crimes, criminal procedure,
    probate and trust, juvenile law, businesses and professions,
    corporations, partnerships, banking, domestic relations, schools
    and higher ed, elections and campaign finance, administrative law,
    cities and towns, counties, public officers, state government,
    aeronautics, motor vehicles, highways, insurance, labor and wages,
    unemployment, paid family leave, and long-term care.
  - **WAC** (Washington Administrative Code) regulations — sibling skill
    at `../wa-administrative-code/`.
  - **Washington state-wide court rules** (Civil Rules, Rules of
    Professional Conduct, appellate rules) — sibling skill at
    `../wa-state-court-rules/`.
  - **Washington county Superior Court local rules** — sibling skill at
    `../wa-county-superior-court-rules/`.
  - **Washington district court local rules** — sibling skill at
    `../wa-district-court-rules/`.
  - **Washington municipal court local rules** — sibling skill at
    `../wa-municipal-court-rules/`.
  - **Federal law** (USC, CFR) is not in this skill suite.
  - **Case law** interpreting the RCW is not in this skill suite.
  Direct the user to the canonical source for anything that falls
  outside both this skill and its siblings.
- **No body source from chapter HTML.** The Legislature's per-chapter
  HTML pages contain only section TOCs and chapter notes — not the
  statute body. This skill's `rules.md` files derive from the combined
  Title PDFs, which do contain the body.
- **This corpus is offline-only.** The local files are authoritative and
  the snapshot is fixed at 2026-05-20. Do not attempt to refetch from
  the web at runtime.

## Provenance

- **Source**: Washington State Legislature 2025 RCW Archive,
  `https://lawfilesext.leg.wa.gov/law/RCWArchive/2025/` (provenance only,
  for human re-derivation — this skill does not refetch at runtime).
- **Captured**: 2026-05-20.
- **Conversion**: `pdftotext -layout -enc UTF-8` over each per-Title
  combined PDF; chapter headings re-injected as Markdown H2; body
  cleanup pipeline applied uniformly.
