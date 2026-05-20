---
name: wa-crlj-civil-rules-limited-jurisdiction
description: Use when the user asks about, cites, quotes, or compares Washington State Civil Rules for Courts of Limited Jurisdiction (CRLJ) — the civil procedure rules that govern district courts and municipal courts (not Superior Court). Triggers on citations like "CRLJ 56", "CRLJ 4", "CRLJ 45", phrases like "civil rules for limited jurisdiction," "district court civil procedure," "small claims procedure," or comparisons with Superior Court CR rules. Do NOT use for Superior Court civil procedure (use CR), criminal rules (CrRLJ / CrR), traffic infractions (IRLJ), or appellate rules (RALJ / RAP).
---

# CRLJ — Civil Rules for Courts of Limited Jurisdiction (Washington State)

**Effective date of this snapshot:** 2026-05-20.

**Jurisdictional scope:** CRLJ governs civil procedure in Washington State **courts of limited jurisdiction** — i.e., district courts and municipal courts. Superior Court civil practice is governed by the parallel **CR** rules. Many CRLJ rules mirror the CR rules but with limited-jurisdiction adaptations (lower dollar thresholds, simplified pleading, district-court-specific service mechanics). Always cite the CRLJ rule, not the analogous CR rule, when the matter is in district or municipal court.

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Body text, subsection lettering ((a), (b), (1), (A)…), adoption/amendment history, and cross-references are clean. Several rules are `[RESERVED]` placeholders in the source corpus (e.g., CRLJ 16, 23, 27–37, 39, 57) — that is the source text, not a conversion loss. Range files (`CRLJ 27 through 37`, `65-67`, `69-70`, `78-80`, `86.04-99.04`) appear under a single heading reflecting the source grouping.

## Files

```
civil-rules-limited-jurisdiction/
├── README.md   ← you are here
└── rules.md    ← all 82 CRLJ rules, concatenated
```

## Looking up a rule

```bash
# Pull a specific rule with generous context
grep -n -A 80 -E '^## CRLJ 56\b' rules.md
grep -n -A 60 -E '^## CRLJ 4\b'  rules.md       # service of process
grep -n -A 60 -E '^## CRLJ 45\b' rules.md       # subpoenas

# List every rule heading in this corpus
grep -n '^## CRLJ ' rules.md

# Keyword search across the whole corpus
grep -n -i 'summary judgment\|default\|small claims' rules.md
```

## Citation format

- `CRLJ 56` — summary judgment
- `CRLJ 56(c)` — subsection
- `CRLJ 45(c)(3)(A)(i)` — deeply nested subsection
- `CRLJ 4.2` — sub-numbered rule (appears in `rules.md` as `## CRLJ 4.2`)
- For ranges like `CRLJ 27`–`CRLJ 37`, the snapshot shows them under a single `## CRLJ 27-37` heading because the source groups reserved rules.

Sort order is canonical (so `CRLJ 13` precedes `CRLJ 13.4`, `CRLJ 14A` precedes `CRLJ 14`).

## Caveats

- **Limited jurisdiction only.** Do not apply CRLJ to Superior Court matters. If the user's question is about Superior Court civil procedure, redirect them to the CR corpus.
- **Reserved rules.** CRLJ 16, 23, 39, 57, and the ranges 27–37, 65–67, 69–70, 78–80, 86.04–99.04 are `[RESERVED]` in the source. Cite the reservation rather than inferring content from CR.
- **Heading sort quirk.** `CRLJ 14A` appears immediately before `CRLJ 14` in this file (ASCII ordering of the source numbering). When a user asks for rules in strict numeric order, walk the headings and reorder mentally.
- **Tables and forms** are rare but, where present, render as space-aligned columns — usable for grep, but treat column alignment as visual hints rather than authoritative tabular data.
- **Effective dates / amendment histories** appear at the end of each rule in square brackets, e.g. `[Adopted effective September 1, 1984; Amended ... October 1, 2024.]`. Quote these verbatim when version matters.
