---
name: wa-rap-rules-of-appellate-procedure
description: Use when the user asks about, cites, quotes, or compares the Washington Rules of Appellate Procedure — the rules that govern review by Washington's Court of Appeals and Supreme Court (notice of appeal, discretionary review, briefs, record on review, motions, attorney fees, costs, personal restraint petitions, and the official RAP forms). Triggers on citation forms like "RAP 2.5", "RAP 2.5(a)(3)", "RAP 18.1", "RAP Form 17", or phrases like "rules of appellate procedure," "appellate brief requirements," "PRP," "personal restraint petition," "RALJ versus RAP." Do NOT use for trial court civil/criminal practice (see CR, CrR, CRLJ, CrRLJ), small-claims-court appeals from courts of limited jurisdiction (see RALJ), or federal appellate practice.
---

# Washington Rules of Appellate Procedure (RAP)

**Effective date of this snapshot:** 2026-05-20.

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Body text, subsection lettering, and citation references are clean. Caveats are limited to the official forms (which include layout artifacts like signature blocks and caption boxes) and a handful of `[RESERVED.]` rule slots.

Scope: appellate practice in Washington's Court of Appeals (Divisions I, II, III) and the Washington Supreme Court — review of trial court decisions, briefs, motions, costs, attorney fees, personal restraint petitions, and the official RAP forms.

## Files

```
rules-of-appellate-procedure/
├── README.md   ← you are here
└── rules.md    ← all 180 RAP rules and forms, concatenated
```

## Looking up a rule

```bash
# Pull a specific rule with surrounding context
grep -n -A 80 -E '^## RAP 2\.5$' rules.md

# Pull a subsection like RAP 2.5(a)(3)
grep -n -B 1 -A 4 -E '\(a\)\(3\)' rules.md | head -40

# Show every rule heading (table of contents)
grep -n '^## RAP ' rules.md

# Find all references to a concept across the rules
grep -n -i 'personal restraint' rules.md

# Pull a specific form
grep -n -A 200 -E '^## RAP Form 17$' rules.md
```

## Citation format

- `RAP 2.5(a)(3)` — rule, subsection, paragraph (the manifest-error-affecting-a-constitutional-right exception).
- `RAP 18.1` — attorney fees and expenses on review.
- `RAP 10.3(a)(6)` — argument section of an appellant's brief.
- `RAP 16.4` — grounds for relief by personal restraint petition.
- `RAP Form 17` — Personal Restraint Petition form for persons confined by state or local government.

Always quote the rule number as `RAP {N}.{N}` (no leading zeros).

## Caveats

- **Reserved slots.** Several rule numbers are placeholders — e.g. `RAP 18.18 through 18.20` shows `[RESERVED.]`. Do not quote substantive text from a reserved rule.
- **Obsolete forms.** Some form files (e.g. `RAP Form 12A`) are marked `[OBSOLETE]`. Treat them as historical only.
- **Form fidelity.** The 30 RAP forms appear as plain text — caption boxes, signature lines, and ruled fillable areas render as ASCII artifacts (lines of underscores, parenthesis brackets in column form). Useful for grep and for confirming form names/numbers; the layout is not authoritative for filing.
- **Running page headers.** Some converted rules carry a `Page N of M` style artifact near footnote breaks; strip those when quoting.
- **Amendment dates.** Each rule typically ends with a bracketed adoption/amendment history (e.g. `[Adopted effective July 1, 1976; Amended effective ... April 29, 2025.]`). The latest amendment date in this snapshot is April 29, 2025. Anything adopted or amended after that is not in this corpus.
- **RAP vs. RALJ.** The RAP governs review by the Court of Appeals and Supreme Court. Appeals from courts of limited jurisdiction to superior court are governed by the RALJ — a separate rule set in this corpus.
