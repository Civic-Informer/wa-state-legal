---
name: rcw
description: Use when the user asks about, cites, quotes, paraphrases, or compares Washington State statute law — the Revised Code of Washington (RCW). Triggers on citations like `RCW 4.16.080`, `RCW 9A.36.011`, `Chapter 62A.9A RCW`, "Washington statute," "state law in Washington," or any subject-matter query (statute of limitations, wrongful death, B&O tax, landlord-tenant, criminal sentencing, etc.) that maps to a Washington Title. Routes the request to the relevant Title's `README.md` for grep-able statute text. Do NOT use for: WAC implementing regulations (sibling skill `wa-administrative-code`), Washington court rules (sibling skills `wa-state-court-rules`, `wa-county-superior-court-rules`, `wa-district-court-rules`, `wa-municipal-court-rules`), federal statutes (out of scope), or case law interpreting the RCW (out of scope).
---

# Revised Code of Washington — Skill-Routed Corpus

This skill answers questions from a curated, on-disk snapshot of the
**Washington State Legislature's 2025 RCW Archive**, captured on
**2026-05-20**. The corpus is an offline, citable snapshot — its
contents are fixed as of the snapshot date. Do not attempt to refetch
from the web at runtime; the local files are authoritative.

This is the **router**. It is the only `SKILL.md` in the bundle. Each
RCW Title has its own subdirectory containing a `README.md` (per-Title
playbook this router instructs you to read) and a `rules.md` (the
consolidated statute body for that Title). Per-Title `README.md` files
are **not** separately registered skills — they are documents this
router tells you to open.

For any topic-specific question, follow the routing table below to the
Title's `README.md` first; that file lists the chapter cites inside its
`rules.md` and shows the grep patterns to extract specific sections.

## What this corpus contains

- **100 Titles** of the RCW, covering every Title number published in the
  2025 archive (Titles 1–91 numeric, plus lettered Titles 9A, 23B, 28A,
  28B, 28C, 29A, 29B, 30A, 30B, 35A, 50A, 50B, 62A, 70A, 71A, 79A).
- **2,764 chapters** consolidated from the Legislature's per-Title
  "Complete Title" PDFs.
- **~96 MB** of grep-able markdown across the corpus.

The source body is the Legislature's combined per-Title PDF (one PDF per
Title, containing the full chapter-by-chapter text). The per-chapter HTML
pages from the Legislature's site contain only section TOCs and chapter
notes — **the actual statute body lives only in the PDFs**, so the PDFs
are the canonical source for `rules.md`.

## Title numbers absent from the archive

These Title numbers do not exist in the RCW and have no directory here:

- `28`, `29`, `30` — replaced by their lettered variants (28A/28B/28C,
  29A/29B, 30A/30B).
- `45`, `56`, `62`, `75` — no longer assigned / reserved.

(Title 23 still exists, distinct from Title 23B.)

## Glossary — Title number → directory name

Directory names use plain-English kebab-case. The bare Title number is
what a lawyer types in citations; the directory name is what the file
tree shows. Both are useful.

### Civil, criminal, judicial

| Title | Directory                                              | Scope (one line)                                                                       |
|------:|--------------------------------------------------------|----------------------------------------------------------------------------------------|
| 1     | `01-general-provisions/`                               | General definitions; rules of construction                                             |
| 2     | `02-courts-of-record/`                                 | Supreme Court, Court of Appeals, superior courts                                       |
| 3     | `03-district-courts-courts-of-limited-jurisdiction/`   | District courts; courts of limited jurisdiction                                        |
| 4     | `04-civil-procedure/`                                  | Civil procedure; statute of limitations; wrongful death; anti-SLAPP                    |
| 5     | `05-evidence/`                                         | Rules of evidence; privileges; witness competency                                      |
| 6     | `06-enforcement-of-judgments/`                         | Judgment liens; executions; garnishment; exemptions                                    |
| 7     | `07-special-proceedings-and-actions/`                  | Mandamus, prohibition, quo warranto; arbitration; protection orders                    |
| 8     | `08-eminent-domain/`                                   | Condemnation; takings; compensation                                                    |
| 9     | `09-crimes-and-punishments/`                           | General crimes (predecessor to 9A)                                                     |
| 9A    | `09A-washington-criminal-code/`                        | Washington Criminal Code (codified offenses; mens rea; defenses)                       |
| 10    | `10-criminal-procedure/`                               | Arrest; bail; trial; post-conviction relief                                            |
| 11    | `11-probate-and-trust-law/`                            | Wills; intestate succession; trusts; guardianship; TEDRA                               |
| 12    | `12-district-courts-civil-procedure/`                  | Civil procedure in district courts                                                     |
| 13    | `13-juvenile-courts-and-juvenile-offenders/`           | Dependencies, terminations, juvenile offenses                                          |

### Agriculture, animals, food

| Title | Directory                                                | Scope                                            |
|------:|----------------------------------------------------------|--------------------------------------------------|
| 15    | `15-agriculture-and-marketing/`                          | Commodity commissions; agricultural marketing   |
| 16    | `16-animals-and-livestock/`                              | Animal cruelty; livestock; dangerous dogs       |
| 17    | `17-weeds-rodents-and-pests/`                            | Weed districts; pesticides; noxious weeds       |
| 20    | `20-commission-merchants-agricultural-products/`         | Commission merchants                            |
| 22    | `22-warehousing-and-deposits/`                           | Warehousing; grain elevators                    |

### Business, banking, commerce

| Title | Directory                                                              | Scope                                                              |
|------:|------------------------------------------------------------------------|--------------------------------------------------------------------|
| 18    | `18-businesses-and-professions/`                                       | Occupational licensing (physicians, lawyers, contractors, etc.)    |
| 19    | `19-business-regulations-miscellaneous/`                               | Consumer Protection Act; advertising; telemarketing                |
| 21    | `21-securities-and-investments/`                                       | Securities; broker-dealers; investment advisers                    |
| 23    | `23-corporations-and-associations-profit/`                             | Profit corporations (legacy)                                       |
| 23B   | `23B-washington-business-corporation-act/`                             | WBCA — formation, governance, mergers, dissolution                 |
| 24    | `24-corporations-and-associations-nonprofit/`                          | Nonprofit corporations; unincorporated associations                |
| 25    | `25-partnerships/`                                                     | RUPA; limited partnerships; LLPs                                   |
| 30A   | `30A-washington-commercial-bank-act/`                                  | State-chartered banks                                              |
| 30B   | `30B-washington-trust-institutions-act/`                               | Trust companies                                                    |
| 31    | `31-miscellaneous-loan-agencies/`                                      | Small loans; payday lending; check cashers                         |
| 32    | `32-washington-savings-bank-act/`                                      | Savings banks                                                      |
| 33    | `33-washington-savings-association-act/`                               | Savings associations                                               |
| 62A   | `62A-uniform-commercial-code/`                                         | UCC — sales, leases, negotiable instruments, secured transactions  |

### Family, education, libraries, elections

| Title | Directory                                            | Scope                                                              |
|------:|------------------------------------------------------|--------------------------------------------------------------------|
| 26    | `26-domestic-relations/`                             | Marriage; dissolution; parenting plans; child support; parentage   |
| 27    | `27-libraries-museums-and-historical-activities/`    | Libraries; museums; historical societies                           |
| 28A   | `28A-common-school-provisions/`                      | K-12 schools; districts; certification; school finance             |
| 28B   | `28B-higher-education/`                              | Universities; community colleges; financial aid                    |
| 28C   | `28C-vocational-education/`                          | Vocational and workforce training                                  |
| 29A   | `29A-elections/`                                     | Voter registration; ballots; recounts; recall                      |
| 29B   | `29B-campaign-disclosure-and-contribution/`          | Campaign finance; Public Disclosure Commission                     |

### Government structure

| Title | Directory                                                | Scope                                                            |
|------:|----------------------------------------------------------|------------------------------------------------------------------|
| 34    | `34-administrative-law/`                                 | Administrative Procedure Act; rulemaking; judicial review        |
| 35    | `35-cities-and-towns/`                                   | Cities and towns; municipal governance                           |
| 35A   | `35A-optional-municipal-code/`                           | Optional Municipal Code                                          |
| 36    | `36-counties/`                                           | County government; county officers; county fees                  |
| 37    | `37-federal-areas-indians/`                              | Federal lands; state-tribal relations                            |
| 38    | `38-militia-and-military-affairs/`                       | Washington National Guard; military service protections          |
| 39    | `39-public-contracts-and-indebtedness/`                  | Public works; bidding; prevailing wages; bonds                   |
| 40    | `40-public-documents-records-and-publications/`          | Public records (technical); publication requirements             |
| 41    | `41-public-employment-civil-service-and-pensions/`       | Civil service; PERS / TRS / LEOFF / PSERS                        |
| 42    | `42-public-officers-and-agencies/`                       | Open Public Meetings Act; Public Records Act; ethics             |
| 43    | `43-state-government-executive/`                         | Governor; executive agencies (DSHS, Ecology, Commerce, …)        |
| 44    | `44-state-government-legislative/`                       | Legislature; codes reviser; redistricting                        |

### Transportation, utilities, insurance, labor

| Title | Directory                                          | Scope                                                                |
|------:|----------------------------------------------------|----------------------------------------------------------------------|
| 14    | `14-aeronautics/`                                  | Aeronautics; airports; drones                                        |
| 46    | `46-motor-vehicles/`                               | Driver licensing; vehicle registration; rules of the road; DUI       |
| 47    | `47-public-highways-and-transportation/`           | WSDOT; highways; ferries; tolling                                    |
| 48    | `48-insurance/`                                    | Insurance regulation; health insurance; surplus lines; captives      |
| 49    | `49-labor-regulations/`                            | Wages and hours; minimum wage; paid sick leave; OSHA                 |
| 50    | `50-unemployment-compensation/`                    | Unemployment insurance                                               |
| 50A   | `50A-family-and-medical-leave/`                    | Paid Family and Medical Leave                                        |
| 50B   | `50B-long-term-care/`                              | WA Cares (Long-Term Services and Supports Trust)                     |
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

### Property, real estate, recording, taxes

| Title | Directory                                                       | Scope                                                              |
|------:|-----------------------------------------------------------------|--------------------------------------------------------------------|
| 58    | `58-boundaries-and-plats/`                                      | Surveys; plats; subdivisions; condominiums                          |
| 59    | `59-landlord-and-tenant/`                                       | Residential Landlord-Tenant Act; unlawful detainer; mobile homes    |
| 60    | `60-liens/`                                                     | Mechanic's, materialman's, garage keeper's, agricultural liens      |
| 61    | `61-mortgages-deeds-of-trust-and-real-estate-contracts/`        | Foreclosure (judicial and nonjudicial)                              |
| 63    | `63-personal-property/`                                         | Sales; replevin; unclaimed property; gift cards                     |
| 64    | `64-real-property-and-conveyances/`                             | Deeds; covenants; easements; condominiums                           |
| 65    | `65-recording-registration-and-legal-publication/`              | Auditor recording; real-estate excise tax                           |
| 82    | `82-excise-taxes/`                                              | B&O tax; sales/use tax; public utility tax; tax preferences         |
| 83    | `83-estate-taxation/`                                           | Washington estate tax                                               |
| 84    | `84-property-taxes/`                                            | Assessment; levy; exemptions; current-use valuation                 |

### Public health, safety, behavioral health

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

### Natural resources, public lands

| Title | Directory                                | Scope                                                              |
|------:|------------------------------------------|--------------------------------------------------------------------|
| 76    | `76-forests-and-forest-products/`        | Forest Practices Act; state forest lands                           |
| 77    | `77-fish-and-wildlife/`                  | WDFW; hunting/fishing licenses; treaty rights                      |
| 78    | `78-mines-minerals-and-petroleum/`       | Mine safety; surface mining; oil and gas                           |
| 79    | `79-public-lands/`                       | State-owned lands; trust lands; aquatic lands                      |
| 79A   | `79A-public-recreational-lands/`         | State parks; scenic rivers                                         |
| 90    | `90-water-rights-environment/`           | Water rights; shorelines; State Environmental Policy Act           |

## Directory layout

```
wa-rcw/
├── SKILL.md                                  ← you are here
├── .build_summary.json                       ← machine-readable per-Title stats
├── 01-general-provisions/
│   ├── README.md
│   └── rules.md
├── 02-courts-of-record/
│   ├── README.md
│   └── rules.md
... (one directory per Title, 100 total) ...
├── 90-water-rights-environment/
│   ├── README.md
│   └── rules.md
└── 91-waterways/
    ├── README.md
    └── rules.md
```

All paths in this skill are **relative** to this directory.

## Routing

For any RCW question, open the matching `README.md` first. Each
per-Title README has:

- A `description:` field with subject triggers, citation forms, and a
  "Do NOT use for" boundary.
- A **fidelity verdict** (FAITHFUL / FAITHFUL WITH MINOR CAVEATS).
- Grep patterns sized for that Title's `rules.md`.
- Citation conventions for that Title.

The glossary tables above are the routing index. If the user cites
`RCW {TT}.{NN}.{MMM}`, open `{TT}-*/README.md` (use the table to find
the directory name).

## Cross-topic search

When you don't yet know which Title is relevant, grep across the whole
corpus:

```bash
# A term anywhere in the corpus
grep -rni 'wrongful death' --include='rules.md' .

# A specific statute cite (regex anchored to RCW citation form)
grep -rn -E 'RCW\s+4\.20\.020' --include='rules.md' .

# All chapter headings (every consolidated chapter across all Titles)
grep -rn -E '^## RCW ' --include='rules.md' . | head -40

# How many sections in the corpus reference a term
grep -rni 'community property' --include='rules.md' . | wc -l
```

Once you've narrowed the question to one Title, switch to that Title's
own `rules.md` for follow-up grep — it's much faster and the per-Title
README's grep patterns are tuned for it.

## Citation format

Standard RCW citation forms recognized inside `rules.md`:

- **Section**: `RCW 4.16.080` — Title 4, Chapter 16, Section 080.
- **Chapter**: `Chapter 4.16 RCW`.
- **Title**: `Title 4 RCW`.
- **UCC section** (Title 62A only): `RCW 62A.9A-313` — note the hyphen.
- **History note** (after each section body): `[2022 c 268 s 32; 2021 c
  215 s 89; 1996 c 134 s 7; ...]`.
- **Cross-references in notes**: appear in italic in the source PDF;
  in `rules.md` they appear as plain text on their own line.

Each chapter heading in `rules.md` is a Markdown H2 of the form
`## RCW {TT}.{NN} — {CHAPTER NAME}`. Section bodies appear underneath
with `RCW {TT}.{NN}.{MMM}` at the start of each section.

## Fidelity status

All 100 Titles have either **FAITHFUL** or **FAITHFUL WITH MINOR
CAVEATS** verdicts; none required PDF-fallback rebuilds. Each Title's
per-README documents its own verdict.

- **FAITHFUL** (91 Titles): statute body, subsection lettering, and
  history-note brackets preserved cleanly. Cite directly.
- **FAITHFUL WITH MINOR CAVEATS** (9 Titles — those with substantial
  rate or fee tables: 36, 39, 41, 46, 47, 48, 51, 82, 84): body text
  is clean; tabular data (rate tables, fee schedules, multi-column
  listings) is preserved as space-aligned text rather than pipe-tables,
  so it is grep-able but not parseable as structured data.

No Title was **DEGRADED**. The combined-Title PDF source produces
consistently clean `pdftotext -layout` output; the cleanup pipeline
(form-feed unification, page-footer strip, de-hyphenation, blank-line
collapse, chapter-heading injection) was identical across all Titles.

## Universal notes

- **Effective dates matter.** This snapshot is **2026-05-20**. Individual
  chapters were certified by the Legislature on dates printed in the
  source PDF page footers (typically mid-2024 through mid-2025) and
  those footers were stripped during cleanup. If a chapter's exact
  certification date is needed for evidentiary use, recover it from the
  Legislature's original Combined Title PDF (`RCW_Title_{NN[X]}_Complete.pdf`)
  at the provenance URL below.
- **Out-of-scope content lives in sibling skills**:
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
