---
name: wa-municipal-court-rules
description: Use when the user asks about, looks up, cites, quotes, or compares a Washington State municipal court local rule — any municipal-rule abbreviation (LMCR, LMCRLJ, LCR, LCRLJ, LCrR, IMC/IMCR, SMCLR, SMCLIR, TMCLCR, TMCLGR, BMC, KMCR, RMCLR, AWHGR, DMMC, EMCR, FWMCR, KMCLR, LFPMC, MIMC, MMC, PMCR, RMC, SeaTac MCR, TMC, WMC, YMCR or a city-specific variant), or any phrase pairing a Washington city name with "municipal court rule", "local rule", "eFiling rule", "motion practice", "bail schedule", or "emergency rule." Routes to per-court READMEs in subdirectories. Also use for cross-court comparison among the 107 municipal courts in this corpus. Do NOT use for: Superior Court local rules (those are in a sibling corpus), district-court rules outside the documented shared-document set, state-promulgated rules (CRLJ, CrRLJ, IRLJ, RALJ, ARLJ, GR, ER, RPC, RAP), Washington Revised Code (RCW), or Washington Administrative Code (WAC).
---

# Washington State Municipal Court Rules

This skill answers questions from a curated, on-disk snapshot of Washington State **municipal court** local rules. It covers **107 municipal courts** across 25 of Washington's 39 counties, derived from the AOC Local Court Rules portal and a few city-hosted publishers as of **2026-05-20**. All answers are drawn from the local markdown files. **Do not fetch from the web.**

This is the router. **This is the only SKILL.md in the bundle.** Each municipal court has a `README.md` (not a SKILL.md) — these aren't separately registered skills; they're per-court playbooks this router instructs you to read.

For any court-specific question, read that court's `README.md` first — it documents the court's rule-abbreviation convention, fidelity verdict (FAITHFUL / MINOR CAVEATS / DEGRADED / PARTIAL), the exact files on hand, and court-specific caveats.

## How municipal court rules work in WA

Municipal courts are **city-run** courts of limited jurisdiction — they handle municipal code violations (city ordinances), criminal misdemeanors arising in the city, traffic infractions, parking, and small civil matters. They are separate from county-run district courts and from county Superior Courts. Each municipal court is created by city charter or ordinance; it adopts its own local rules that supplement the state-promulgated rules for courts of limited jurisdiction (CRLJ, CrRLJ, IRLJ, RALJ, ARLJ, GR).

**Most municipal courts publish their local rules through the WA Administrative Office of the Courts (AOC)** at `courts.wa.gov/court_rules/`. A few large or independent courts host their rules on their own city websites (Seattle, Tacoma, Port Orchard, Lynnwood, Colfax — see Special cases below). And **27 smaller municipal courts in this corpus operate under contract with the county district court** and use the county district court's rules document directly — see Shared documents below.

## Glossary of citation prefix patterns

Municipal courts use a wider variety of citation prefixes than state-level or Superior Court rules. Cities have adopted different conventions over time. Common patterns:

| Pattern              | Example courts                                  | What it means                                              |
|----------------------|------------------------------------------------|-------------------------------------------------------------|
| Bare `LMCR` / `LMCRLJ` | Many small/mid-size courts                    | "Local Municipal Court Rule" — generic                       |
| Bare `LCR` / `LCRLJ`   | Some smaller courts                            | "Local Court Rule" — generic, indistinguishable from district style without context |
| Bare `LCrR`            | Some smaller courts                            | "Local Criminal Rule"                                        |
| City-prefixed         | Seattle (`SMCLR`/`SMCLIR`), Tacoma (`TMCLCR`/`TMCLGR`), Bremerton (`BMC LCrRU`/`BMC LIRU`), Renton/Roy (`RMCLR`), Mercer Island (`MIMC`), Federal Way (`FWMCR`), Issaquah (`IMC`/`IMCR`), Des Moines (`DMMCLGR`/`DMMCLR`/`DMMCLIR`), Airway Heights (`AWHGR`/`AWHIRLJ`), Lake Forest Park (`LFPMCGR`/`LFPMCR`), Spokane (`SMC`-family) | City code embedded in the prefix |
| Numbered "Rule N"     | Bellingham, Bonney Lake, Centralia, Elma, Everett, Ferndale, Hoquiam, Lynden | No prefix at all — rules are simply numbered "Rule 1, Rule 2, ..." |
| Mandatory-eFiling singleton (LGR 30 / AMCLR 30 / South Bend Rule 22) | Aberdeen, Chehalis, Cle Elum, Lake Forest Park, Roslyn, South Bend | Statewide eFiling pattern adopted as a one-off ER, effective June/July 2026 |

**The per-court README is the authoritative source for that court's exact prefix.** Always read it before citing.

## Routing — by county

Municipal courts are organized geographically. The table below groups the 107 courts by the **county** they sit in. To answer a city-specific question, look up the city, open that court's `README.md`, then read `rules.md`.

| County        | Municipal courts (city slug → directory)                                                                                                    |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Asotin**    | `clarkston-municipal/`                                                                                                                       |
| **Clark**     | `battle-ground-municipal/` *(joint document also covers La Center & Ridgefield, which AOC does not list separately)*                         |
| **Columbia**  | `dayton-municipal/`                                                                                                                          |
| **Cowlitz**   | `castle-rock-municipal/`, `kalama-municipal/`, `kelso-municipal/`, `longview-municipal/`, `woodland-municipal/` — **all share `LCR_Cowlitz_DIS.pdf`** |
| **Douglas**   | `east-wenatchee-municipal/`                                                                                                                  |
| **Franklin**  | `pasco-municipal/`                                                                                                                           |
| **Grant**     | `coulee-city-municipal/`, `electric-city-municipal/`, `ephrata-municipal/`, `george-municipal/`, `grand-coulee-municipal/`, `mattawa-municipal/`, `moses-lake-municipal/`, `quincy-municipal/`, `royal-city-municipal/`, `soap-lake-municipal/`, `warden-municipal/` — **all 11 share `LCR_Grant_DIS.pdf`** |
| **Grays Harbor** | `aberdeen-municipal/`, `elma-municipal/`, `hoquiam-municipal/`, `montesano-municipal/`, `oakville-municipal/`, `ocean-shores-municipal/`, `westport-municipal/` |
| **Island**    | `coupeville-municipal/`, `langley-municipal/`, `oak-harbor-municipal/` — **all share `LCR_Island_DIS.pdf` (OCR-reconstructed)**              |
| **King**      | `algona-municipal/` *(shares King DIS)*, `black-diamond-municipal/`, `bothell-municipal/`, `des-moines-municipal/`, `enumclaw-municipal/`, `federal-way-municipal/`, `issaquah-municipal/`, `kent-municipal/`, `kirkland-municipal/`, `lake-forest-park-municipal/`, `maple-valley-municipal/`, `mercer-island-municipal/`, `normandy-park-municipal/`, `pacific-municipal/` *(shares King DIS)*, `renton-municipal/`, `seatac-municipal/`, `seattle-municipal/` *(HTML source)*, `tukwila-municipal/` |
| **Kitsap**    | `bainbridge-island-municipal/`, `bremerton-municipal/`, `port-orchard-municipal/` *(city-hosted)*, `poulsbo-municipal/`                       |
| **Kittitas**  | `cle-elum-municipal/`, `roslyn-municipal/`                                                                                                   |
| **Lewis**     | `centralia-municipal/`, `chehalis-municipal/`, `napavine-municipal/`, `winlock-municipal/`                                                   |
| **Mason**     | `shelton-municipal/`                                                                                                                         |
| **Okanogan**  | `brewster-municipal/`, `omak-municipal/`, `twisp-municipal/`, `winthrop-municipal/`                                                          |
| **Pacific**   | `south-bend-municipal/`                                                                                                                      |
| **Pierce**    | `bonney-lake-municipal/`, `buckley-municipal/`, `dupont-municipal/` *(shares Lakewood)*, `fife-municipal/`, `fircrest-municipal/`, `gig-harbor-municipal/`, `lakewood-municipal/`, `milton-municipal/`, `orting-municipal/` *(8 emergency rules)*, `puyallup-municipal/`, `roy-municipal/`, `ruston-municipal/`, `steilacoom-municipal/` *(shares Lakewood)*, `sumner-municipal/`, `tacoma-municipal/` *(base rules not published online — PARTIAL)* |
| **Skagit**    | `anacortes-municipal/`, `burlington-municipal/`, `mount-vernon-municipal/`, `sedro-woolley-municipal/` — **first three share `LCR_Skagit_DIS.pdf`** |
| **Skamania**  | `north-bonneville-municipal/`, `stevenson-municipal/` — **both use Skamania County District Court rules**                                    |
| **Snohomish** | `edmonds-municipal/`, `everett-municipal/`, `lynnwood-municipal/` *(city-hosted)*, `marysville-municipal/`, `monroe-municipal/`              |
| **Spokane**   | `airway-heights-municipal/`, `cheney-municipal/`, `spokane-municipal/`                                                                       |
| **Thurston**  | `olympia-municipal/`                                                                                                                         |
| **Whatcom**   | `bellingham-municipal/`, `blaine-municipal/`, `everson-nooksack-municipal/`, `ferndale-municipal/`, `lynden-municipal/`, `sumas-municipal/`  |
| **Whitman**   | `colfax-municipal/` *(scanned image, OCR'd — DEGRADED)*                                                                                      |
| **Yakima**    | `selah-municipal/`, `sunnyside-municipal/`, `wapato-municipal/`, `yakima-municipal/`, `zillah-municipal/`                                    |

**Counties NOT represented in this corpus** (no municipal court was listed on the AOC index at snapshot time): Adams, Benton, Chelan, Clallam, Ferry, Garfield, Jefferson, Klickitat, Lincoln, Pend Oreille, San Juan, Stevens, Wahkiakum, Walla Walla. If the user asks about a municipal court in one of these counties, say so explicitly — the AOC list did not include any municipal court there as of 2026-05-20.

## Shared documents — 27 courts use 6 shared PDFs

Smaller municipal courts often contract their judicial work to the county district court rather than publishing their own rules. In this corpus, **27 of the 107 courts have no court-specific rules document** — their `rules.md` is the county district court (or, in the Lakewood case, sibling municipal court) document. The README in each affected directory explains the sharing.

| Shared document          | Used by                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| `LCR_King_DIS.pdf`       | Algona, Pacific                                                                                         |
| `LCR_Skagit_DIS.pdf`     | Anacortes, Burlington, Mount Vernon                                                                     |
| `LCR_Cowlitz_DIS.pdf`    | Castle Rock, Kalama, Kelso, Longview, Woodland                                                          |
| `LCR_Grant_DIS.pdf`      | Coulee City, Electric City, Ephrata, George, Grand Coulee, Mattawa, Moses Lake, Quincy, Royal City, Soap Lake, Warden |
| `LCR_Island_DIS.pdf`     | Coupeville, Langley, Oak Harbor *(OCR-reconstructed from a scanned image PDF)*                          |
| `LCR_Lakewood_MUN.pdf`   | DuPont, Lakewood, Steilacoom *(Lakewood is the originating court; DuPont and Steilacoom adopt by contract)* |

When citing a rule from one of these 27 courts, the **rule text** is the shared document's text; the **citation** should still name the user's city (e.g., "Moses Lake Municipal Court LCR 7" rather than "Grant County District Court LCR 7") because that's where the rule operates.

## Special cases — read these notes before quoting

- **`seattle-municipal/`** — Rules are published as **HTML** on `seattle.gov`, not as a PDF. The `rules.md` consolidates the main HTML page (SMCLR + SMCLIR full text), two `.docx` monetary penalty schedules, three General Administrative Order (GAO) PDFs, and an HTML proposed-rules index. Fidelity: FAITHFUL WITH MINOR CAVEATS. The "proposed rules" section contains rule **proposals** for public comment, not adopted rules — do not quote those as authoritative.
- **`tacoma-municipal/`** — **The base TMCLCR rules are not published online** as of 2026-05-20. Confirmed by exhaustive probing of `tacoma.gov` and `cms.tacoma.gov`. The `rules.md` carries only the **emergency rule supplements** (2026 TMC emergency + 2025/2026 PCDC emergency that applies via contract) plus the city's municipal-court index page for context. Fidelity: **PARTIAL.** If the user asks for the base TMCLCR rule text, recommend they request a copy from the Tacoma Municipal Court clerk — it is not available digitally.
- **`colfax-municipal/`** — Source is a **scanned-image PDF with no text layer**. Reconstructed via Tesseract OCR. Fidelity: **DEGRADED.** Quotations should be verified against the original PDF; expect 0/O, 1/I/l, and 5/S confusion, joined-words artifacts, and table-layout linearization.
- **`port-orchard-municipal/`** — Rules document is hosted on `storage.googleapis.com` via `portorchardwa.gov`, not on the AOC site. Single PDF, FAITHFUL.
- **`lynnwood-municipal/`** — Hosted on `lynnwoodwa.gov`, not AOC. Single PDF (revised 2019), FAITHFUL.
- **`orting-municipal/`** — Has a **stack of 9 documents**: 1 base + 8 emergency-rule supplements. ER05 (effective 2025-07-07) is a full restatement that **explicitly supersedes** ER01–ER04; ER06–ER08 are successive revisions on top of ER05. When answering an Orting question, prefer ER08's text for any rule it touches; fall back to ER05; fall back to the base only for rules never touched by any ER. All 9 PDFs were OCR'd from image-only scans.
- **`battle-ground-municipal/`** — The same Battle Ground PDF also governs **La Center** and **Ridgefield** municipal courts (per the document's joint cover), but AOC does not list those two cities separately. There is no `la-center-municipal/` or `ridgefield-municipal/` directory; route La Center / Ridgefield questions to `battle-ground-municipal/`.
- **`everson-nooksack-municipal/`** — Single combined court for two cities (Everson + Nooksack).
- **`north-bonneville-municipal/` and `stevenson-municipal/`** — Both use the Skamania County District Court rules document; AOC routes them through `MUN/<city>/` paths that resolve to `LCR_Skamania_DIS.pdf`.

## Mandatory eFiling — the June/July 2026 pattern

Six courts in the corpus carry a 2026 emergency rule adopting **statewide mandatory eFiling** (LGR 30 / AMCLR 30 / LFPMCGR 30 / "Rule 22" depending on the court's nomenclature), effective **June 3, 2026** or **July 1, 2026**. The pattern courts are Aberdeen, Chehalis, Cle Elum, Lake Forest Park, Roslyn, South Bend. If the user asks about eFiling deadlines or requirements, the rule text is substantially similar across these six; the citation must match the court's own nomenclature.

## Looking up a rule

```bash
# A specific city + rule number (most common)
grep -n -A 60 -E 'LMCR ?7\b' federal-way-municipal/rules.md

# Cross-court comparison of a topic (e.g. motion practice across the corpus)
grep -rni --include='rules.md' -E 'motion.*continuance' .

# Find every court whose rules mention a specific RCW chapter
grep -rni --include='rules.md' 'RCW 35\.' .

# Emergency rules across the corpus
grep -rni --include='rules.md' -E '^## Emergency Rule' .

# Mandatory eFiling rule
grep -rni --include='rules.md' -E 'mandatory.{0,20}(eFiling|electronic filing)' .
```

When a user names a city, **prefer the per-court grep** (`grep -n -A 60 ... <slug>/rules.md`) over the cross-corpus form. Cross-corpus grep is for comparison questions, not single-court lookups.

## Directory layout

```
wa-municipal-court-rules/                       ← this is the skill root
├── SKILL.md                                    ← this file (the only SKILL.md in the bundle)
├── aberdeen-municipal/{README.md, rules.md}
├── airway-heights-municipal/{README.md, rules.md}
├── algona-municipal/{README.md, rules.md}
├── ...                                          ← 107 court directories in total
├── yakima-municipal/{README.md, rules.md}
└── zillah-municipal/{README.md, rules.md}
```

All paths in this skill are **relative** to this directory.

## Fidelity status (corpus-wide)

Spot-check verdicts across all 107 courts:

| Verdict                       | Count | Notes                                                                                       |
|-------------------------------|-------|---------------------------------------------------------------------------------------------|
| FAITHFUL                      | ~60   | Text-native PDF, clean pdftotext extraction. Cite directly.                                  |
| FAITHFUL WITH MINOR CAVEATS   | ~45   | Includes the ~30 courts whose source PDF was a scanned image and required Tesseract OCR. Body text reads cleanly; expect occasional glyph substitutions (e.g. `(£)` for `(f)`), and TOC dot-leader noise. The per-court README flags it. |
| PARTIAL                       | 1     | `tacoma-municipal/` — base rules not published online; only emergency rules captured.        |
| DEGRADED                      | 1     | `colfax-municipal/` — scanned image PDF, full OCR reconstruction. Verify quotes against the original. |

The per-court README is the authoritative verdict for that court; the table above is summary only.

## Citation format

Match each court's preferred prefix exactly (the per-court README documents it). Examples:

- `Seattle Municipal Court SMCLR 7(b)` *(HTML-sourced)*
- `Federal Way Municipal Court FWMCR 3.1`
- `Bremerton Municipal Court BMC LCrRU 4` *(literal space in the prefix — preserve)*
- `Moses Lake Municipal Court LCR 7` *(shared Grant County District document — cite by city, not by county)*
- `Orting Municipal Emergency Rule 08 (effective YYYY-MM-DD)`
- `Tacoma Municipal Court 2026 Emergency Local Rule §X` *(no base TMCLCR available)*

## Universal notes

- **Snapshot date: 2026-05-20.** Effective dates of underlying rules vary per court — read the per-court README. Some rules were last amended in 2019; some were adopted as 2026 emergency supplements. The municipal-court landscape is amended on rolling schedules. If currency matters for a filing-critical question, recommend the user reverify against the official source (AOC portal for most courts; the city site for the 5 city-hosted courts).
- **Out-of-scope content** — Superior Court local rules (sibling corpus), district-court rules outside the documented shared-document set, state-promulgated rules (CRLJ, CrRLJ, IRLJ, RALJ, ARLJ, GR, ER, RPC, RAP), Washington Revised Code (RCW), and Washington Administrative Code (WAC) are **not** in this corpus. Decline to answer those from this skill and direct the user to the appropriate sibling skill or canonical source.
- **Counties absent from this corpus** — see the routing table note above. If asked about a municipal court in Adams, Benton, Chelan, Clallam, Ferry, Garfield, Jefferson, Klickitat, Lincoln, Pend Oreille, San Juan, Stevens, Wahkiakum, or Walla Walla, say AOC did not list one at snapshot time; recommend the user check the current AOC list or contact the city directly.
- This corpus is **offline-only.** Never refetch from the web. The markdown is the source of truth.
