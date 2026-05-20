---
name: wac
description: Use when the user cites, quotes, asks about, or compares any chapter or section of the Washington Administrative Code (WAC) — Washington State's body of agency regulations. Triggers on citations like 'WAC 4-30-040', 'chapter 173-201A WAC', 'Title 388 WAC', 'WAC section', and on agency-rule questions for Washington state agencies (DSHS, Ecology, Health, L&I, Licensing, Revenue, Fish & Wildlife, OFM, Insurance Commissioner, UTC, etc.). Routes to per-title READMEs. Do NOT use for RCW (Revised Code of Washington) statutes — those are a separate corpus; do NOT use for federal Code of Federal Regulations (CFR); do NOT use for city or county ordinances; do NOT use for court rules.
---

# Washington Administrative Code (WAC) — 2025 Archive

This skill answers questions from a curated, on-disk snapshot of the WAC. Do not fetch from the web.

This is the router. **This is the only SKILL.md in the bundle.** Each Title has its own subdirectory containing a `README.md` (per-title playbook) and `rules.md` (full-text body of every chapter in that Title). For any title-specific question, read that title's `README.md` first.

**Effective date of this snapshot:** 2026-05-20.

**Coverage:** 227 WAC Titles, 2825 chapter combined-PDF bodies consolidated from the 2025 archive (one upstream chapter PDF was 404 on the legislature's server — a non-standard appendix in Title 237).

## What this corpus contains

Each `rules.md` is built from the per-chapter `COMBINEDCHAPTER.pdf` files in the WAC 2025 archive — one PDF per chapter containing the full body of every section in that chapter, with section subheadings, subsection numbering, and statutory-authority history brackets preserved. Conversion is `pdftotext -layout -enc UTF-8` followed by a cleanup pass that drops form-feeds, strips per-page `Certified on M/D/YYYY ... Page N` footers, rejoins lowercase end-of-line hyphenation, and collapses 3+ blank lines to 2. Each patched topic directory also keeps a `rules.md.toc.bak` containing the prior section-index-only `rules.md` for cross-checking that every section the TOC promised appears in the new body text.

Not consolidated into any `rules.md` (upstream artifacts kept by the corpus builder, not shipped with the public skill):
- The official 2025 WAC General Index PDF — useful for finding which Title/chapter governs a topic when grep fails. Available from the Washington State Legislature.
- The 2,825 source `COMBINEDCHAPTER.pdf` files and cleaned `.txt` intermediates the body text was built from. Not redistributed; refer to the legislature's WAC archive if you need to verify against the source PDFs.

## Routing by subject area

Every Title gets its own per-title README. Categories below are a navigation aid; the canonical address for a regulation is its Title number (e.g. Title 173 = Department of Ecology).

### Government Operations & Elections

| Title | Agency | Chapters | Read first |
|-------|--------|----------|------------|
| 1 | Code Reviser, Office Of The | 3 | `001-code-reviser-office-of-the/README.md` |
| 34 | Asian Pacific American Affairs, Commission On | 2 | `034-asian-pacific-american-affairs-commission-on/README.md` |
| 44 | Attorney General'S Office | 4 | `044-attorney-generals-office/README.md` |
| 48 | Auditor, Office Of State | 3 | `048-auditor-office-of-state/README.md` |
| 240 | Governor, Office Of The | 4 | `240-governor-office-of-the/README.md` |
| 251 | Personnel, Department Of | 0 | `251-personnel-department-of/README.md` |
| 292 | Ethics In Public Service | 6 | `292-ethics-in-public-service/README.md` |
| 322 | Hispanic Affairs, Commission On | 1 | `322-hispanic-affairs-commission-on/README.md` |
| 326 | Minority And Women'S Business Enterprises, Office Of | 8 | `326-minority-and-womens-business-enterprises-office-of/README.md` |
| 356 | Personnel, Department Of (General Government) | 0 | `356-personnel-department-of-general-government/README.md` |
| 357 | Financial Management, Office Of-State Human Resources Director | 18 | `357-financial-management-office-of-state-human-resources-director/README.md` |
| 358 | Personnel Appeals Board | 5 | `358-personnel-appeals-board/README.md` |
| 359 | Personnel, Department Of | 0 | `359-personnel-department-of/README.md` |
| 390 | Public Disclosure Commission | 12 | `390-public-disclosure-commission/README.md` |
| 417 | Redistricting Commission | 3 | `417-redistricting-commission/README.md` |
| 434 | Secretary Of State | 42 | `434-secretary-of-state/README.md` |

### Financial Services

| Title | Agency | Chapters | Read first |
|-------|--------|----------|------------|
| 4 | Accountancy, Board Of | 1 | `004-accountancy-board-of/README.md` |
| 50 | Financial Institutions, | 0 | `050-financial-institutions/README.md` |
| 184 | Employees' Retirement System, Public | 0 | `184-employees-retirement-system-public/README.md` |
| 186 | Employees' Retirement, Statewide Cities | 0 | `186-employees-retirement-statewide-cities/README.md` |
| 208 | Financial Institutions, Department Of | 34 | `208-financial-institutions-department-of/README.md` |
| 226 | Freight Mobility Strategic Investment Board | 2 | `226-freight-mobility-strategic-investment-board/README.md` |
| 263 | Industrial Insurance Appeals, Board Of | 1 | `263-industrial-insurance-appeals-board-of/README.md` |
| 284 | Insurance Commissioner | 73 | `284-insurance-commissioner/README.md` |
| 287 | Investment Board, State | 4 | `287-investment-board-state/README.md` |
| 290 | Judicial Retirement Board | 0 | `290-judicial-retirement-board/README.md` |
| 374 | Pollution Liability Insurance Agency | 9 | `374-pollution-liability-insurance-agency/README.md` |
| 415 | Retirement Systems, Department Of | 21 | `415-retirement-systems-department-of/README.md` |
| 419 | Financial Institutions, Department Of | 0 | `419-financial-institutions-department-of/README.md` |
| 460 | Financial Institutions, Department Of | 23 | `460-financial-institutions-department-of/README.md` |
| 462 | Teachers' Retirement | 0 | `462-teachers-retirement/README.md` |

### Revenue, Tax & Gaming

| Title | Agency | Chapters | Read first |
|-------|--------|----------|------------|
| 140 | Convention And Trade Center | 2 | `140-convention-and-trade-center/README.md` |
| 210 | State Treasurer'S Office | 4 | `210-state-treasurers-office/README.md` |
| 230 | Gambling Commission | 16 | `230-gambling-commission/README.md` |
| 314 | Liquor And Cannabis Board | 42 | `314-liquor-and-cannabis-board/README.md` |
| 315 | Lottery Commission | 14 | `315-lottery-commission/README.md` |
| 389 | State Treasurer'S Office | 1 | `389-state-treasurers-office/README.md` |
| 456 | Tax Appeals, Board Of | 3 | `456-tax-appeals-board-of/README.md` |
| 458 | Revenue, Department Of | 23 | `458-revenue-department-of/README.md` |
| 474 | State Treasurer'S Office | 3 | `474-state-treasurers-office/README.md` |

### Commerce, Housing & Utilities

| Title | Agency | Chapters | Read first |
|-------|--------|----------|------------|
| 130 | Commerce, Department Of | 4 | `130-commerce-department-of/README.md` |
| 133 | Commerce, Department Of | 4 | `133-commerce-department-of/README.md` |
| 194 | Commerce, Department Of | 11 | `194-commerce-department-of/README.md` |
| 262 | Housing Finance Commission | 3 | `262-housing-finance-commission/README.md` |
| 365 | Commerce, Department Of | 28 | `365-commerce-department-of/README.md` |
| 399 | Commerce, Department Of | 6 | `399-commerce-department-of/README.md` |
| 463 | Energy Facility Site Evaluation Council | 26 | `463-energy-facility-site-evaluation-council/README.md` |

### Labor & Workforce

| Title | Agency | Chapters | Read first |
|-------|--------|----------|------------|
| 192 | Employment Security Department | 57 | `192-employment-security-department/README.md` |
| 288 | Jail Industries Board | 3 | `288-jail-industries-board/README.md` |
| 296 | Labor And Industries, Department Of | 121 | `296-labor-and-industries-department-of/README.md` |

### Licensing & Professions

| Title | Agency | Chapters | Read first |
|-------|--------|----------|------------|
| 36 | Licensing, Department Of | 3 | `036-licensing-department-of/README.md` |
| 98 | Licensing, Department Of | 0 | `098-licensing-department-of/README.md` |
| 181 | Professional Educator Standards Board | 14 | `181-professional-educator-standards-board/README.md` |
| 196 | Engineers And Land Surveyors, Board Of Registration For Professional | 13 | `196-engineers-and-land-surveyors-board-of-registration-for-professional/README.md` |
| 308 | Licensing, Department Of | 85 | `308-licensing-department-of/README.md` |

### Health & Human Services

| Title | Agency | Chapters | Read first |
|-------|--------|----------|------------|
| 55 | Basic Health Plan | 0 | `055-basic-health-plan/README.md` |
| 67 | Blind, Department Of Services For The | 6 | `067-blind-department-of-services-for-the/README.md` |
| 110 | Children, Youth, And Families, Department Of | 34 | `110-children-youth-and-families-department-of/README.md` |
| 113 | Chiropractic Disciplinary Board | 0 | `113-chiropractic-disciplinary-board/README.md` |
| 114 | Chiropractic Examiners, Board Of | 0 | `114-chiropractic-examiners-board-of/README.md` |
| 148 | Deaf And Hard Of Hearing Youth, Center For | 9 | `148-deaf-and-hard-of-hearing-youth-center-for/README.md` |
| 162 | Human Rights Commission | 14 | `162-human-rights-commission/README.md` |
| 182 | Health Care Authority | 91 | `182-health-care-authority/README.md` |
| 243 | Health Care Policy Board | 1 | `243-health-care-policy-board/README.md` |
| 245 | Health Services Commission | 0 | `245-health-services-commission/README.md` |
| 246 | Health, Department Of | 186 | `246-health-department-of/README.md` |
| 247 | Health Care Facilities Authority | 5 | `247-health-care-facilities-authority/README.md` |
| 248 | Health, Board And Division Of | 0 | `248-health-board-and-division-of/README.md` |
| 261 | Hospital Commission | 0 | `261-hospital-commission/README.md` |
| 275 | Social And Health Services, Department Of (Institutions) | 0 | `275-social-and-health-services-department-of-institutions/README.md` |
| 320 | Medical Disciplinary Board | 0 | `320-medical-disciplinary-board/README.md` |
| 360 | Pharmacy, Board Of | 0 | `360-pharmacy-board-of/README.md` |
| 388 | Social And Health Services, | 126 | `388-social-and-health-services/README.md` |
| 440 | Social And Health Services, Department Of | 0 | `440-social-and-health-services-department-of/README.md` |

### Education — K-12 & Education Boards

| Title | Agency | Chapters | Read first |
|-------|--------|----------|------------|
| 3 | Academic Achievement And Accountability Commission | 0 | `003-academic-achievement-and-accountability-commission/README.md` |
| 14 | Advanced Tuition Payment, Committee On | 7 | `014-advanced-tuition-payment-committee-on/README.md` |
| 180 | Education, State Board Of | 14 | `180-education-state-board-of/README.md` |
| 249 | Higher Education Assistance Authority | 0 | `249-higher-education-assistance-authority/README.md` |
| 249A | Higher Education, Joint Center For | 1 | `249A-higher-education-joint-center-for/README.md` |
| 250 | Student Achievement Council | 30 | `250-student-achievement-council/README.md` |
| 253 | Higher Education Facilities Authority | 3 | `253-higher-education-facilities-authority/README.md` |
| 392 | Public Instruction, Superintendent Of | 81 | `392-public-instruction-superintendent-of/README.md` |
| 490 | Workforce Training And Education Coordinating Board, Also Vocational Rehabilitation | 8 | `490-workforce-training-and-education-coordinating-board-also-vocational-rehabilitation/README.md` |

### Education — Community & Technical Colleges

| Title | Agency | Chapters | Read first |
|-------|--------|----------|------------|
| 132A | Community Colleges-Peninsula College | 16 | `132A-community-colleges-peninsula-college/README.md` |
| 132B | Community Colleges-Grays Harbor College | 11 | `132B-community-colleges-grays-harbor-college/README.md` |
| 132C | Olympic College | 6 | `132C-olympic-college/README.md` |
| 132D | Skagit Valley College | 13 | `132D-skagit-valley-college/README.md` |
| 132E | Everett Community College | 12 | `132E-everett-community-college/README.md` |
| 132F | Seattle Colleges | 18 | `132F-seattle-colleges/README.md` |
| 132G | Shoreline Community College | 15 | `132G-shoreline-community-college/README.md` |
| 132H | Bellevue College | 15 | `132H-bellevue-college/README.md` |
| 132I | Highline College | 21 | `132I-highline-college/README.md` |
| 132J | Community Colleges-Green River College | 9 | `132J-community-colleges-green-river-college/README.md` |
| 132K | Pierce College | 13 | `132K-pierce-college/README.md` |
| 132L | Centralia College | 11 | `132L-centralia-college/README.md` |
| 132M | Lower Columbia College | 9 | `132M-lower-columbia-college/README.md` |
| 132N | Clark College | 11 | `132N-clark-college/README.md` |
| 132P | Community Colleges-Yakima Valley Community College | 10 | `132P-community-colleges-yakima-valley-community-college/README.md` |
| 132Q | Spokane Colleges | 12 | `132Q-spokane-colleges/README.md` |
| 132R | Big Bend Community College | 15 | `132R-big-bend-community-college/README.md` |
| 132S | Columbia Basin College | 15 | `132S-columbia-basin-college/README.md` |
| 132T | Community Colleges-Walla Walla Community College | 13 | `132T-community-colleges-walla-walla-community-college/README.md` |
| 132U | Community Colleges-Whatcom Community College | 14 | `132U-community-colleges-whatcom-community-college/README.md` |
| 132V | Community Colleges-Tacoma Community College | 13 | `132V-community-colleges-tacoma-community-college/README.md` |
| 132W | Wenatchee Valley College | 15 | `132W-wenatchee-valley-college/README.md` |
| 132X | Community Colleges-South Puget Sound Community College | 8 | `132X-community-colleges-south-puget-sound-community-college/README.md` |
| 132Y | Edmonds College | 11 | `132Y-edmonds-college/README.md` |
| 132Z | Cascadia College | 17 | `132Z-cascadia-college/README.md` |
| 495A | Bates Technical College | 14 | `495A-bates-technical-college/README.md` |
| 495B | Bellingham Technical College | 14 | `495B-bellingham-technical-college/README.md` |
| 495C | Clover Park Technical College | 16 | `495C-clover-park-technical-college/README.md` |
| 495D | Lake Washington Institute Of Technology | 23 | `495D-lake-washington-institute-of-technology/README.md` |
| 495E | Renton Technical College | 15 | `495E-renton-technical-college/README.md` |

### Education — Universities & State Colleges

| Title | Agency | Chapters | Read first |
|-------|--------|----------|------------|
| 72 | Blind, Washington State School For The | 9 | `072-blind-washington-state-school-for-the/README.md` |
| 106 | Central Washington University | 15 | `106-central-washington-university/README.md` |
| 108 | Charter School Commission | 6 | `108-charter-school-commission/README.md` |
| 131 | Community And Technical Colleges, Board For | 11 | `131-community-and-technical-colleges-board-for/README.md` |
| 172 | Eastern Washington University | 25 | `172-eastern-washington-university/README.md` |
| 174 | Evergreen State College, The | 16 | `174-evergreen-state-college-the/README.md` |
| 175 | Revenue, Department Of | 0 | `175-revenue-department-of/README.md` |
| 177 | Economic Opportunity, Office Of | 0 | `177-economic-opportunity-office-of/README.md` |
| 178 | Economic Development Finance Authority | 2 | `178-economic-development-finance-authority/README.md` |
| 430 | Washington State School Directors' Association | 1 | `430-washington-state-school-directors-association/README.md` |
| 478 | University Of Washington | 22 | `478-university-of-washington/README.md` |
| 504 | Washington State University | 23 | `504-washington-state-university/README.md` |
| 508 | Ecology, Department Of | 2 | `508-ecology-department-of/README.md` |
| 516 | Western Washington University | 25 | `516-western-washington-university/README.md` |

### Public Safety, Corrections & Emergency Services

| Title | Agency | Chapters | Read first |
|-------|--------|----------|------------|
| 118 | Military Department | 9 | `118-military-department/README.md` |
| 137 | Corrections, Department Of | 31 | `137-corrections-department-of/README.md` |
| 139 | Criminal Justice Training Commission | 18 | `139-criminal-justice-training-commission/README.md` |
| 289 | Corrections Standards Board | 0 | `289-corrections-standards-board/README.md` |
| 297 | Washington Law Enforcement Officers' And Firefighters' Retirement Board | 0 | `297-washington-law-enforcement-officers-and-firefighters-retirement-board/README.md` |
| 299 | Law Enforcement Officers' Training Commission | 0 | `299-law-enforcement-officers-training-commission/README.md` |
| 323 | Military Department | 2 | `323-military-department/README.md` |
| 381 | Indeterminate Sentence Review Board | 10 | `381-indeterminate-sentence-review-board/README.md` |
| 437 | Sentencing Guidelines Commission | 2 | `437-sentencing-guidelines-commission/README.md` |
| 491 | Volunteer Firefighters And Reserve Officers, State Board For | 5 | `491-volunteer-firefighters-and-reserve-officers-state-board-for/README.md` |

### Transportation

| Title | Agency | Chapters | Read first |
|-------|--------|----------|------------|
| 12 | Transportation, Department Of | 0 | `012-transportation-department-of/README.md` |
| 88 | Transportation, Department Of | 1 | `088-transportation-department-of/README.md` |
| 204 | State Patrol | 15 | `204-state-patrol/README.md` |
| 212 | State Patrol | 9 | `212-state-patrol/README.md` |
| 252 | Highway Commission | 0 | `252-highway-commission/README.md` |
| 446 | State Patrol | 17 | `446-state-patrol/README.md` |
| 448 | State Patrol | 3 | `448-state-patrol/README.md` |
| 468 | Transportation, Department Of | 51 | `468-transportation-department-of/README.md` |
| 470 | Transportation Of Dangerous Cargoes, Advisory Committee On | 0 | `470-transportation-of-dangerous-cargoes-advisory-committee-on/README.md` |
| 479 | Transportation Improvement Board | 6 | `479-transportation-improvement-board/README.md` |
| 480 | Utilities And Transportation Commission | 36 | `480-utilities-and-transportation-commission/README.md` |

### Natural Resources, Environment & Agriculture

| Title | Agency | Chapters | Read first |
|-------|--------|----------|------------|
| 16 | Agriculture, Department Of | 143 | `016-agriculture-department-of/README.md` |
| 134 | Conservation, Department Of | 0 | `134-conservation-department-of/README.md` |
| 135 | Conservation Commission | 4 | `135-conservation-commission/README.md` |
| 173 | Ecology, Department Of | 163 | `173-ecology-department-of/README.md` |
| 197 | Ecology, Department Of | 1 | `197-ecology-department-of/README.md` |
| 220 | Fish And Wildlife, Department Of | 56 | `220-fish-and-wildlife-department-of/README.md` |
| 232 | Fish And Wildlife, Department Of | 0 | `232-fish-and-wildlife-department-of/README.md` |
| 237 | Natural Resources, Department On | 1 | `237-natural-resources-department-on/README.md` |
| 260 | Horse Racing Commission | 27 | `260-horse-racing-commission/README.md` |
| 286 | Recreation And Conservation Office | 4 | `286-recreation-and-conservation-office/README.md` |
| 317 | Ecology, Department Of | 3 | `317-ecology-department-of/README.md` |
| 332 | Natural Resources, Board And Department Of | 26 | `332-natural-resources-board-and-department-of/README.md` |
| 344 | Oil And Gas Conservation Committee | 3 | `344-oil-and-gas-conservation-committee/README.md` |
| 352 | Parks And Recreation Commission | 26 | `352-parks-and-recreation-commission/README.md` |
| 372 | Ecology, Department Of | 3 | `372-ecology-department-of/README.md` |
| 400 | Puget Sound Partnership | 2 | `400-puget-sound-partnership/README.md` |
| 420 | Recreation And Conservation Office | 3 | `420-recreation-and-conservation-office/README.md` |

### Culture & Heritage

| Title | Agency | Chapters | Read first |
|-------|--------|----------|------------|
| 25 | Archaeology And Historic Preservation, | 5 | `025-archaeology-and-historic-preservation/README.md` |
| 30 | Arts Commission | 9 | `030-arts-commission/README.md` |
| 241 | State Personnel Board (Historical; No Active Chapters; Only Public Records Remains) | 1 | `241-state-personnel-board-historical/README.md` |
| 254 | Historic Preservation, Advisory Council On | 1 | `254-historic-preservation-advisory-council-on/README.md` |
| 255 | Historical Society, Washington State | 3 | `255-historical-society-washington-state/README.md` |
| 256 | Historical Society, Eastern Washington State | 4 | `256-historical-society-eastern-washington-state/README.md` |
| 304 | Library Commission | 3 | `304-library-commission/README.md` |

### Other / Specialty Agencies

| Title | Agency | Chapters | Read first |
|-------|--------|----------|------------|
| 10 | Administrative Hearings, Office Of | 6 | `010-administrative-hearings-office-of/README.md` |
| 18 | Air Pollution | 0 | `018-air-pollution/README.md` |
| 24 | Apple Commission | 4 | `024-apple-commission/README.md` |
| 51 | Enterprise Services, Department Of | 12 | `051-enterprise-services-department-of/README.md` |
| 60 | Beef Commission | 1 | `060-beef-commission/README.md` |
| 82 | Financial Management, Office Of | 12 | `082-financial-management-office-of/README.md` |
| 90 | Canvassing Board | 0 | `090-canvassing-board/README.md` |
| 100 | 1989 Centennial Commission | 1 | `100-1989-centennial-commission/README.md` |
| 112 | Family And Children'S Ombudsman, Office Of The | 1 | `112-family-and-childrens-ombudsman-office-of-the/README.md` |
| 120 | Community Development, Office Of | 0 | `120-community-development-office-of/README.md` |
| 136 | County Road Administration Board | 31 | `136-county-road-administration-board/README.md` |
| 142 | Dairy Products Commission | 5 | `142-dairy-products-commission/README.md` |
| 143 | Consolidated Technology Services | 2 | `143-consolidated-technology-services/README.md` |
| 154 | Deferred Compensation, Committee For | 0 | `154-deferred-compensation-committee-for/README.md` |
| 158 | Design Standards Committee-Arterial Streets | 0 | `158-design-standards-committee-arterial-streets/README.md` |
| 167 | Drug Abuse Prevention Office | 0 | `167-drug-abuse-prevention-office/README.md` |
| 170 | Early Learning, Department Of | 0 | `170-early-learning-department-of/README.md` |
| 179 | Paraeducator Board | 11 | `179-paraeducator-board/README.md` |
| 183 | Washington Citizens' Commission On Salaries For Elected Officials | 9 | `183-washington-citizens-commission-on-salaries-for-elected-officials/README.md` |
| 187 | Employee Suggestion Awards Board | 0 | `187-employee-suggestion-awards-board/README.md` |
| 198 | Environmental And Land Use Hearings Office | 2 | `198-environmental-and-land-use-hearings-office/README.md` |
| 199 | Environmental Hearings Office | 0 | `199-environmental-hearings-office/README.md` |
| 200 | Enterprise Services, Department Of | 24 | `200-enterprise-services-department-of/README.md` |
| 218 | Forensic Investigations Council | 2 | `218-forensic-investigations-council/README.md` |
| 222 | Forest Practices Board | 15 | `222-forest-practices-board/README.md` |
| 223 | Environmental And Land Use Hearings Office | 1 | `223-environmental-and-land-use-hearings-office/README.md` |
| 224 | Fruit Commission | 1 | `224-fruit-commission/README.md` |
| 236 | Enterprise Services, Department Of | 0 | `236-enterprise-services-department-of/README.md` |
| 242 | Environmental And Land Use Hearings Office | 2 | `242-environmental-and-land-use-hearings-office/README.md` |
| 244 | Hardwoods Commission | 1 | `244-hardwoods-commission/README.md` |
| 257 | Home Care Quality Authority | 4 | `257-home-care-quality-authority/README.md` |
| 259 | Environmental Hearings Office | 0 | `259-environmental-hearings-office/README.md` |
| 294 | Land Use Study Commission | 1 | `294-land-use-study-commission/README.md` |
| 298 | Leased Tidelands Valuation Boards | 1 | `298-leased-tidelands-valuation-boards/README.md` |
| 300 | Librarians, Certification Of | 1 | `300-librarians-certification-of/README.md` |
| 306 | Law Revision Commission | 1 | `306-law-revision-commission/README.md` |
| 316 | Marine Employees' Commission | 0 | `316-marine-employees-commission/README.md` |
| 318 | Maritime Commission | 0 | `318-maritime-commission/README.md` |
| 330 | Municipality Of Metropolitan Seattle | 1 | `330-municipality-of-metropolitan-seattle/README.md` |
| 335 | Nuclear Waste Board | 1 | `335-nuclear-waste-board/README.md` |
| 342 | Oceanographic Commission | 1 | `342-oceanographic-commission/README.md` |
| 363 | Pilotage Commissioners, Board Of | 2 | `363-pilotage-commissioners-board-of/README.md` |
| 371 | Environmental And Land Use Hearings Office | 1 | `371-environmental-and-land-use-hearings-office/README.md` |
| 380 | Printing And Duplicating Committee | 0 | `380-printing-and-duplicating-committee/README.md` |
| 383 | Productivity Board | 2 | `383-productivity-board/README.md` |
| 391 | Public Employment Relations Commission | 9 | `391-public-employment-relations-commission/README.md` |
| 402 | Radiation Control Agency | 0 | `402-radiation-control-agency/README.md` |
| 410 | Reciprocity Commission | 0 | `410-reciprocity-commission/README.md` |
| 414 | Records Committee, Local | 0 | `414-records-committee-local/README.md` |
| 461 | Environmental And Land Use Hearings Office | 1 | `461-environmental-and-land-use-hearings-office/README.md` |
| 465 | Tobacco Settlement Authority | 0 | `465-tobacco-settlement-authority/README.md` |
| 466 | Toll Bridge Authority | 0 | `466-toll-bridge-authority/README.md` |
| 467 | Traffic Safety Commission | 3 | `467-traffic-safety-commission/README.md` |
| 482 | Veterans Rehabilitation Council | 0 | `482-veterans-rehabilitation-council/README.md` |
| 484 | Veterans Affairs, Department Of | 6 | `484-veterans-affairs-department-of/README.md` |

## Glossary — every agency, sorted by Title number

| Title (citation form) | Agency (as in source) | Directory |
|----------------------|----------------------|-----------|
| 1 | CODE REVISER, OFFICE OF THE | `001-code-reviser-office-of-the/` |
| 3 | ACADEMIC ACHIEVEMENT AND ACCOUNTABILITY COMMISSION | `003-academic-achievement-and-accountability-commission/` |
| 4 | ACCOUNTANCY, BOARD OF | `004-accountancy-board-of/` |
| 10 | ADMINISTRATIVE HEARINGS, OFFICE OF | `010-administrative-hearings-office-of/` |
| 12 | TRANSPORTATION, DEPARTMENT OF | `012-transportation-department-of/` |
| 14 | ADVANCED TUITION PAYMENT, COMMITTEE ON | `014-advanced-tuition-payment-committee-on/` |
| 16 | AGRICULTURE, DEPARTMENT OF | `016-agriculture-department-of/` |
| 18 | AIR POLLUTION | `018-air-pollution/` |
| 24 | APPLE COMMISSION | `024-apple-commission/` |
| 25 | ARCHAEOLOGY AND HISTORIC PRESERVATION, | `025-archaeology-and-historic-preservation/` |
| 30 | ARTS COMMISSION | `030-arts-commission/` |
| 34 | ASIAN PACIFIC AMERICAN AFFAIRS, COMMISSION ON | `034-asian-pacific-american-affairs-commission-on/` |
| 36 | LICENSING, DEPARTMENT OF | `036-licensing-department-of/` |
| 44 | ATTORNEY GENERAL'S OFFICE | `044-attorney-generals-office/` |
| 48 | AUDITOR, OFFICE OF STATE | `048-auditor-office-of-state/` |
| 50 | FINANCIAL INSTITUTIONS, | `050-financial-institutions/` |
| 51 | ENTERPRISE SERVICES, DEPARTMENT OF | `051-enterprise-services-department-of/` |
| 55 | BASIC HEALTH PLAN | `055-basic-health-plan/` |
| 60 | BEEF COMMISSION | `060-beef-commission/` |
| 67 | BLIND, DEPARTMENT OF SERVICES FOR THE | `067-blind-department-of-services-for-the/` |
| 72 | BLIND, WASHINGTON STATE SCHOOL FOR THE | `072-blind-washington-state-school-for-the/` |
| 82 | FINANCIAL MANAGEMENT, OFFICE OF | `082-financial-management-office-of/` |
| 88 | TRANSPORTATION, DEPARTMENT OF | `088-transportation-department-of/` |
| 90 | CANVASSING BOARD | `090-canvassing-board/` |
| 98 | LICENSING, DEPARTMENT OF | `098-licensing-department-of/` |
| 100 | 1989 CENTENNIAL COMMISSION | `100-1989-centennial-commission/` |
| 106 | CENTRAL WASHINGTON UNIVERSITY | `106-central-washington-university/` |
| 108 | CHARTER SCHOOL COMMISSION | `108-charter-school-commission/` |
| 110 | CHILDREN, YOUTH, AND FAMILIES, DEPARTMENT OF | `110-children-youth-and-families-department-of/` |
| 112 | FAMILY AND CHILDREN'S OMBUDSMAN, OFFICE OF THE | `112-family-and-childrens-ombudsman-office-of-the/` |
| 113 | CHIROPRACTIC DISCIPLINARY BOARD | `113-chiropractic-disciplinary-board/` |
| 114 | CHIROPRACTIC EXAMINERS, BOARD OF | `114-chiropractic-examiners-board-of/` |
| 118 | MILITARY DEPARTMENT | `118-military-department/` |
| 120 | COMMUNITY DEVELOPMENT, OFFICE OF | `120-community-development-office-of/` |
| 130 | COMMERCE, DEPARTMENT OF | `130-commerce-department-of/` |
| 131 | COMMUNITY AND TECHNICAL COLLEGES, BOARD FOR | `131-community-and-technical-colleges-board-for/` |
| 132A | COMMUNITY COLLEGES-PENINSULA COLLEGE | `132A-community-colleges-peninsula-college/` |
| 132B | COMMUNITY COLLEGES-GRAYS HARBOR COLLEGE | `132B-community-colleges-grays-harbor-college/` |
| 132C | OLYMPIC COLLEGE | `132C-olympic-college/` |
| 132D | SKAGIT VALLEY COLLEGE | `132D-skagit-valley-college/` |
| 132E | EVERETT COMMUNITY COLLEGE | `132E-everett-community-college/` |
| 132F | SEATTLE COLLEGES | `132F-seattle-colleges/` |
| 132G | SHORELINE COMMUNITY COLLEGE | `132G-shoreline-community-college/` |
| 132H | BELLEVUE COLLEGE | `132H-bellevue-college/` |
| 132I | HIGHLINE COLLEGE | `132I-highline-college/` |
| 132J | COMMUNITY COLLEGES-GREEN RIVER COLLEGE | `132J-community-colleges-green-river-college/` |
| 132K | PIERCE COLLEGE | `132K-pierce-college/` |
| 132L | CENTRALIA COLLEGE | `132L-centralia-college/` |
| 132M | LOWER COLUMBIA COLLEGE | `132M-lower-columbia-college/` |
| 132N | CLARK COLLEGE | `132N-clark-college/` |
| 132P | COMMUNITY COLLEGES-YAKIMA VALLEY COMMUNITY COLLEGE | `132P-community-colleges-yakima-valley-community-college/` |
| 132Q | SPOKANE COLLEGES | `132Q-spokane-colleges/` |
| 132R | BIG BEND COMMUNITY COLLEGE | `132R-big-bend-community-college/` |
| 132S | COLUMBIA BASIN COLLEGE | `132S-columbia-basin-college/` |
| 132T | COMMUNITY COLLEGES-WALLA WALLA COMMUNITY COLLEGE | `132T-community-colleges-walla-walla-community-college/` |
| 132U | COMMUNITY COLLEGES-WHATCOM COMMUNITY COLLEGE | `132U-community-colleges-whatcom-community-college/` |
| 132V | COMMUNITY COLLEGES-TACOMA COMMUNITY COLLEGE | `132V-community-colleges-tacoma-community-college/` |
| 132W | WENATCHEE VALLEY COLLEGE | `132W-wenatchee-valley-college/` |
| 132X | COMMUNITY COLLEGES-SOUTH PUGET SOUND COMMUNITY COLLEGE | `132X-community-colleges-south-puget-sound-community-college/` |
| 132Y | EDMONDS COLLEGE | `132Y-edmonds-college/` |
| 132Z | CASCADIA COLLEGE | `132Z-cascadia-college/` |
| 133 | COMMERCE, DEPARTMENT OF | `133-commerce-department-of/` |
| 134 | CONSERVATION, DEPARTMENT OF | `134-conservation-department-of/` |
| 135 | CONSERVATION COMMISSION | `135-conservation-commission/` |
| 136 | COUNTY ROAD ADMINISTRATION BOARD | `136-county-road-administration-board/` |
| 137 | CORRECTIONS, DEPARTMENT OF | `137-corrections-department-of/` |
| 139 | CRIMINAL JUSTICE TRAINING COMMISSION | `139-criminal-justice-training-commission/` |
| 140 | CONVENTION AND TRADE CENTER | `140-convention-and-trade-center/` |
| 142 | DAIRY PRODUCTS COMMISSION | `142-dairy-products-commission/` |
| 143 | CONSOLIDATED TECHNOLOGY SERVICES | `143-consolidated-technology-services/` |
| 148 | DEAF AND HARD OF HEARING YOUTH, CENTER FOR | `148-deaf-and-hard-of-hearing-youth-center-for/` |
| 154 | DEFERRED COMPENSATION, COMMITTEE FOR | `154-deferred-compensation-committee-for/` |
| 158 | DESIGN STANDARDS COMMITTEE-ARTERIAL STREETS | `158-design-standards-committee-arterial-streets/` |
| 162 | HUMAN RIGHTS COMMISSION | `162-human-rights-commission/` |
| 167 | DRUG ABUSE PREVENTION OFFICE | `167-drug-abuse-prevention-office/` |
| 170 | EARLY LEARNING, DEPARTMENT OF | `170-early-learning-department-of/` |
| 172 | EASTERN WASHINGTON UNIVERSITY | `172-eastern-washington-university/` |
| 173 | ECOLOGY, DEPARTMENT OF | `173-ecology-department-of/` |
| 174 | EVERGREEN STATE COLLEGE, THE | `174-evergreen-state-college-the/` |
| 175 | REVENUE, DEPARTMENT OF | `175-revenue-department-of/` |
| 177 | ECONOMIC OPPORTUNITY, OFFICE OF | `177-economic-opportunity-office-of/` |
| 178 | ECONOMIC DEVELOPMENT FINANCE AUTHORITY | `178-economic-development-finance-authority/` |
| 179 | PARAEDUCATOR BOARD | `179-paraeducator-board/` |
| 180 | EDUCATION, STATE BOARD OF | `180-education-state-board-of/` |
| 181 | PROFESSIONAL EDUCATOR STANDARDS BOARD | `181-professional-educator-standards-board/` |
| 182 | HEALTH CARE AUTHORITY | `182-health-care-authority/` |
| 183 | WASHINGTON CITIZENS' COMMISSION ON SALARIES FOR ELECTED OFFICIALS | `183-washington-citizens-commission-on-salaries-for-elected-officials/` |
| 184 | EMPLOYEES' RETIREMENT SYSTEM, PUBLIC | `184-employees-retirement-system-public/` |
| 186 | EMPLOYEES' RETIREMENT, STATEWIDE CITIES | `186-employees-retirement-statewide-cities/` |
| 187 | EMPLOYEE SUGGESTION AWARDS BOARD | `187-employee-suggestion-awards-board/` |
| 192 | EMPLOYMENT SECURITY DEPARTMENT | `192-employment-security-department/` |
| 194 | COMMERCE, DEPARTMENT OF | `194-commerce-department-of/` |
| 196 | ENGINEERS AND LAND SURVEYORS, BOARD OF REGISTRATION FOR PROFESSIONAL | `196-engineers-and-land-surveyors-board-of-registration-for-professional/` |
| 197 | ECOLOGY, DEPARTMENT OF | `197-ecology-department-of/` |
| 198 | ENVIRONMENTAL AND LAND USE HEARINGS OFFICE | `198-environmental-and-land-use-hearings-office/` |
| 199 | ENVIRONMENTAL HEARINGS OFFICE | `199-environmental-hearings-office/` |
| 200 | ENTERPRISE SERVICES, DEPARTMENT OF | `200-enterprise-services-department-of/` |
| 204 | STATE PATROL | `204-state-patrol/` |
| 208 | FINANCIAL INSTITUTIONS, DEPARTMENT OF | `208-financial-institutions-department-of/` |
| 210 | STATE TREASURER'S OFFICE | `210-state-treasurers-office/` |
| 212 | STATE PATROL | `212-state-patrol/` |
| 218 | FORENSIC INVESTIGATIONS COUNCIL | `218-forensic-investigations-council/` |
| 220 | FISH AND WILDLIFE, DEPARTMENT OF | `220-fish-and-wildlife-department-of/` |
| 222 | FOREST PRACTICES BOARD | `222-forest-practices-board/` |
| 223 | ENVIRONMENTAL AND LAND USE HEARINGS OFFICE | `223-environmental-and-land-use-hearings-office/` |
| 224 | FRUIT COMMISSION | `224-fruit-commission/` |
| 226 | FREIGHT MOBILITY STRATEGIC INVESTMENT BOARD | `226-freight-mobility-strategic-investment-board/` |
| 230 | GAMBLING COMMISSION | `230-gambling-commission/` |
| 232 | FISH AND WILDLIFE, DEPARTMENT OF | `232-fish-and-wildlife-department-of/` |
| 236 | ENTERPRISE SERVICES, DEPARTMENT OF | `236-enterprise-services-department-of/` |
| 237 | NATURAL RESOURCES, DEPARTMENT ON | `237-natural-resources-department-on/` |
| 240 | GOVERNOR, OFFICE OF THE | `240-governor-office-of-the/` |
| 241 | STATE PERSONNEL BOARD (historical; no active chapters; only Public Records remains) | `241-state-personnel-board-historical/` |
| 242 | ENVIRONMENTAL AND LAND USE HEARINGS OFFICE | `242-environmental-and-land-use-hearings-office/` |
| 243 | HEALTH CARE POLICY BOARD | `243-health-care-policy-board/` |
| 244 | HARDWOODS COMMISSION | `244-hardwoods-commission/` |
| 245 | HEALTH SERVICES COMMISSION | `245-health-services-commission/` |
| 246 | HEALTH, DEPARTMENT OF | `246-health-department-of/` |
| 247 | HEALTH CARE FACILITIES AUTHORITY | `247-health-care-facilities-authority/` |
| 248 | HEALTH, BOARD AND DIVISION OF | `248-health-board-and-division-of/` |
| 249 | HIGHER EDUCATION ASSISTANCE AUTHORITY | `249-higher-education-assistance-authority/` |
| 249A | HIGHER EDUCATION, JOINT CENTER FOR | `249A-higher-education-joint-center-for/` |
| 250 | STUDENT ACHIEVEMENT COUNCIL | `250-student-achievement-council/` |
| 251 | PERSONNEL, DEPARTMENT OF | `251-personnel-department-of/` |
| 252 | HIGHWAY COMMISSION | `252-highway-commission/` |
| 253 | HIGHER EDUCATION FACILITIES AUTHORITY | `253-higher-education-facilities-authority/` |
| 254 | HISTORIC PRESERVATION, ADVISORY COUNCIL ON | `254-historic-preservation-advisory-council-on/` |
| 255 | HISTORICAL SOCIETY, WASHINGTON STATE | `255-historical-society-washington-state/` |
| 256 | HISTORICAL SOCIETY, EASTERN WASHINGTON STATE | `256-historical-society-eastern-washington-state/` |
| 257 | HOME CARE QUALITY AUTHORITY | `257-home-care-quality-authority/` |
| 259 | ENVIRONMENTAL HEARINGS OFFICE | `259-environmental-hearings-office/` |
| 260 | HORSE RACING COMMISSION | `260-horse-racing-commission/` |
| 261 | HOSPITAL COMMISSION | `261-hospital-commission/` |
| 262 | HOUSING FINANCE COMMISSION | `262-housing-finance-commission/` |
| 263 | INDUSTRIAL INSURANCE APPEALS, BOARD OF | `263-industrial-insurance-appeals-board-of/` |
| 275 | SOCIAL AND HEALTH SERVICES, DEPARTMENT OF (INSTITUTIONS) | `275-social-and-health-services-department-of-institutions/` |
| 284 | INSURANCE COMMISSIONER | `284-insurance-commissioner/` |
| 286 | RECREATION AND CONSERVATION OFFICE | `286-recreation-and-conservation-office/` |
| 287 | INVESTMENT BOARD, STATE | `287-investment-board-state/` |
| 288 | JAIL INDUSTRIES BOARD | `288-jail-industries-board/` |
| 289 | CORRECTIONS STANDARDS BOARD | `289-corrections-standards-board/` |
| 290 | JUDICIAL RETIREMENT BOARD | `290-judicial-retirement-board/` |
| 292 | ETHICS IN PUBLIC SERVICE | `292-ethics-in-public-service/` |
| 294 | LAND USE STUDY COMMISSION | `294-land-use-study-commission/` |
| 296 | LABOR AND INDUSTRIES, DEPARTMENT OF | `296-labor-and-industries-department-of/` |
| 297 | WASHINGTON LAW ENFORCEMENT OFFICERS' AND FIREFIGHTERS' RETIREMENT BOARD | `297-washington-law-enforcement-officers-and-firefighters-retirement-board/` |
| 298 | LEASED TIDELANDS VALUATION BOARDS | `298-leased-tidelands-valuation-boards/` |
| 299 | LAW ENFORCEMENT OFFICERS' TRAINING COMMISSION | `299-law-enforcement-officers-training-commission/` |
| 300 | LIBRARIANS, CERTIFICATION OF | `300-librarians-certification-of/` |
| 304 | LIBRARY COMMISSION | `304-library-commission/` |
| 306 | LAW REVISION COMMISSION | `306-law-revision-commission/` |
| 308 | LICENSING, DEPARTMENT OF | `308-licensing-department-of/` |
| 314 | LIQUOR AND CANNABIS BOARD | `314-liquor-and-cannabis-board/` |
| 315 | LOTTERY COMMISSION | `315-lottery-commission/` |
| 316 | MARINE EMPLOYEES' COMMISSION | `316-marine-employees-commission/` |
| 317 | ECOLOGY, DEPARTMENT OF | `317-ecology-department-of/` |
| 318 | MARITIME COMMISSION | `318-maritime-commission/` |
| 320 | MEDICAL DISCIPLINARY BOARD | `320-medical-disciplinary-board/` |
| 322 | HISPANIC AFFAIRS, COMMISSION ON | `322-hispanic-affairs-commission-on/` |
| 323 | MILITARY DEPARTMENT | `323-military-department/` |
| 326 | MINORITY AND WOMEN'S BUSINESS ENTERPRISES, OFFICE OF | `326-minority-and-womens-business-enterprises-office-of/` |
| 330 | MUNICIPALITY OF METROPOLITAN SEATTLE | `330-municipality-of-metropolitan-seattle/` |
| 332 | NATURAL RESOURCES, BOARD AND DEPARTMENT OF | `332-natural-resources-board-and-department-of/` |
| 335 | NUCLEAR WASTE BOARD | `335-nuclear-waste-board/` |
| 342 | OCEANOGRAPHIC COMMISSION | `342-oceanographic-commission/` |
| 344 | OIL AND GAS CONSERVATION COMMITTEE | `344-oil-and-gas-conservation-committee/` |
| 352 | PARKS AND RECREATION COMMISSION | `352-parks-and-recreation-commission/` |
| 356 | PERSONNEL, DEPARTMENT OF (GENERAL GOVERNMENT) | `356-personnel-department-of-general-government/` |
| 357 | FINANCIAL MANAGEMENT, OFFICE OF-STATE HUMAN RESOURCES DIRECTOR | `357-financial-management-office-of-state-human-resources-director/` |
| 358 | PERSONNEL APPEALS BOARD | `358-personnel-appeals-board/` |
| 359 | PERSONNEL, DEPARTMENT OF | `359-personnel-department-of/` |
| 360 | PHARMACY, BOARD OF | `360-pharmacy-board-of/` |
| 363 | PILOTAGE COMMISSIONERS, BOARD OF | `363-pilotage-commissioners-board-of/` |
| 365 | COMMERCE, DEPARTMENT OF | `365-commerce-department-of/` |
| 371 | ENVIRONMENTAL AND LAND USE HEARINGS OFFICE | `371-environmental-and-land-use-hearings-office/` |
| 372 | ECOLOGY, DEPARTMENT OF | `372-ecology-department-of/` |
| 374 | POLLUTION LIABILITY INSURANCE AGENCY | `374-pollution-liability-insurance-agency/` |
| 380 | PRINTING AND DUPLICATING COMMITTEE | `380-printing-and-duplicating-committee/` |
| 381 | INDETERMINATE SENTENCE REVIEW BOARD | `381-indeterminate-sentence-review-board/` |
| 383 | PRODUCTIVITY BOARD | `383-productivity-board/` |
| 388 | SOCIAL AND HEALTH SERVICES, | `388-social-and-health-services/` |
| 389 | STATE TREASURER'S OFFICE | `389-state-treasurers-office/` |
| 390 | PUBLIC DISCLOSURE COMMISSION | `390-public-disclosure-commission/` |
| 391 | PUBLIC EMPLOYMENT RELATIONS COMMISSION | `391-public-employment-relations-commission/` |
| 392 | PUBLIC INSTRUCTION, SUPERINTENDENT OF | `392-public-instruction-superintendent-of/` |
| 399 | COMMERCE, DEPARTMENT OF | `399-commerce-department-of/` |
| 400 | PUGET SOUND PARTNERSHIP | `400-puget-sound-partnership/` |
| 402 | RADIATION CONTROL AGENCY | `402-radiation-control-agency/` |
| 410 | RECIPROCITY COMMISSION | `410-reciprocity-commission/` |
| 414 | RECORDS COMMITTEE, LOCAL | `414-records-committee-local/` |
| 415 | RETIREMENT SYSTEMS, DEPARTMENT OF | `415-retirement-systems-department-of/` |
| 417 | REDISTRICTING COMMISSION | `417-redistricting-commission/` |
| 419 | FINANCIAL INSTITUTIONS, DEPARTMENT OF | `419-financial-institutions-department-of/` |
| 420 | RECREATION AND CONSERVATION OFFICE | `420-recreation-and-conservation-office/` |
| 430 | WASHINGTON STATE SCHOOL DIRECTORS' ASSOCIATION | `430-washington-state-school-directors-association/` |
| 434 | SECRETARY OF STATE | `434-secretary-of-state/` |
| 437 | SENTENCING GUIDELINES COMMISSION | `437-sentencing-guidelines-commission/` |
| 440 | SOCIAL AND HEALTH SERVICES, DEPARTMENT OF | `440-social-and-health-services-department-of/` |
| 446 | STATE PATROL | `446-state-patrol/` |
| 448 | STATE PATROL | `448-state-patrol/` |
| 456 | TAX APPEALS, BOARD OF | `456-tax-appeals-board-of/` |
| 458 | REVENUE, DEPARTMENT OF | `458-revenue-department-of/` |
| 460 | FINANCIAL INSTITUTIONS, DEPARTMENT OF | `460-financial-institutions-department-of/` |
| 461 | ENVIRONMENTAL AND LAND USE HEARINGS OFFICE | `461-environmental-and-land-use-hearings-office/` |
| 462 | TEACHERS' RETIREMENT | `462-teachers-retirement/` |
| 463 | ENERGY FACILITY SITE EVALUATION COUNCIL | `463-energy-facility-site-evaluation-council/` |
| 465 | TOBACCO SETTLEMENT AUTHORITY | `465-tobacco-settlement-authority/` |
| 466 | TOLL BRIDGE AUTHORITY | `466-toll-bridge-authority/` |
| 467 | TRAFFIC SAFETY COMMISSION | `467-traffic-safety-commission/` |
| 468 | TRANSPORTATION, DEPARTMENT OF | `468-transportation-department-of/` |
| 470 | TRANSPORTATION OF DANGEROUS CARGOES, ADVISORY COMMITTEE ON | `470-transportation-of-dangerous-cargoes-advisory-committee-on/` |
| 474 | STATE TREASURER'S OFFICE | `474-state-treasurers-office/` |
| 478 | UNIVERSITY OF WASHINGTON | `478-university-of-washington/` |
| 479 | TRANSPORTATION IMPROVEMENT BOARD | `479-transportation-improvement-board/` |
| 480 | UTILITIES AND TRANSPORTATION COMMISSION | `480-utilities-and-transportation-commission/` |
| 482 | VETERANS REHABILITATION COUNCIL | `482-veterans-rehabilitation-council/` |
| 484 | VETERANS AFFAIRS, DEPARTMENT OF | `484-veterans-affairs-department-of/` |
| 490 | WORKFORCE TRAINING AND EDUCATION COORDINATING BOARD, ALSO VOCATIONAL REHABILITATION | `490-workforce-training-and-education-coordinating-board-also-vocational-rehabilitation/` |
| 491 | VOLUNTEER FIREFIGHTERS AND RESERVE OFFICERS, STATE BOARD FOR | `491-volunteer-firefighters-and-reserve-officers-state-board-for/` |
| 495A | BATES TECHNICAL COLLEGE | `495A-bates-technical-college/` |
| 495B | BELLINGHAM TECHNICAL COLLEGE | `495B-bellingham-technical-college/` |
| 495C | CLOVER PARK TECHNICAL COLLEGE | `495C-clover-park-technical-college/` |
| 495D | LAKE WASHINGTON INSTITUTE OF TECHNOLOGY | `495D-lake-washington-institute-of-technology/` |
| 495E | RENTON TECHNICAL COLLEGE | `495E-renton-technical-college/` |
| 504 | WASHINGTON STATE UNIVERSITY | `504-washington-state-university/` |
| 508 | ECOLOGY, DEPARTMENT OF | `508-ecology-department-of/` |
| 516 | WESTERN WASHINGTON UNIVERSITY | `516-western-washington-university/` |

## Directory layout

```
wac-skill/
├── SKILL.md                                            <- this file (the only SKILL.md)
├── 001-code-reviser-office-of-the/
│   ├── README.md
│   └── rules.md
├── 003-academic-achievement-and-accountability-commission/
│   ├── README.md
│   └── rules.md
├── 004-accountancy-board-of/
│   ├── README.md
│   └── rules.md
├── 010-administrative-hearings-office-of/
│   ├── README.md
│   └── rules.md
├── 012-transportation-department-of/
│   ├── README.md
│   └── rules.md
├── ...  (220 more title directories)
├── 508-ecology-department-of/
│   ├── README.md
│   └── rules.md
├── 516-western-washington-university/
│   ├── README.md
│   └── rules.md
└── _build/                                              <- build manifest (not part of the skill)
```

All paths in this skill are **relative** to this directory.

## Cross-title search

```bash
# Pull the full body of a specific section by citation
grep -rn -A 80 'WAC 173-201A-200' --include='rules.md' .

# Any chapter title containing a keyword
grep -rn -E '^## WAC [^—]* —.*licens' --include='rules.md' .

# Find which title a topic lives in (case-insensitive, body text searched too)
grep -rni 'cannabis' --include='rules.md' . | head

# List every chapter heading across the corpus
grep -rh '^## WAC ' --include='rules.md' . | sort

# Search the prior TOC-only backups instead of full bodies (e.g. to verify
# that every TOC-listed section has body text in the new rules.md)
grep -rn 'WAC 4-30-100' --include='rules.md.toc.bak' .
```

## Citation format

- Section: `WAC 173-201A-200` (Title-Chapter-Section)
- Chapter: `chapter 173-201A WAC` or just `WAC 173-201A`
- Title: `Title 173 WAC`
- Always include `WAC` so the citation isn't confused with an RCW statute.

## Fidelity status

- **174 titles: FAITHFUL.** `rules.md` contains the full body text of every chapter, sourced from the 2025 archive's per-chapter `COMBINEDCHAPTER.pdf` files. Section subheadings, subsection numbering, and statutory-authority history brackets are preserved. Fee tables and other column-aligned tables are kept as whitespace-aligned text (grep-able and quotable, but not GFM tables). Each patched topic keeps the prior section-index-only `rules.md` as `rules.md.toc.bak` for cross-checking.
- **1 title: DEGRADED — SOURCE UNAVAILABLE.** Title 237 (Natural Resources, Department On) has a single non-standard appendix chapter (`WAC 237-990`) whose `COMBINEDCHAPTER.pdf` returned a 404 from the legislature's 2025 archive at snapshot time. The `rules.md` carries a placeholder section marking the permanent gap; `rules.md.toc.bak` retains the chapter's original index entry.
- **52 titles: N/A — NO ACTIVE CHAPTERS.** Empty chapter list in the 2025 archive, confirmed by both the absence of chapters in the chapter HTML index and the absence of any combined-chapter PDFs for the title. These titles retain a stub `rules.md` (no `rules.md.toc.bak` is written when there is nothing to back up).

## Universal notes

- **Effective date:** This snapshot is dated 2026-05-20. The WAC is amended continuously; for currency-sensitive use, the user should re-verify against the official source.
- **Out of scope:**
  - **RCW (Revised Code of Washington) statutes** are not in this corpus. The WAC implements RCW; the two are separate bodies. If the user actually wants statute text (e.g. "RCW 9A.04.110"), route to the sibling `wa-rcw/` skill, not this one.
  - **Federal Code of Federal Regulations (CFR)** is not in this corpus.
  - **City and county codes/ordinances** are not in this corpus.
  - **Court rules** (CR, RPC, GR, RAP, etc.) are not in this corpus — see the sibling skills `wa-state-court-rules/` (statewide rules), `wa-county-superior-court-rules/` (county Superior Court local rules), `wa-district-court-rules/`, and `wa-municipal-court-rules/`.
  - For chapters whose combined PDF was not fetchable (Title 237's `237-990` appendix), see the official Washington State Legislature website.
- **Body text source / provenance:** Full section text in this snapshot was sourced from the Washington State Legislature's per-chapter `COMBINEDCHAPTER.pdf` files in the 2025 WAC archive (publisher path: `Lawfilesext.leg.wa.gov/law/WACArchive/2025/...`), converted with `pdftotext -layout` and cleaned. The raw PDFs and intermediate `.txt` files are not redistributed with this skill; anyone who needs to re-derive or audit the corpus can pull them directly from the legislature.
- This corpus is offline-only. Never fetch or refetch from the web at runtime — the on-disk markdown is authoritative for this skill.

