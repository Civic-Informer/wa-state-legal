---
name: wa-ralj-appeals-from-limited-jurisdiction
description: Use when the user asks about, cites, quotes, or compares the Washington Rules for Appeal of Decisions of Courts of Limited Jurisdiction — the superior-court appeal procedure from district/municipal/CLJ rulings (notice of appeal, bonds, stays, the record, transcripts of electronic record, briefs, oral argument, decision, costs, and attorney fees on appeal). Triggers on citations like "RALJ 2.4", "RALJ 6.3.1", "RALJ 9.3", or phrases like "appeal from district court", "appeal to superior court from court of limited jurisdiction", "RALJ notice of appeal", "RALJ stay". Do NOT use for appeals to the Court of Appeals or Supreme Court (those are governed by RAP), for de novo review of small claims (CRLJ 73/75), or for the underlying district/municipal court procedure (CRLJ / CrRLJ / IRLJ).
---

# Washington Rules for Appeal of Decisions of Courts of Limited Jurisdiction (RALJ)

**Effective date of this snapshot:** 2026-05-20.

**Fidelity verdict:** FAITHFUL. Body text, subsection lettering ((a), (b)(1), etc.), cross-references (e.g. 'rule 6.3', 'RCW 10.101.010(3)(a)-(c)'), and adoption/amendment history are clean. Headings use canonical RALJ numbering (e.g. `## RALJ 6.3.1`).

## Files

```
appeals-from-limited-jurisdiction/
├── README.md   ← you are here
└── rules.md    ← all 45 RALJ rules, concatenated
```

## Looking up a rule

```bash
# Whole rule by citation (works for both 2-segment and 3-segment numbers)
grep -n -A 80 '^## RALJ 2\.4$' rules.md
grep -n -A 80 '^## RALJ 6\.3\.1$' rules.md

# Find every rule that mentions a topic
grep -in -B1 -A2 'transcript'   rules.md
grep -in -B1 -A2 'notice of appeal' rules.md
grep -in -B1 -A2 'cost bill'    rules.md
grep -in -B1 -A2 'stay'         rules.md

# Cross-reference: which rules cite another rule (e.g. 9.3)
grep -in 'rule 9\.3\|RALJ 9\.3' rules.md
```

## Citation format

- `RALJ 2.4` (two-segment: title.rule)
- `RALJ 6.3.1` (three-segment for the inserted/renumbered transcript rule)
- `RALJ 9.3(c)(4)` (subsection lettering preserved in body text)
- Adoption history is printed at the foot of each rule, e.g. `[Adopted effective January 1, 1981; Amended effective September 25, 2018.]`

## Caveats

- **Headings carry the rule number only.** The descriptive title (e.g. 'SCOPE OF RULES', 'COSTS') appears one or two lines into the body text rather than in the `##` heading.
- **`RALJ 2.7` is `[RESERVED]`.** Intentional — preserved as a one-line section so the numbering sequence stays intact.
- **`RALJ 6.3.1` was originally adopted as `RALJ 6.3A`** and renumbered effective 2002-06-25 (noted in its adoption history). Both forms may appear in older case law; the consolidated file uses the current `6.3.1` form.
- **Adjacent rules not in this corpus:** RAP (appeals from superior court), CRLJ / CrRLJ / IRLJ (trial procedure in courts of limited jurisdiction), CRLJ 73/75 (de novo review of small claims and of decisions by non-attorney judges — explicitly excluded by RALJ 1.1(b)). Direct the user to those rule sets when out of scope.
- **Snapshot is static.** Some rules cite RCW provisions (e.g. `RCW 10.101.010(3)(a)-(c)` in RALJ 9.3); confirm RCW text against the current code, not from this corpus.
