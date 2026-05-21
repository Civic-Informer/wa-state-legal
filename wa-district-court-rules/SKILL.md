---
name: wa-district-court-rules
description: Use when the user asks about, looks up, cites, quotes, or compares a Washington State district court (courts of limited jurisdiction) local rule — any district-court LCRLJ / LIRLJ / LCrRLJ / LARLJ / LRALJ / LMAR / LGR or county-prefixed variant (e.g. WWDGR for Walla Walla) attached to any of these 40 Washington district courts: Adams, Asotin, Benton, Chelan, Clallam I, Clallam II, Clark, Columbia, Cowlitz, Douglas, Ferry, Franklin, Garfield, Grant, Grays Harbor, Island, Jefferson, King, Kitsap, Klickitat West, Lewis, Lincoln, Lower Kittitas, Upper Kittitas, Mason, Pacific North, Pacific South, Pierce, San Juan, Skagit, Skamania, Snohomish, Spokane, Stevens, Thurston, Wahkiakum, Walla Walla, Whatcom, Whitman, Yakima. Also use for cross-court comparison and procedural questions tied to a specific district court (filing/venue routing, criminal procedure in courts of limited jurisdiction, infraction procedure, mandatory-appearance rules, mandatory arbitration, electronic-filing rules). Do NOT use for Superior Court LOCAL rules (those are in the sibling `wa-county-superior-court-rules/` skill), municipal-court LOCAL rules that aren't routed through a district court (those are in the sibling `wa-municipal-court-rules/` skill), the statewide CRLJ/IRLJ/CrRLJ/ARLJ/RALJ rules (sibling `wa-state-court-rules/`), RCW (sibling skills `wa-rcw-1-50/` and `wa-rcw-51-100/`), or WAC (sibling `wa-administrative-code/`).
---

# Washington State District Court Local Rules

This skill answers questions from a curated, on-disk snapshot of local court rules for 40 Washington district courts (the trial courts of limited jurisdiction, distinct from Superior Court). All answers are drawn from these local markdown files. **Do not fetch from the web.**

This is the router. **This is the only SKILL.md in the bundle.** Each district court has a `README.md` (not a SKILL.md) — these aren't separately registered skills; they're per-court playbooks this router instructs you to read.

For any court-specific question, read that court's `README.md` first — it documents the court's citation conventions, fidelity verdict (FAITHFUL / MINOR CAVEATS / PARTIAL), the exact files on hand, and court-specific caveats.

## Glossary — district-court citation prefixes

Washington district courts use the *limited-jurisdiction* (LJ) variants of the statewide rule families, plus court-specific local prefixes. Most courts use bare letters; Walla Walla prepends a `WW` prefix.

| Abbrev | Stands for | What it governs |
|--------|-----------|-----------------|
| LCRLJ  | Local Civil Rule (Limited Jurisdiction) | Civil procedure in district court |
| LIRLJ  | Local Infraction Rule (Limited Jurisdiction) | Civil & traffic infractions |
| LCrRLJ | Local Criminal Rule (Limited Jurisdiction) | Criminal procedure in district court |
| LARLJ  | Local Mandatory Arbitration Rule (Limited Jurisdiction) | Small-claim arbitration |
| LRALJ  | Local Rule for Appeal to Superior Court (Limited Jurisdiction) | RALJ appeals from district court |
| LMAR   | Local Mandatory Arbitration Rule | Some courts use this in place of LARLJ |
| LGR    | Local General Rule | Administrative, e.g. cameras, electronic filing |
| LCR / LCrR / LIR | Older/bare-prefix variants of LCRLJ / LCrRLJ / LIRLJ | Used in some courts (e.g. Lower Kittitas, Lewis) |
| WWDGR / WWDIR / WWDCR / WWDCrR | Walla Walla District { General / Infraction / Civil / Criminal } Rule | Walla Walla-specific local prefix |

Inside `rules.md` files we preserve whatever abbreviation the court itself prints. The directory name is descriptive English (e.g. `walla-walla/`); the citation prefix lives in the rule text.

## Routing

| Court | Read first | Verdict | Notes |
|-------|-----------|---------|-------|
| Adams County | `adams/README.md` | FAITHFUL WITH MINOR CAVEATS | eff. 2025-09-01 |
| Asotin County | `asotin/README.md` | FAITHFUL | eff. 2025-09-01 |
| Benton County | `benton/README.md` | FAITHFUL WITH MINOR CAVEATS | eff. 2025-09-01 |
| Chelan County | `chelan/README.md` | FAITHFUL WITH MINOR CAVEATS | eff. 2025-09-01 |
| Clallam County District Court 1 | `clallam-i/README.md` | FAITHFUL WITH MINOR CAVEATS | Multi-file: base rules + 1 emergency rule (ER01, eff. 2026-05-15) |
| Clallam County District Court 2 | `clallam-ii/README.md` | FAITHFUL | eff. 2025-09-01 |
| Clark County | `clark/README.md` | FAITHFUL | eff. 2025-09-01 |
| Columbia County | `columbia/README.md` | FAITHFUL | eff. 2025-09-01 |
| Cowlitz County | `cowlitz/README.md` | FAITHFUL | eff. 2025-09-01 |
| Douglas County | `douglas/README.md` | FAITHFUL | eff. 2025-09-01 |
| Ferry County | `ferry/README.md` | FAITHFUL | eff. 2025-09-01 |
| Franklin County | `franklin/README.md` | FAITHFUL WITH MINOR CAVEATS | eff. 2025-09-01 |
| Garfield County | `garfield/README.md` | FAITHFUL WITH MINOR CAVEATS | eff. 2025-09-01 |
| Grant County | `grant/README.md` | FAITHFUL WITH MINOR CAVEATS | STALE — last updated 2004-09-01 per courts.wa.gov index |
| Grays Harbor County | `grays-harbor/README.md` | FAITHFUL | eff. 2025-09-01 |
| Island County | `island/README.md` | FAITHFUL WITH MINOR CAVEATS | eff. 2025-09-01 |
| Jefferson County | `jefferson/README.md` | FAITHFUL | eff. 2025-09-01 |
| King County | `king/README.md` | FAITHFUL | eff. 2025-09-01 |
| Kitsap County | `kitsap/README.md` | FAITHFUL | eff. 2025-09-01 |
| Klickitat County West | `klickitat-west/README.md` | FAITHFUL | eff. 2025-09-01 |
| Lewis County | `lewis/README.md` | FAITHFUL | eff. 2025-09-01 |
| Lincoln County | `lincoln/README.md` | FAITHFUL | eff. 2025-09-01 |
| Lower Kittitas County | `lower-kittitas/README.md` | PARTIAL | PARTIAL — 11 individual rule PDFs only; no consolidated base on county website |
| Upper Kittitas County | `upper-kittitas/README.md` | FAITHFUL | Multi-file: base rules + 1 emergency rule (ER01, eff. 2026-04-29) |
| Mason County | `mason/README.md` | FAITHFUL | eff. 2025-09-01 |
| Pacific County North | `pacific-north/README.md` | PARTIAL | PARTIAL — only Rule 4 (venue) + emergency Rule 5 (DUI) published |
| Pacific County South | `pacific-south/README.md` | FAITHFUL WITH MINOR CAVEATS | Multi-file: base rules (2019) + 2 emergency rules (2026) |
| Pierce County | `pierce/README.md` | FAITHFUL | eff. 2024-08-21 |
| San Juan County | `san-juan/README.md` | FAITHFUL | eff. 2025-09-01 |
| Skagit County | `skagit/README.md` | FAITHFUL | eff. 2025-09-01 |
| Skamania County | `skamania/README.md` | FAITHFUL | eff. 2025-09-01 |
| Snohomish County | `snohomish/README.md` | FAITHFUL | eff. 2025-09-01 |
| Spokane County | `spokane/README.md` | FAITHFUL WITH MINOR CAVEATS | eff. 2025-09-01 |
| Stevens County | `stevens/README.md` | FAITHFUL | eff. 2025-09-01 |
| Thurston County | `thurston/README.md` | FAITHFUL | eff. 2025-09-01 |
| Wahkiakum County | `wahkiakum/README.md` | FAITHFUL WITH MINOR CAVEATS | Multi-file: base rules + 2 emergency rules (Jan + Apr 2026) |
| Walla Walla County | `walla-walla/README.md` | FAITHFUL | Source corrected: standard pattern URL, not the dynamic `ruleId=` URL |
| Whatcom County | `whatcom/README.md` | FAITHFUL | eff. 2025-09-01 |
| Whitman County | `whitman/README.md` | FAITHFUL | eff. 2025-09-01 |
| Yakima County | `yakima/README.md` | FAITHFUL WITH MINOR CAVEATS | 22 individual rule PDFs (no separate base); 6 are OCR'd; URL-slug typos noted in README |

**District court vs Superior Court vs municipal court (don't confuse them).** This corpus is *only* district courts — the county-level trial courts of limited jurisdiction that handle traffic infractions, misdemeanors, civil claims under $100,000, small claims, and limited civil. If the user asks about a **county Superior Court** local rule (felonies, civil over $100k, family law, juvenile court, probate), that's the sibling skill `wa-county-superior-court-rules/` — different rule numbers, different prefixes. If the user asks about a **city-run municipal court** local rule (city-ordinance prosecutions not routed through a district court), that's the sibling skill `wa-municipal-court-rules/`. Match the user's wording: "district court" / "justice court" / "municipal-routing through a district court" → this corpus; "superior court" / "family law" / "felony" → `wa-county-superior-court-rules/`; "municipal court" / "city ordinance" → `wa-municipal-court-rules/`.

## Multi-file stacks — read the supplements

These courts have more than one source PDF in their `rules.md`. Later supplements may modify or supersede the base — read in order.

| Court | Stack | What's in it |
|-------|-------|--------------|
| Clallam I | base + ER01 | Base rules + Emergency Rule 01 (eff. 2026-05-15) |
| Upper Kittitas | base + ER01 | Base rules (2025-09-01) + Emergency Rule 01 (eff. 2026-04-29) |
| Pacific South | base + ER01 + ER02 | Base rules (2019-07-09) + ER01 (2026-02-12) + ER02 (2026-05-11) |
| Wahkiakum | base + ER01 + ER02 | Base rules + ER01 (2026-01-23) + ER02 (2026-04-26) |
| Lower Kittitas | 11 rule PDFs | LCrR 4.5 + 3 forms, LCrR 7.2(f), LGR 17(a)(7), LGR 30, LGR 30(b)(4), LIR 3.1, LIR 3.5(f), LIR 6.6(e). No base ruleset. |
| Yakima | 22 rule PDFs | Individual L-ARLJ, L-CRLJ, L-CrRLJ, L-IRLJ rules from county DocumentCenter. No base ruleset. |

## Special cases — read before quoting

- **`adams`, `benton`, `chelan`, `clallam-i`, `franklin`, `garfield`, `island`, `lower-kittitas` (LGR 17, LIR 3.1), `pacific-north`, `pacific-south` (base), `spokane`, `wahkiakum` (ER01 + ER02), and 6 of 22 `yakima` files are OCR-derived** — scanned-image source PDFs with no text layer; isolated character substitutions (1/I/l, 0/O, `|`/I) are possible. Each affected README flags this in Caveats.
- **`pacific-north`** — `PARTIAL` verdict. Only Local Court Rule 4 (venue-routing between Pacific North and Pacific South) and an undated emergency Local Court Rule 5 (DUI mandatory appearance) are published; no consolidated base ruleset on courts.wa.gov.
- **`lower-kittitas`** — `PARTIAL` verdict. 11 individual rule PDFs on the county website (`co.kittitas.wa.us`); no consolidated base. Source URLs are heavily percent-encoded (`%20`, `%28`, `%29`) and preserved verbatim on disk.
- **`yakima`** — 22 individual rule PDFs from the county CivicEngage DocumentCenter (`yakimacounty.us/DocumentCenter/View/{id}/{slug}`). The page anchor text and URL slugs occasionally disagree (`L-RALJ-62` in the URL is actually `L-ARLJ 6.2`); the per-file headings in `rules.md` carry the corrected rule numbers.
- **`grant`** — base rules in this snapshot date to 2004-09-01 per the courts.wa.gov index. No newer revision has been published. Treat as `STALE`; verify with the court before relying on any rule.
- **`pacific-south`** — base rules date to 2019-07-09 (older than most). Two 2026 emergency rules are layered on top. The off-publisher amendment PDF the patch-index originally pointed at (`co.pacific.wa.us/.../2-2026-Local-Court-Rule-5.pdf`) turned out to be the same content as ER01 here, not a separate document.
- **`wahkiakum`** — base rules PDF exists on courts.wa.gov (contradicting the patch.md note that no base rules were published). No effective date is surfaced in the page metadata. Two emergency rules are also active.
- **`walla-walla`** — the courts.wa.gov dynamic URL (`?fa=court_rules.rulesPDF&ruleId=districtdiswaltable&pdf=1`) returns only a 1-page table of rules summary, NOT the rule bodies. This snapshot uses the standard-pattern path (`pdf/LCR/36/DIS/LCR_Walla_Walla_DIS.pdf`) instead. Walla Walla uses unusual `WWDGR` / `WWDIR` / `WWDCR` / `WWDCrR` prefixes.
- **`clallam-i`** — the ER01 source filename contains a literal space, URL-encoded as `LCR_Clallam%20I_DIS_ER01.pdf`. The on-disk filename preserves the `%20` verbatim.
- **`adams`** — uses non-standard `LCRLJ` / `LIRLJ` headings with a single flat ruleset (no LARLJ / LMAR family).

## District courts that include municipal-court matters

Several rural counties have district courts that also house the municipal courts of their cities under one set of rules. These are documented in the relevant `README.md`:

| District court | Embedded municipal courts |
|----------------|--------------------------|
| Grays Harbor   | McCleary Municipal Court |
| Island         | Oak Harbor, Coupeville, Langley |
| King           | Algona Municipal, Pacific Municipal |
| Skagit         | Anacortes, Burlington, Mount Vernon Municipal |
| Skamania       | Stevenson Municipal, North Bonneville Municipal |
| Stevens        | Chewelah, Colville, Kettle Falls, Springdale Municipal |
| Thurston       | Tumwater Municipal |
| Yakima         | Moxee, Union Gap Municipal |

If the user asks about one of these municipal courts and the question is procedural (filing, infractions, criminal-court calendar), the district court's rules typically govern — start with that district's `README.md`. Substantive ordinances and city-specific rules are in the `wa-municipal-court-rules` corpus.

## Directory layout

```
wa-district-court-rules/                       ← this is the skill root
├── SKILL.md                                   ← this file (the only SKILL.md in the bundle)
├── adams/{README.md, rules.md}
├── asotin/{README.md, rules.md}
├── benton/{README.md, rules.md}
├── chelan/{README.md, rules.md}
├── clallam-i/{README.md, rules.md}            base + ER01
├── clallam-ii/{README.md, rules.md}
├── clark/{README.md, rules.md}
├── columbia/{README.md, rules.md}
├── cowlitz/{README.md, rules.md}
├── douglas/{README.md, rules.md}
├── ferry/{README.md, rules.md}
├── franklin/{README.md, rules.md}
├── garfield/{README.md, rules.md}
├── grant/{README.md, rules.md}                STALE — 2004
├── grays-harbor/{README.md, rules.md}
├── island/{README.md, rules.md}
├── jefferson/{README.md, rules.md}
├── king/{README.md, rules.md}
├── kitsap/{README.md, rules.md}
├── klickitat-west/{README.md, rules.md}
├── lewis/{README.md, rules.md}
├── lincoln/{README.md, rules.md}
├── lower-kittitas/{README.md, rules.md}       PARTIAL — 11 discrete rule PDFs
├── upper-kittitas/{README.md, rules.md}       base + ER01
├── mason/{README.md, rules.md}
├── pacific-north/{README.md, rules.md}        PARTIAL — only Rule 4 + emergency Rule 5
├── pacific-south/{README.md, rules.md}        base + ER01 + ER02
├── pierce/{README.md, rules.md}
├── san-juan/{README.md, rules.md}
├── skagit/{README.md, rules.md}
├── skamania/{README.md, rules.md}
├── snohomish/{README.md, rules.md}
├── spokane/{README.md, rules.md}
├── stevens/{README.md, rules.md}
├── thurston/{README.md, rules.md}
├── wahkiakum/{README.md, rules.md}            base + ER01 + ER02
├── walla-walla/{README.md, rules.md}          WW-prefixed (WWDGR / WWDIR / WWDCR / WWDCrR)
├── whatcom/{README.md, rules.md}
├── whitman/{README.md, rules.md}
└── yakima/{README.md, rules.md}               22 discrete rule PDFs (no separate base)
```

All paths in this skill are **relative** to this directory.

## Cross-court search

```bash
# Find every court's rule on a topic
grep -rni 'mandatory appearance' --include='rules.md' .

# Every court's local civil rule 7 (motions). Prefix varies — this covers the common variants.
grep -rniE '\b(LCRLJ|LCR|LCrRLJ|LCrR|LCR LJ|WWDCR) ?7\b' --include='rules.md' .

# Every court's local infraction rule 3.5 (decision on written statements)
grep -rniE '\b(LIRLJ|LIR|WWDIR) ?3\.5' --include='rules.md' .

# Every court's RALJ-appeals rules
grep -rniE '\b(LRALJ|RALJ)' --include='rules.md' .
```

## Citation format

- Match the abbreviation the court itself prints in `rules.md`. Examples:
  - `Adams County District Court LCRLJ 65`
  - `King County District Court LCRLJ 7(b)(4)`
  - `Pierce County District Court LCrRLJ 3.1`
  - `Spokane County District Court LARLJ 6.2`
  - `Walla Walla County District Court WWDGR 16` (note the WW prefix)
  - `Yakima County District Court L-ARLJ 6.2` (Yakima uses hyphenated prefixes)
  - `Lower Kittitas District Court LGR 30(b)(4)` (Lower Kittitas uses bare LGR / LCrR / LIR)
  - `Wahkiakum County District Court ER01 (eff. 2026-01-23)` for an emergency rule supplement
- For multi-file courts (Clallam I, Upper Kittitas, Pacific South, Wahkiakum), specify which document a quoted rule comes from when ambiguous: e.g. `Pacific South LCR 5 (Emergency Rule 02, eff. 2026-05-11)`.
- Always quote rule text verbatim from `rules.md` and report the file path so the reader can verify.

## Fidelity status (corpus-wide)

| Verdict | Count | Items |
|---------|-------|-------|
| FAITHFUL | 26 | asotin, clallam-ii, clark, columbia, cowlitz, douglas, ferry, grays-harbor, jefferson, king, kitsap, klickitat-west, lewis, lincoln, upper-kittitas, mason, pierce, san-juan, skagit, skamania, snohomish, stevens, thurston, walla-walla, whatcom, whitman |
| FAITHFUL WITH MINOR CAVEATS | 12 | adams, benton, chelan, clallam-i, franklin, garfield, grant, island, pacific-south, spokane, wahkiakum, yakima |
| PARTIAL | 2 | lower-kittitas, pacific-north |
| DEGRADED | 0 | (none) |

The MINOR CAVEATS bucket is dominated by OCR-derived items (scanned PDFs from courts.wa.gov that don't carry a text layer). The substantive rule body of each OCR'd court has been spot-checked against the source PDF and reads faithfully; isolated character-level substitutions can appear, especially in form-templates and TOC dot-leaders.

## Universal notes

- **Snapshot date for this corpus:** 2026-05-20. Most base rules carry an effective date of 2025-09-01; Grant (2004-09-01) and Pacific South (2019-07-09) are the outliers.
- **District court ≠ Superior Court ≠ municipal court.** This corpus does not contain Superior Court or municipal-court local rules. For Superior Court LOCAL rules, route to the sibling `wa-county-superior-court-rules/` skill. For city municipal-court LOCAL rules, route to the sibling `wa-municipal-court-rules/` skill.
- **Statewide rules are out of scope.** CRLJ, IRLJ, CrRLJ, ARLJ, RALJ, GR, ER, RAP, RPC, etc. are in the sibling `wa-state-court-rules/` skill, not this one.
- **RCW and WAC are out of scope.** Route to whichever of `wa-rcw-1-50/` (skill `rcw-1-50`, Titles 1–50 plus 9A/23B/28A/28B/28C/29A/29B/30A/30B/35A/50A/50B) or `wa-rcw-51-100/` (skill `rcw-51-100`, Titles 51–91 plus 62A/70A/71A/79A) covers the Title for statutes, and `wa-administrative-code/` for agency regulations.
- **OCR-derived text can have character-level errors.** For the OCR'd items, the rule body has been spot-checked and reads faithfully; for verbatim quotation in briefs or motions, verify against the original source PDF at the URL printed in each court's README (provenance only — do not refetch programmatically).
- **Some rules are intentionally short.** "[Reserved]" / "[Rescinded]" entries are legitimately a few hundred bytes — that's not a scrape failure.
- **This corpus is offline-only. Never refetch from the web.** Source URLs in each README are provenance only.
