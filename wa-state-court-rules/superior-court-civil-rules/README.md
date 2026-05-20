---
name: wa-cr-superior-court-civil-rules
description: Use when the user asks about, cites, quotes, or compares Washington Superior Court Civil Rules (CR) — the rules governing civil procedure in Washington State superior courts (pleadings, motions, discovery, depositions, summary judgment, class actions, trial, judgments). Triggers on citations like `CR 56`, `CR 12(b)(6)`, `CR 23(b)(3)`, "Washington civil rule," "Wa. Super. Ct. Civ. R." Do NOT use for Civil Rules for Courts of Limited Jurisdiction (CRLJ), Criminal Rules (CrR/CrRLJ), Rules of Evidence (ER), General Rules (GR), Appellate Rules (RAP), federal civil procedure (FRCP), or county-specific local rules.
---

# Superior Court Civil Rules (Washington State)

**Effective date of this snapshot:** 2026-05-20.

**Fidelity verdict:** FAITHFUL. Body text, lettered/numbered subsections, citations, and adoption/amendment history are clean. No multi-column or table content in this rule set; centered-banner headings (`CR N` / title) reproduce with leading whitespace but remain readable and grep-able.

## Files

```
superior-court-civil-rules/
├── README.md   ← you are here
└── rules.md    ← all 96 CR rules, concatenated in rule-number order
```

## Looking up a rule

```bash
# Pull one whole rule (heading + body) — adjust -A line count for longer rules
grep -n -A 80 -E '^## CR 56$' rules.md
grep -n -A 200 -E '^## CR 26$' rules.md     # CR 26 is one of the longest
grep -n -A 300 -E '^## CR 30$' rules.md     # depositions; ~300 lines

# Find every subsection of a rule
grep -n -E '^\s*\(b\)' rules.md             # noisy — narrow with rule context

# List every rule heading
grep -n '^## CR ' rules.md

# Search across the rule set for a term
grep -n -i 'summary judgment' rules.md
grep -n -i 'class action' rules.md
```

## Citation format

- `CR 56` — whole rule (summary judgment)
- `CR 12(b)(6)` — rule + lettered + numbered subsection
- `CR 23(b)(3)` — class action predominance / superiority
- `CR 26(b)(4)` — discovery scope, expert trial-preparation materials
- `CR 30(b)(6)` — organizational deposition
- Long form: "Wash. Super. Ct. Civ. R. 56" or "Wa. R. Civ. P. 56"

## Caveats

- **Two headings per rule.** Each rule begins with the synthetic `## CR N` heading (the canonical anchor for grep) immediately followed by a centered banner (e.g. `CR 56` / `SUMMARY JUDGMENT`). Don't quote the duplicate banner — the synthetic heading is the citation anchor.
- **Reserved rules retained.** `CR 53` (Masters), `CR 61` (Harmless Error), `CR 72-76` (Appeals), and `CR 84` (Forms) all appear as `[RESERVED]` placeholders. Substantive Master rules live in `CR 53.1` through `CR 53.4`.
- **`CR 2A` (Stipulations)** sorts between `CR 2` and `CR 3` in this file; the synthetic heading is `## CR 2A`.
- **`CR 72-76`** is a single combined entry containing only the `[RESERVED]` notice and a section header "9. APPEALS." Treat as a single anchor.
- **Adoption / amendment history** appears at the bottom of each rule in brackets, e.g. `[Adopted effective July 1, 1967; Amended effective ...]`. Useful for "when did this take effect?" questions.
- **Leading whitespace** is preserved in the body text; quotes copied raw will look indented. Strip leading whitespace when quoting.
- **Smart quotes / apostrophes** convert as UTF-8 curly quotes (`’`, `"`). They will copy-paste correctly but may not match plain ASCII in grep — use `[’\']` or just `'` patterns when in doubt.
- **96 rules, one heading per rule.** Small entries are legitimately `[RESERVED]`.
