---
name: wa-local-court-rules
description: Use when the user asks about, looks up, cites, quotes, or compares a Washington State county Superior Court local rule — any local rule abbreviation (LCR/LCrR/LFLR/LJuCR/LGR/LCAR/LMAR/LRALJ/LSPR/LGALR or any county-prefixed variant like PCLR/WCCR/KCLCR/SCLCR/CCLCR/WWLCR/WCLCR/ACLR/LR) attached to any of these 32 Washington counties: Adams, Asotin, Benton, Chelan, Clallam, Clark, Columbia, Cowlitz, Douglas, Ferry, Franklin, Garfield, Grant, Grays Harbor, Island, Jefferson, King, Kitsap, Kittitas, Klickitat, Lewis, Lincoln, Mason, Okanogan, Pacific, Pend Oreille, Pierce, San Juan, Skagit, Skamania, Snohomish, Spokane, Stevens, Thurston, Wahkiakum, Walla Walla, Whatcom, Whitman, Yakima. Also use for cross-county comparison and for procedural questions tied to a specific county's Superior Court (motion deadlines, family-law procedure, criminal procedure, arbitration). This corpus is **exclusively Superior Court (county trial court) local rules**. Do NOT use for: statewide rules promulgated by the Washington Supreme Court (CR, CrR, RAP, ER, RPC, GR — those live in the sibling `wa-state-court-rules/` skill); district-court local rules (sibling `wa-district-court-rules/`); municipal-court local rules (sibling `wa-municipal-court-rules/`); RCW (sibling skills `wa-rcw-1-50/` and `wa-rcw-51-100/`); or WAC (sibling `wa-administrative-code/`).
---

# Washington State Superior Court Local Rules

This skill answers questions from a curated, on-disk snapshot of **Superior Court** local rules for 32 Washington county Superior Courts (organized into 26 published rulesets, since some adjacent counties share a combined ruleset). Superior Courts are Washington's county-level trial courts of general jurisdiction. The statewide rules promulgated by the **Washington Supreme Court** (CR, CrR, RAP, GR, ER, RPC, etc.) are out of scope here — those live in the sibling `wa-state-court-rules/` skill. District-court and municipal-court local rules also live in their own sibling skills (`wa-district-court-rules/`, `wa-municipal-court-rules/`). All answers in this skill are drawn from local markdown files in this directory. Do not fetch from the web.

This is the router. **This is the only SKILL.md in the bundle.** Each county (or combined-county) directory has a `README.md` (not a SKILL.md) — these aren't separately registered skills; they're per-county playbooks this router instructs you to read.

For any county-specific question, read that county's `README.md` first — it documents the county's rule-abbreviation convention, fidelity verdict (FAITHFUL / MINOR CAVEATS / DEGRADED), the exact files on hand, and county-specific caveats.

## Routing

| County / Court                | Read first                                | Citation prefix                                                |
|-------------------------------|-------------------------------------------|----------------------------------------------------------------|
| Adams                         | `adams/README.md`                         | **ACLR** (single flat ruleset, Rule 1-N — no LCR family)        |
| Asotin / Columbia / Garfield  | `asotin-columbia-garfield/README.md`      | LCR, LCrR, LGR, LJuCR, LSPR, LGALR (bare) — *OCR'd, MINOR CAVEATS* |
| Benton / Franklin             | `benton-franklin/README.md`               | LCR, LCAR, LCrR, LGR, LFLR, LSPR (bare) — *2023 snapshot*       |
| Chelan                        | `chelan/README.md`                        | LCR, LCrR, LGR, LMAR, LGALR, LAR (bare) — *OCR'd, MINOR CAVEATS; **2022 snapshot*** |
| Clallam                       | `clallam/README.md`                       | LCR, LCrR, LMAR, LGALR, LRALJ, LAR (bare)                       |
| Clark (WA)                    | `clark/README.md`                         | LCR, LCrR, LCAR, LGALR, LSPR (bare) — *OCR'd, MINOR CAVEATS*    |
| Cowlitz                       | `cowlitz/README.md`                       | **CC-** prefix: CCLGR, CCLAR, CCLCR, CCLCrR, CCLGALR, CCLSPR    |
| Douglas                       | `douglas/README.md`                       | bare **LR** (not LCR), LCrR, LSPR                               |
| Ferry / Pend Oreille / Stevens| `ferry-pend-oreille-stevens/README.md`    | LCR, LCrR, LAR, LJuCR, LRALJ (bare)                             |
| Grant                         | `grant/README.md`                         | LCR, LCrR, LAR, LRALJ (bare)                                    |
| Grays Harbor                  | `grays-harbor/README.md`                  | LCR, LCrR, LGR, LGALR, LMAR, LRALJ, LJuCR (bare)                |
| Island                        | `island/README.md`                        | LCR, LFLR, LCrR, LJuCR, LSPR (bare)                             |
| Jefferson                     | `jefferson/README.md`                     | LCR, LCrR, LFLR, LGR, LCAR, LRALJ, LSPR (bare)                  |
| King                          | `king/README.md`                          | LCR, LFLR, LGR, LCrR, LCAR, LJuCR, LGALR, LMPR, LRALJ (bare)    |
| Kitsap                        | `kitsap/README.md`                        | **KCLCR, KCLAR** + emergency rule supplements                   |
| Kittitas                      | `kittitas/README.md`                      | LCR/LGR (or GLR), LCrR, LMAR, LGALR, LSPR (bare) — *OCR'd, MINOR CAVEATS; **2023 snapshot*** |
| Klickitat / Skamania          | `klickitat-skamania/README.md`            | LMAR + forms-heavy snapshot — *DEGRADED*                        |
| Lewis                         | `lewis/README.md`                         | LCR, LCrR, LAR, LMAR, LSPR (bare) — *2019 snapshot, STALE*      |
| Lincoln                       | `lincoln/README.md`                       | LCR, LCrR, LAR (bare)                                           |
| Mason                         | `mason/README.md`                         | LCR, LSCCAR, LSPR, LGAL, LCrR, LJuCR, LRALJ, LGR (bare)         |
| Okanogan                      | `okanogan/README.md`                      | LCR, LCrR, LMAR, LGALR, LSPR (bare)                             |
| Pacific / Wahkiakum           | `pacific-wahkiakum/README.md`             | LCR, LCrR, LGR, LGALR, LAR (bare)                               |
| Pierce                        | `pierce/README.md`                        | **PCLR, PCLSCCAR, PCLAPR, PCLGR, PCLSPR, PCLCRR**               |
| San Juan                      | `san-juan/README.md`                      | LCR, LCrR, LGR, LJuCR (bare)                                    |
| Skagit                        | `skagit/README.md`                        | **SCL-** prefix: SCLAR, SCLGR, SCLCR, SCLCrR, SCLFLR, SCLGALR    |
| Snohomish                     | `snohomish/README.md`                     | **SCL-** prefix: SCLCR, SCLSPR + emergency rule supplements      |
| Spokane                       | `spokane/README.md`                       | LCR, LCrR, LGR, LAR, LJuCR, LSCCAR, LSPR, LRALJ (bare)          |
| Thurston                      | `thurston/README.md`                      | LCR, LFLR, LCrR, LJuCR, LSPR, LGR (bare)                        |
| Walla Walla                   | `walla-walla/README.md`                   | **WW-** prefix: WWLAR, WWLGR, WWLCR, WWLCrR, WWLSPR, WWLJuCR, WWLGALR |
| Whatcom                       | `whatcom/README.md`                       | **WCCR, WCAR** (Whatcom-prefixed)                                |
| Whitman                       | `whitman/README.md`                       | **WCL-** prefix: WCLAR, WCLCR, WCLCrR, WCLFLR, WCLGALR           |
| Yakima                        | `yakima/README.md`                        | LCR, LCrR, LFLR, LGR, LCAR, LJuCR, LAR, LRALJ (bare)            |

**Counties use different prefixes.** Most counties use bare LCR / LFLR / LCrR / etc. Some prepend a county code: PCL- (Pierce), KCL- (Kitsap), CC- (Cowlitz), SCL- (Skagit + Snohomish — disambiguate by county!), WW- (Walla Walla), WCL- (Whitman), WCC-/WCA- (Whatcom). Adams uses a one-of-a-kind flat **ACLR** ruleset; Douglas uses a bare **LR** (not LCR). Match the county's own convention when citing.

### Critical prefix collisions

- **`SCL-` prefix** is used by both **Skagit** and **Snohomish**. Always disambiguate by the county the user named. The rule numbering schemes differ — never carry a rule from one to the other.
- **`WC*` prefix** family: **Whatcom** uses WCCR / WCAR (Whatcom County Court Rules / Whatcom County Arbitration Rules). **Whitman** uses WCLAR / WCLCR / WCLCrR / WCLFLR. The third letter distinguishes them (Whatcom: WCC- / WCA-; Whitman: WCL-).
- **`CC*` prefix**: **Cowlitz** uses CCLAR / CCLCR / CCLCrR. (Not currently shared with any other county in the corpus.)

**Routing rule:** when the user names a county, read that county's `README.md` before searching files. Kitsap and Snohomish in particular have emergency rule supplements that override the main rules — the per-county README explains which file to consult.

## Directory layout

```
wa-county-superior-court-rules/                     ← this is the skill root
├── SKILL.md                                        ← this file (the only SKILL.md in the bundle)
├── adams/{README.md, local-rules.md}
├── asotin-columbia-garfield/{README.md, local-rules.md}
├── benton-franklin/{README.md, local-rules.md}
├── chelan/{README.md, local-rules.md}
├── clallam/{README.md, local-rules.md}
├── clark/{README.md, local-rules.md}
├── cowlitz/{README.md, local-rules.md}
├── douglas/{README.md, local-rules.md}
├── ferry-pend-oreille-stevens/{README.md, local-rules.md}
├── grant/{README.md, local-rules.md}
├── grays-harbor/{README.md, local-rules.md}
├── island/{README.md, local-rules.md}
├── jefferson/{README.md, local-rules.md}
├── king/{README.md, local-rules.md}
├── kitsap/
│   ├── README.md
│   ├── local-rules.md
│   └── emergency-rule-0{1..8}.md                   8 supplements
├── kittitas/{README.md, local-rules.md}
├── klickitat-skamania/{README.md, local-rules.md}
├── lewis/{README.md, local-rules.md}
├── lincoln/{README.md, local-rules.md}
├── mason/{README.md, local-rules.md}
├── okanogan/{README.md, local-rules.md}
├── pacific-wahkiakum/{README.md, local-rules.md}
├── pierce/{README.md, local-rules.md}
├── san-juan/{README.md, local-rules.md}
├── skagit/{README.md, local-rules.md}
├── snohomish/
│   ├── README.md
│   ├── local-rules.md
│   └── emergency-rule-0{1..9}.md                   9 supplements (only 5 unique — see snohomish/README.md)
├── spokane/{README.md, local-rules.md}
├── thurston/{README.md, local-rules.md}
├── walla-walla/{README.md, local-rules.md}
├── whatcom/{README.md, local-rules.md}
├── whitman/{README.md, local-rules.md}
└── yakima/{README.md, local-rules.md}
```

All paths in this skill are **relative** to this directory. If a county README says "see `local-rules.md`", it means the sibling file inside that county's folder.

## Cross-county search

For "find every county's rule on X" or comparisons, grep across every county's main file:

```bash
# Match across every county's main file (run from this directory)
grep -rni "summary judgment" --include='local-rules.md' .

# Headings only — every county's rule 7 (motions). Prefix varies by county; this
# regex covers the common variants.
grep -rniE '^\s*\*?\*?(ACLR|PCLR|WCCR|KCLCR|SCLCR|CCLCR|WWLCR|WCLCR|LCR|LR) ?7\b' --include='*.md' .

# All counties' criminal rule 3.1 (right to counsel)
grep -rniE '(PCLCrR|KCLCrR|CCLCrR|WWLCrR|WCLCrR|SCLCrR|LCrR) ?3\.1' --include='local-rules.md' .
```

## Citation format

- Match the rule-set abbreviation the county itself uses. Examples:
  - `Adams County ACLR 1(C)` (Adams uses a flat ACLR set, not LCR families)
  - `Pierce County PCLR 7(b)(4)`
  - `Whatcom County WCCR 7.2(b)`
  - `Whitman County WCLCR 1(a)` (different from Whatcom — note the WCL- prefix)
  - `Kitsap County KCLCR 77(k)(11)`
  - `Snohomish County SCLCR 7(b)(9)`
  - `Skagit County SCLCR 7(b)` (also SCL-; disambiguate by county name)
  - `Cowlitz County CCLCR 40(b)`
  - `Walla Walla County WWLCR 7(b)`
  - `Douglas County LR 56(j)` (bare LR, not LCR)
  - `King County LCR 7(b)(4)(B)`
- For Kitsap and Snohomish emergency supplements, name the emergency rule explicitly: `Snohomish SCLCR 30 (Emergency Rule 02, eff. 8/13/2025)`.

Always quote rule text verbatim from `local-rules.md` (or the relevant supplement) and report the file path so the reader can verify.

## Fidelity status of this corpus

- **FAITHFUL** (clean text-based PDF): adams, douglas, ferry-pend-oreille-stevens, grant, grays-harbor, lincoln, okanogan, pacific-wahkiakum, spokane, walla-walla, whitman, yakima, king, mason, whatcom, island, kitsap, pierce, thurston, snohomish.
- **FAITHFUL WITH MINOR CAVEATS** (clean conversion + small layout quirks): benton-franklin, clallam, cowlitz, jefferson, san-juan, skagit.
- **FAITHFUL WITH MINOR CAVEATS — OCR-derived** (rule body verified faithful by spot-check against source PDF; isolated character substitutions in TOC/forms): asotin-columbia-garfield, chelan, clark, kittitas. See each county's README for the specific OCR error patterns observed.
- **DEGRADED** (forms-heavy snapshot, sparse rule body): klickitat-skamania.
- **STALE / OLDER SNAPSHOT** (clean conversion but the published PDF predates the courts.wa.gov index "effective date"):
  - lewis — 2019-09-01 (2026 revision in public comment but not yet effective)
  - chelan — 2022-09-01 (despite "Sep 1, 2025" listing)
  - benton-franklin — 2023-09-01 (despite "Sep 1, 2023" — earliest 2023, courts.wa.gov has not republished)
  - kittitas — 2023-09-01 (despite "Sep 1, 2025" listing)
  - mason — 2023-09-01

See each county's `README.md` "Caveats" section for specifics.

## Universal notes

- **Effective dates matter.** Each per-county `README.md` lists the snapshot date. Most counties are Sept 1, 2025; Mason is Sept 1, 2023; Benton/Franklin is Sept 1, 2023; Lewis is Sept 1, 2019 (oldest, flag staleness).
- **Statewide Supreme Court rules (CR, CrR, RAP, ER, RPC, GR), RCW, WAC, and district/municipal court local rules are not in this corpus.** Decline to answer those from this skill; the sibling skills (`wa-state-court-rules/`, `wa-rcw-1-50/` (RCW Titles 1–50), `wa-rcw-51-100/` (RCW Titles 51–91), `wa-administrative-code/`, `wa-district-court-rules/`, `wa-municipal-court-rules/`) cover them.
- **OCR-derived text can have character-level errors.** For the four OCR counties (asotin-columbia-garfield, chelan, clark, kittitas), the rule body has been spot-checked and is faithful for substantive citation; for verbatim quotation in briefs, verify against the source PDF. See each county's README for the specific OCR-error patterns observed.
- **Some rules are intentionally short.** "[Rescinded]" / "[Reserved]" entries are legitimately a few hundred bytes; that's not a scrape failure.
- **This corpus is offline-only. Never refetch from the web.**
