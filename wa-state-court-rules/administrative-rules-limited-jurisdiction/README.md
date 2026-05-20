---
name: wa-arlj-administrative-rules-limited-jurisdiction
description: Use when the user asks about, cites, quotes, or compares Washington State Administrative Rules for Courts of Limited Jurisdiction (ARLJ) — administrative rules governing district and municipal courts (definitions, court administration, probation departments, mandatory court administrator education, presiding judge duties). Triggers on citations like "ARLJ 3", "ARLJ 11", "ARLJ 14 Standards", and on questions about Washington district/municipal court administration rules. Do NOT use for CrRLJ (criminal rules), CRLJ (civil rules), IRLJ (infraction rules), RALJ (appellate rules from CLJ), GR (general rules), or Washington statutes/RCWs.
---

# ARLJ — Administrative Rules for Courts of Limited Jurisdiction (Washington State)

**Effective date of this snapshot:** 2026-05-20.

**Fidelity verdict:** FAITHFUL. Body text, subsection lettering ((a), (1)), section headings, and citation references are preserved cleanly across all 16 rules. Several rules are marked [RESCINDED] in source and are preserved as such.

## Files

```
administrative-rules-limited-jurisdiction/
├── README.md   ← you are here
└── rules.md    ← all 16 ARLJ rules + ARLJ 14 Standards companion
```

## Looking up a rule

```bash
# Pull a specific rule (with following context)
grep -n -A 80 -E '^## ARLJ 11$' rules.md

# Pull the standards document under ARLJ 14
grep -n -A 250 -E '^## ARLJ 14 Standards$' rules.md

# Find every ARLJ rule that defines a term
grep -n -i 'means' rules.md

# Find probation-related rules
grep -n -i 'probation' rules.md

# Find rescinded rules
grep -n -B1 -A2 'RESCINDED' rules.md
```

## Citation format

- `ARLJ 1` (rule number)
- `ARLJ 7` (rescinded rule — note status when quoting)
- `ARLJ 11.2(a)(1)` (rule, subrule, subsection, item)
- `ARLJ 14 Standards § 2(1)` (the separate Standards document under ARLJ 14)

## Rule inventory

| Rule | Subject | Status |
|------|---------|--------|
| ARLJ 1 | Qualifying Examination of Lay Candidates for Justice of the Peace | RESCINDED (1981) |
| ARLJ 2 | (see rules.md) | active |
| ARLJ 3 | Definition of Terms | active (amended 2024) |
| ARLJ 4 | (see rules.md) | active |
| ARLJ 5 | (see rules.md) | active |
| ARLJ 6 | (see rules.md) | active |
| ARLJ 7 | (rescinded) | RESCINDED (1997) |
| ARLJ 8 | (see rules.md) | active |
| ARLJ 9 | (see rules.md) | active |
| ARLJ 10 | (see rules.md) | active |
| ARLJ 11 | Misdemeanant Probation Department | active (amended 2024, 2025) |
| ARLJ 12 | (see rules.md) | active |
| ARLJ 13 | (see rules.md) | active |
| ARLJ 14 | Mandatory Continuing Court Administrator Education | active (adopted 2023) |
| ARLJ 14 Standards | DMC Administrator Mandatory CE Standards | adopted 2023 |
| ARLJ 15 | (see rules.md) | active |

## Caveats

- **Rescinded rules retained.** ARLJ 1 (rescinded 1981) and ARLJ 7 (rescinded 1997) are included with their rescission notices. Do not quote substantive language from these as currently operative.
- **ARLJ 14 Standards is a separate document** from ARLJ 14 itself. They are companion texts and should be cited distinctly.
- **Running headers.** A few rules have repeated court-name/page-number lines interleaved between paragraphs. Strip them when quoting verbatim.
- **Snapshot, not live.** This corpus is dated 2026-05-20; if the user needs the current rule, they should consult the official source published by the Washington Courts.
- **Out of scope.** Does not contain CrRLJ, CRLJ, IRLJ, RALJ, GR, CrR, CR, RAP, ER, or any RCW chapter. Route those elsewhere.
