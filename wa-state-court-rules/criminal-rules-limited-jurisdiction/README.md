---
name: wa-crrlj-criminal-rules-limited-jurisdiction
description: Use when the user asks about, cites, quotes, or compares Washington's Criminal Rules for Courts of Limited Jurisdiction (CrRLJ) — the rules governing criminal procedure in Washington district and municipal courts. Triggers on citations like "CrRLJ 3.1", "CrRLJ 4.2", "CrRLJ 3.3", references to courts of limited jurisdiction criminal practice (arraignment, pleas, speedy-trial in district/municipal court, misdemeanor procedure), or the abbreviation "CrRLJ" generally. Do NOT use for Superior Court criminal procedure (that is CrR), civil rules for courts of limited jurisdiction (CRLJ), juvenile court (JuCR), or the Rules of Appellate Procedure (RAP).
---

# CrRLJ — Criminal Rules for Courts of Limited Jurisdiction (Washington State)

**Effective date of this snapshot:** 2026-05-20.

**Scope:** These rules govern criminal proceedings in Washington's **courts of limited jurisdiction** — i.e. district courts and municipal courts. They do **not** apply to Superior Court criminal cases (those are governed by the separate CrR rules) and they do **not** cover civil matters in courts of limited jurisdiction (those are CRLJ).

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Body text, subsection lettering ((a), (b), (1), (2)), citation references, and adoption/amendment notes are preserved cleanly. Caveats below cover the few layout artifacts.

## Files

```
criminal-rules-limited-jurisdiction/
├── README.md   ← you are here
└── rules.md    ← all 76 CrRLJ rules, concatenated
```

## Looking up a rule

```bash
# Single rule (e.g., right to counsel)
grep -n -A 80 '^## CrRLJ 3\.1$' rules.md

# Rule plus its standards/subparts (e.g., 3.1 and 3.1 Standards)
grep -n -A 80 '^## CrRLJ 3\.1' rules.md

# A specific subsection (e.g., CrRLJ 4.2(g))
grep -n -B 1 -A 8 '(g) Written Statement' rules.md

# All rule headings
grep -n '^## CrRLJ' rules.md

# Anything mentioning "speedy trial"
grep -ni 'speedy trial' rules.md
```

## Citation format

- `CrRLJ 3.1` — Right to and Assignment of Lawyer.
- `CrRLJ 3.1 Standards` — Standards for Indigent Defense (adopted under CrRLJ 3.1).
- `CrRLJ 4.2(g)` — subsection citation; preserve the parenthetical letter/number as it appears in the source.
- `CrRLJ 3.2.1` — for rules with a third-level dotted number (e.g., 3.2.1, 4.3.1).

Always quote the precise subsection lettering from `rules.md`. The parenthetical structure ((a), (b)(1), (b)(2)(i), etc.) is preserved.

## Caveats

- **Multi-column tables in CrRLJ 4.2 (DUI sentencing grid).** The DUI mandatory-minimum sentencing tables in the plea-statement form (CrRLJ 4.2) render as space-aligned columns that wrap awkwardly. The text content is present and citable, but column alignment is unreliable — treat numbers in the sentencing tables as approximate text positions, not as authoritative tabular data.
- **CrRLJ 3.1 Standards is a separate document.** The "Standards for Indigent Defense" adopted under CrRLJ 3.1 appears in `rules.md` immediately after CrRLJ 3.1 under the heading `## CrRLJ 3.1 Standards`. It is structurally part of the rule but is numbered as "Standard 1", "Standard 2", etc., not as CrRLJ subsections.
- **Some rules are `[RESERVED]`.** Several headings (e.g., CrRLJ 7.1, 7.7, 8.5, 8.7, 8.11) consist only of the rule number and `[RESERVED]`. That is faithful to the source — the Washington Supreme Court has reserved those numbers without adopting text.
- **Rule 6.13 covers a sensitive scope.** CrRLJ 6.13 is the rule on procedures for child witnesses; it is long and uses a particular subsection structure. Re-check the exact lettering in `rules.md` before quoting.
- **Adoption / amendment history** at the bottom of each rule (the bracketed `[Adopted effective ...; Amended effective ...]` line) is preserved and is the authoritative dating for that rule's text in this snapshot.
- **Heading numbering.** The headings in `rules.md` (`CrRLJ 3.1`, `CrRLJ 3.2.1`, `CrRLJ 6.1.1`) match the Washington Supreme Court's canonical numbering for this rule set.

## What is not in this corpus

- **CrR** (Superior Court Criminal Rules) — separate topic.
- **CRLJ** (Civil Rules for Courts of Limited Jurisdiction) — separate topic.
- **JuCR** (Juvenile Court Rules) — separate topic.
- **RCW** (Revised Code of Washington statutes) — not here; CrRLJ frequently cites RCW chapters (esp. RCW 10.77, RCW 46.61) but the statutory text is external.
- **Local rules** of individual district/municipal courts that supplement CrRLJ — see the sibling corpora `wa-district-court-rules/` and `wa-municipal-court-rules/`.
