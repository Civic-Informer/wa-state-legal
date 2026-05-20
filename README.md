# Washington State Law — open-source Claude Code skills

A curated, on-disk snapshot of Washington State legal source material, packaged as installable Claude Code skills. Six sibling corpora live here, each with its own router `SKILL.md` and per-topic `README.md` playbooks. The goal is to make Washington's statutes, regulations, and court rules cite-able and queryable by an LLM **without** requiring it to fetch from the open web — the local markdown is the authoritative source for each skill.

| Directory | Skill | Covers |
|-----------|-------|--------|
| [`wa-rcw/`](./wa-rcw/) | `rcw` | **Revised Code of Washington** — full statute body text. 100 Titles, 2,764 chapters. |
| [`wa-administrative-code/`](./wa-administrative-code/) | `wac` | **Washington Administrative Code** — codified agency regulations. 227 published Titles, ~2,825 chapters. |
| [`wa-state-court-rules/`](./wa-state-court-rules/) | `wa-court-rules` | State-promulgated WA court rules (CR, CrR, GR, ER, RPC, CRLJ, CrRLJ, RALJ, ARLJ, RAP) plus U.S. District Court for the Western District of Washington (WAWD) Local Civil Rules. |
| [`wa-county-superior-court-rules/`](./wa-county-superior-court-rules/) | `wa-local-court-rules` | **Superior Court** local rules for 32 Washington counties, organized into 26 published rulesets (some adjacent counties share a combined ruleset). |
| [`wa-district-court-rules/`](./wa-district-court-rules/) | `wa-district-court-rules` | **District court** (courts of limited jurisdiction) local rules for 40 Washington district courts. |
| [`wa-municipal-court-rules/`](./wa-municipal-court-rules/) | `wa-municipal-court-rules` | **Municipal court** local rules for 107 city-run municipal courts across 25 of WA's 39 counties. |

Note: a couple of the skill names differ from their directory names — most prominently, `wa-county-superior-court-rules/` ships as the skill `wa-local-court-rules`, and `wa-administrative-code/` ships as `wac`. The table above is the source of truth for directory ↔ skill mapping.

## Disclaimer — not legal advice

**The authors are not lawyers.** Nothing in this repository is legal advice, and using these skills does not create an attorney-client relationship. The materials here are reference snapshots for research and informational use only. For any filing-critical, time-sensitive, or rights-affecting question, consult a licensed Washington attorney and verify the current rule, regulation, or statute against the official source. The skill bundles explicitly instruct Claude to recommend re-verification when currency matters — but that recommendation only goes as far as the user takes it.

## Snapshot date

All six corpora are dated **2026-05-20**. They are offline-authoritative for that date. The Washington Legislature, the Code Reviser's Office, and the courts amend statutes, regulations, and rules on an ongoing basis; this snapshot will drift. Re-derive when you need a fresher cut. Several corpora carry older effective dates beneath the snapshot date (see Known caveats).

## Sources

Every byte of legal text in this repo was derived from official government publishers. No third-party reporters, no headnotes, no annotations.

| Corpus | Official source |
|--------|----------------|
| RCW statute text | Washington State Legislature, **2025 RCW Archive** — per-Title "Complete Title" PDFs at `https://lawfilesext.leg.wa.gov/law/RCWArchive/2025/`. Chapter and TOC pages at `https://app.leg.wa.gov/RCW/`. |
| WAC regulation text | Washington State Legislature, **2025 WAC Archive** — per-chapter COMBINEDCHAPTER PDFs at `https://lawfilesext.leg.wa.gov/law/WACArchive/2025/`. |
| WA state court rules (CR, CrR, GR, ER, RPC, CRLJ, CrRLJ, RALJ, ARLJ, RAP) | Washington Courts, official court rules portal — `https://www.courts.wa.gov/court_rules/`. |
| WAWD federal local civil rules | U.S. District Court, Western District of Washington — `https://www.wawd.uscourts.gov/local-rules`. |
| County Superior Court local rules | Each county's local-rule listing on the Washington Courts portal: `https://www.courts.wa.gov/court_rules/?fa=court_rules.list&group=loc`. A few counties self-host on county-government sites (Spokane, Whitman, Lewis). |
| District court local rules | Washington Courts portal (same path), plus county-government sites for a small number of courts (Lower Kittitas at `co.kittitas.wa.us`). |
| Municipal court local rules | AOC Local Court Rules portal, plus city-hosted publishers (Seattle, Tacoma, Port Orchard, Lynnwood, Colfax). |

Per-corpus and per-topic `README.md` files inside each subdirectory document the specific files consulted, the fidelity verdict from spot-checks against the source PDF/HTML, and any caveats (running-footer noise, tracked-edit strikethrough artifacts, OCR substitutions, source-PDF typos preserved verbatim, etc.).

## Parsing strategy

The general pipeline was the same across all six corpora:

1. **Fetch official PDFs/HTML** from the publisher URLs above. For the RCW and WAC, the Legislature publishes per-Title or per-chapter PDFs; for state and county court rules, the publisher's site exposes one PDF (or HTML) per rule set.
2. **Extract text** with `pdftotext -layout -enc UTF-8` (Poppler). The `-layout` flag preserves columnar structure, which matters for subsection lettering, dollar figures, dates, and amendment markers. A small number of image-only PDFs required OCR; those topics are explicitly flagged in their READMEs.
3. **Consolidate per topic** — one `rules.md` / `local-rules.md` per chapter / rule set / court. Markdown headings mirror the source's section / rule numbering so citations resolve cleanly.
4. **Spot-check fidelity** against the source PDF/HTML, recording a verdict per topic in the topic's `README.md` (e.g. FAITHFUL, FAITHFUL WITH MINOR CAVEATS, OCR-DERIVED, PARTIAL, DEGRADED). Anything below FAITHFUL WITH MINOR CAVEATS is flagged so a downstream user can't silently rely on a defective extraction.
5. **Write the skill scaffolding** — a router `SKILL.md` at each corpus root, plus a per-topic `README.md` that documents which files exist, how the corpus prefers to be cited, and any per-topic caveats. The router's `description:` field is the trigger surface that gets the skill auto-loaded when a user cites a relevant rule, regulation, or statute.

The skill bundles **do not fetch from the web at runtime**. Source URLs are recorded for provenance and re-derivation, not for live retrieval.

## Using as Claude Code skills

Each subdirectory is a self-contained skill bundle. To install, copy each directory into your `~/.claude/skills/` tree under the skill name shown in the table above:

```
cp -r wa-rcw                          ~/.claude/skills/rcw
cp -r wa-administrative-code          ~/.claude/skills/wac
cp -r wa-state-court-rules            ~/.claude/skills/wa-court-rules
cp -r wa-county-superior-court-rules  ~/.claude/skills/wa-local-court-rules
cp -r wa-district-court-rules         ~/.claude/skills/wa-district-court-rules
cp -r wa-municipal-court-rules        ~/.claude/skills/wa-municipal-court-rules
```

Claude Code picks up each skill automatically when a user cites or paraphrases the relevant material (e.g. `RCW 4.16.080`, `WAC 296-126-040`, `CR 56`, `PCLR 7`, "Washington statute of limitations," "Pierce County motion deadline," "Seattle Municipal Court local rule"). The router `SKILL.md` then reads the appropriate per-topic `README.md` and answers from the on-disk markdown.

## Scope

**In:**
- Codified Washington **statutes** (RCW) — all 100 Titles, 2,764 chapters.
- Codified Washington **administrative regulations** (WAC) — all 227 published Titles.
- **State-promulgated court rules** (Supreme Court of Washington) — civil, criminal, evidence, professional conduct, appellate, limited-jurisdiction, and general administration.
- **WAWD federal Local Civil Rules** — the federal trial court for western Washington (Seattle/Tacoma). Federal districts outside the Western District (E.D. Wash., D. Idaho, D. Oregon) and the Ninth Circuit Rules are **not** included.
- **Superior Court local rules** for all 39 Washington counties (32 directories / 26 published rulesets — some adjacent counties share a combined ruleset, e.g. Asotin/Columbia/Garfield, Benton/Franklin, Ferry/Pend Oreille/Stevens, Klickitat/Skamania, Pacific/Wahkiakum).
- **District court local rules** for 40 Washington district courts (the trial courts of limited jurisdiction at the county level).
- **Municipal court local rules** for 107 city-run municipal courts across 25 of WA's 39 counties.

**Out:**
- Case law interpreting any of the above.
- Federal statutes (USC), federal regulations (CFR), and federal court rules outside WAWD.
- Washington session laws / chapter laws / pre-2025 historical versions of RCW or WAC.
- Local prosecutor/sheriff/clerk policies, administrative orders not promulgated as local rules, and bar-association style guides.

See each subdirectory's `SKILL.md` and `README.md` for full per-corpus scope, fidelity notes, and citation conventions.

## Known caveats

These are the items a public reader should know before relying on this corpus. Each sub-corpus README documents them in more detail.

### `wa-rcw/`
- 91 of 100 Titles are FAITHFUL. 9 Titles (36, 39, 41, 46, 47, 48, 51, 82, 84) are FAITHFUL WITH MINOR CAVEATS — large rate/fee tables are preserved as whitespace-aligned text, grep-able but not as structured pipe-tables. No Title is DEGRADED.
- **Title 62A quirk:** the Uniform Commercial Code uses hyphenated section numbering (`RCW 62A.9A-313`). Source-PDF chapter boundaries are `Article N`; these are normalized to `## RCW 62A.N` headings during the build.
- Reserved/skipped Titles (28, 29, 30, 45, 56, 62, 75) are intentionally absent — they were repealed or replaced by lettered variants.

### `wa-administrative-code/`
- 174 Titles FAITHFUL. 52 Titles are N/A — empty in the 2025 archive (historical or superseded agency designations); only a stub `rules.md` is present.
- 1 Title DEGRADED: **Title 237 (Natural Resources, Board on)** — its sole chapter `WAC 237-990` (Determination of Geographic Names appendix) 404'd on the Legislature's server; body text is missing, replaced with a placeholder.
- Wide fee/schedule tables are preserved as whitespace-aligned text, not GitHub-flavored pipe tables. Section subheadings may appear inline rather than as `###` headings. End-of-line hyphenation has been rejoined — verify exact spelling against the source PDF before block-quoting.
- WAC sections reference RCW chapters via statutory-authority brackets. Users citing `RCW …` want the `rcw` skill; users citing `WAC …` want this one.

### `wa-state-court-rules/`
- Rule sets covered: **CR** (96 rules), **CrR** (65), **GR** (58), **ER** (67), **RPC** (67), **CRLJ** (82), **CrRLJ** (76), **RALJ** (45), **ARLJ** (16), **RAP** (180), and bundled **WAWD** Local Civil Rules.
- **Federal boundary is WAWD only.** Do not extrapolate to other federal districts or to the Ninth Circuit.
- Every rule set is at minimum FAITHFUL WITH MINOR CAVEATS. Known form-layout degradations (ASCII-flattened — usable for keyword search, not authoritative as filing layouts): **CrR 4.2** plea form, **GR 14** appendix, **CrRLJ 4.2** DUI sentencing table, **RAP Form 17** PRP, and **WAWD LCR 37** sample pleading form. WAWD fee schedule is not embedded.
- `[Reserved]` / `[Rescinded]` entries are intentional (preserve numbering).
- Many rules cite RCW chapters (esp. RCW 5, RCW 10.77, RCW 46.61) and WAC sections; the statutory/regulatory text itself lives in the `rcw` and `wac` skills.

### `wa-county-superior-court-rules/` (skill: `wa-local-court-rules`)
- Snapshot dates are mostly **2025-09-01**, but several counties carry older effective dates: **Lewis** (2019-09-01, STALE), Chelan (2022-09-01), Benton/Franklin (2023-09-01), Kittitas (2023-09-01), Mason (2023-09-01).
- Fidelity: ~20 counties FAITHFUL, ~6 FAITHFUL WITH MINOR CAVEATS, 4 OCR-DERIVED with minor caveats (Asotin/Columbia/Garfield, Chelan, Clark, Kittitas), and **1 DEGRADED** — **Klickitat/Skamania** is a forms-heavy snapshot with sparse rule body text.
- Combined-county rulesets: `asotin-columbia-garfield/` (3 counties), `benton-franklin/`, `ferry-pend-oreille-stevens/` (3), `klickitat-skamania/`, `pacific-wahkiakum/`.
- Citation-prefix collisions worth flagging: `SCL-` is used by **both Skagit and Snohomish** for different rules — disambiguate by county. `WC*` family splits between **Whatcom** (`WCC-`/`WCA-`) and **Whitman** (`WCL-`).
- Idiosyncratic styles: **Adams** uses a flat `ACLR` ruleset (no LCR family); **Douglas** uses bare `LR` (not `LCR`); Pierce, Kitsap, Skagit, Snohomish, Walla Walla, and Whitman use county-prefixed families (`PCLR`, `KCLCR`, `SCLCR`, `WW-`, `WCL-`).
- Per-county content file is named `local-rules.md` (not `rules.md`).

### `wa-district-court-rules/`
- 40 district courts. Fidelity: **26 FAITHFUL, 12 FAITHFUL WITH MINOR CAVEATS, 2 PARTIAL, 0 DEGRADED.**
- **STALE court — `grant/`:** base rules date to **2004-09-01**; no later revision has been published by the court. Verify currency with the court before relying on any rule.
- **PARTIAL courts:** `pacific-north/` (only Local Court Rule 4 venue + emergency Rule 5 DUI; no consolidated base) and `lower-kittitas/` (11 discrete rule PDFs from `co.kittitas.wa.us`, no consolidated base).
- Older-than-most base: `pacific-south/` rules dated **2019-07-09** (layered with two 2026 emergency rules).
- Multi-court-per-county pattern: **Clallam I + Clallam II**, **Pacific North + Pacific South**, **Upper Kittitas + Lower Kittitas**, and **Klickitat West** (the only Klickitat district court the courts.wa.gov index publishes).
- **Walla Walla** uses a unique `WW-` prefix family (`WWDGR / WWDIR / WWDCR / WWDCrR`); every other court uses bare `LCRLJ / LIRLJ / LCrRLJ / LARLJ`. Yakima hyphenates (`L-CRLJ`); Lower Kittitas + Lewis use older bare `LCR / LCrR / LIR` (no `LJ` suffix).
- Multi-file rule stacks (read in order): Clallam I (base + ER01), Upper Kittitas (base + ER01), Pacific South (base + ER01 + ER02), Wahkiakum (base + ER01 + ER02), Lower Kittitas (11 PDFs, no base), Yakima (22 PDFs, no base).
- Eight district courts also house embedded municipal-court calendars (Grays Harbor, Island, King, Skagit, Skamania, Stevens, Thurston, Yakima).
- **Yakima URL-slug quirk:** county DocumentCenter slugs occasionally disagree with the actual rule number (e.g. URL `L-RALJ-62` is actually `L-ARLJ 6.2`); in-file headings carry the corrected numbers.

### `wa-municipal-court-rules/`
- 107 city-run municipal courts across **25 of WA's 39 counties** (14 counties are absent — they have no represented municipal court).
- **Shared-document pattern:** 27 of 107 courts share six county-level PDFs (`LCR_King_DIS`, `LCR_Skagit_DIS`, `LCR_Cowlitz_DIS`, `LCR_Grant_DIS` covering 11 cities, `LCR_Island_DIS` OCR'd, `LCR_Lakewood_MUN`). Their `rules.md` is the county district-court text verbatim; citing by city is still correct.
- **Joint-coverage outliers:** the Battle Ground PDF also governs **La Center and Ridgefield** (no separate directories); `everson-nooksack-municipal/` is a single combined court; **North Bonneville + Stevenson** share `LCR_Skamania_DIS.pdf`.
- **DEGRADED:** `colfax-municipal/` (OCR of a scanned image — verify quotes against the city-hosted PDF).
- **PARTIAL:** `tacoma-municipal/` (the base TMCLCR ruleset isn't published online; only 2026 emergency rules + Pierce County DC emergency rules are captured). Orting stacks nine emergency-rule documents — ER05 supersedes ER01–04, then ER06–ER08 layer on top; pick the latest.
- **Prefix diversity:** bare `LMCR / LCR / LCrR`, city-prefixed (Seattle `SMCLR`, Tacoma `TMCLCR`, Bremerton `BMC LCrRU`, Federal Way `FWMCR`, Issaquah `IMC`, Des Moines `DMMC`, Airway Heights `AWHGR`, Lake Forest Park `LFPMC`), numbered-only "Rule N" (Bellingham et al.), and statewide mandatory-eFiling singletons (LGR 30 / AMCLR 30 / "Rule 22") effective June–July 2026.
- **Format outliers:** Seattle is HTML-sourced (plus DOCX penalty schedules and three GAO PDFs); Port Orchard and Lynnwood are city-hosted PDFs.

## License

[MIT](./LICENSE) for the scaffolding, organization, and markdown extractions. The underlying statutory, regulatory, and court-rule text is uncopyrightable government-edict material — see the note at the bottom of the `LICENSE` file for the *Georgia v. Public.Resource.Org* / *Banks v. Manchester* basis. Contributions, additional jurisdictions, and fidelity bug reports welcome via PR or issue.
