---
name: wa-er-rules-of-evidence
description: Use when the user asks about, cites, quotes, or compares the Washington State Rules of Evidence — admissibility, relevance, hearsay, privileges, witnesses, opinion testimony, authentication, or the best-evidence rule in Washington courts. Triggers on citations like "ER 401", "ER 404(b)", "ER 802", "ER 803(a)(2)", "WA evidence rule", "Washington hearsay exception". Do NOT use for the Federal Rules of Evidence (FRE), other states' evidence codes, Washington Civil/Criminal Procedure rules (CR/CrR), or for the RCW statutes referenced inside individual rules (e.g., RCW 5.45, RCW 5.44).
---

# Washington Rules of Evidence (ER)

**Effective date of this snapshot:** 2026-05-20.

**Fidelity verdict:** FAITHFUL. All 67 rules render cleanly: single-column statutory text; no tables; subsection lettering, indentation, and `[Adopted/Amended effective ...]` provenance lines preserved.

## Files

```
rules-of-evidence/
├── README.md   ← you are here
└── rules.md    ← all 67 ER rules, concatenated in rule-number order
```

## Looking up a rule

```bash
# A whole rule by number (works for 3- or 4-digit rule numbers)
grep -n -A 200 -E '^## ER 802$' rules.md

# Just the section heading + first lines
grep -n -A 5 -E '^## ER 404$' rules.md

# Find every hearsay exception that mentions "business" or "regularly conducted"
grep -n -B 1 -A 4 -iE 'regularly conducted|business records' rules.md

# List all rule headings
grep -nE '^## ER ' rules.md
```

## Citation format

- `ER 401` — Definition of "relevant evidence"
- `ER 404(b)` — Other crimes, wrongs, or acts
- `ER 802` — The hearsay rule
- `ER 803(a)(2)` — Excited utterance exception
- `ER 901(b)(1)` — Authentication by witness with knowledge
- `ER 1101` — Applicability of the rules

When the rule body cross-references the RCW (e.g., "[Reserved. See RCW 5.45.]"), cite the RCW for the substantive content; cite the ER number for the placeholder/reservation.

## Coverage (Articles I–XI)

| Article | Rules | Subject |
|---------|-------|---------|
| I       | ER 101–106  | General provisions |
| II      | ER 201      | Judicial notice |
| III     | ER 301–302  | Presumptions |
| IV      | ER 401–413  | Relevancy and its limits |
| V       | ER 501–502  | Privileges |
| VI      | ER 601–615  | Witnesses |
| VII     | ER 701–706  | Opinions and expert testimony |
| VIII    | ER 801–807  | Hearsay |
| IX      | ER 901–904  | Authentication and identification |
| X       | ER 1001–1008| Contents of writings, recordings, photographs |
| XI      | ER 1101–1103| Miscellaneous |

## Caveats

- Several rules are placeholders that defer to the RCW — notably `ER 803(a)(6)` ("Records of Regularly Conducted Activity. [Reserved. See RCW 5.45.]") and `ER 803(a)(8)` ("Public Records and Reports. [Reserved. See RCW 5.44.040.]"). The RCW text is not in this corpus.
- A handful of rules are `[RESERVED]` placeholders (e.g., `ER 1102` Amendments). They are real ER numbers, not omissions.
- Each rule preserves its full amendment history line (`[Adopted effective ...]`, `[Amended effective ...]`) at the end of the body. Use that line to confirm the version date when quoting.
- Most rules also carry a `Comment {N}` block; the dominant marker is `[Deleted effective September 1, 2006.]`, meaning the official drafter's comments were withdrawn — body text remains authoritative.
- Header lines such as the running "ER {N}" / "{TITLE}" appear at the top of each section body in addition to the synthetic `## ER {N}` heading — strip the centered-caps duplicate when quoting.
