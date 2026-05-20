---
name: wa-crr-superior-court-criminal-rules
description: Use when the user asks about, cites, quotes, or compares Washington State Superior Court Criminal Rules (CrR) — felony procedure in superior court, including arraignment, pleas, speedy trial, discovery, suppression, post-conviction relief, and indigent defense standards. Triggers on citation forms like "CrR 3.1", "CrR 4.7", "CrR 7.8", "Criminal Rule 3.3", "Washington CrR", or any request about superior-court criminal procedure (felonies). Do NOT use for misdemeanor procedure in courts of limited jurisdiction (use CrRLJ), juvenile offender procedure (use JuCR), civil rules (CR), appellate rules (RAP), or evidence rules (ER).
---

# Washington Superior Court Criminal Rules (CrR)

**Effective date of this snapshot:** 2026-05-20.

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Body text, subsection lettering ((a), (b), (1), (2), (i), (ii)), citation references, and adoption/amendment history are all preserved. The long plea-of-guilty statement forms inside CrR 4.2 retain space-aligned table headers (offender score / standard range / enhancements) that wrap awkwardly when grepped but are readable; same for the warrant-of-arrest and sex-offender registration forms. Suitable for direct citation of rule text; column alignment in those tables is unreliable — treat as text, not tabular data.

## Files

```
superior-court-criminal-rules/
├── README.md   ← you are here
└── rules.md    ← all 65 CrR rules, concatenated in rule-number order
```

## Looking up a rule

```bash
# Pull a specific rule (e.g. CrR 3.1, Right to and Assignment of Lawyer)
grep -n -A 200 '^## CrR 3\.1$' rules.md

# Right to counsel + indigent defense caseload standards (separate file in source)
grep -n -A 400 '^## CrR 3\.1 Standards$' rules.md

# Speedy trial
grep -n -A 200 '^## CrR 3\.3$' rules.md

# Pleas (long; contains the statutory plea statement form)
grep -n -A 1200 '^## CrR 4\.2$' rules.md

# Discovery
grep -n -A 250 '^## CrR 4\.7$' rules.md

# Post-conviction relief from judgment
grep -n -A 200 '^## CrR 7\.8$' rules.md

# List every rule heading
grep -n '^## CrR ' rules.md
```

## Citation format

- `CrR 3.1` — Right to and Assignment of Lawyer
- `CrR 3.1 Standards` — Standards for Indigent Defense (companion document to CrR 3.1)
- `CrR 3.2`, `CrR 3.2A`, `CrR 3.2B`, `CrR 3.2.1` — Release of Accused / Bail / Procedure Following Warrantless Arrest (note: these are four distinct rules, not subsections)
- `CrR 4.7` — Discovery
- `CrR 7.8` — Relief from Judgment or Order

Always cite the rule number exactly as it appears in the source (e.g., `CrR 4.3.1`, not `CrR 4.31`). When quoting from the long form in CrR 4.2(g) (Statement of Defendant on Plea of Guilty), cite as `CrR 4.2(g)` and reference the form by paragraph number.

## Caveats

- The corpus contains **65 rule files** including standalone variants (`CrR 3.2A` Release of Accused, `CrR 3.2B` Procedure Following Warrantless Arrest) and a separate `CrR 3.1 Standards` document for indigent defense caseload limits. These are not subsections of the rules they sit near; treat each as its own citable rule.
- `CrR 1.5` (Style and Form) is `[Reserved. See GR 14.]` — content lives in the General Rules, not here.
- `CrR 4.2(g)` includes the full text of the **Statement of Defendant on Plea of Guilty** (Non-Sex Offense Felony) form, plus an alternate sex-offense version. These are statutory forms with fill-in blanks; spacing in the form blocks is preserved — do not assume markdown semantics.
- The indigent-defense caseload standard at `CrR 3.1 Standards`, Standard 3.4 was amended effective January 1, 2026 — felony attorneys are capped at 47 felony case credits/year, misdemeanor at 120/year, civil commitment at 250/year, with a 10-year phased implementation. Verify the snapshot date against any post-2026-05-20 amendments before relying on caseload numbers.
- Adoption/amendment history brackets at the foot of each rule are preserved verbatim — useful for dating the version a court applied.
- Hyphenated line-break artifacts (`docu-\nment`) were removed during consolidation. If a hyphen appears mid-word in the markdown, it is intentional in the source.
