---
name: wa-rpc-rules-of-professional-conduct
description: Use when the user asks about, cites, quotes, or compares Washington State's Rules of Professional Conduct — the ethics rules governing Washington lawyers (competence, confidentiality, conflicts of interest, fees, candor toward the tribunal, advertising, unauthorized practice, etc.). Triggers on citations like "RPC 1.6", "RPC 1.7(b)", "RPC 3.3", "RPC 8.4", references to "Washington RPC" or "WA Rules of Professional Conduct", and questions about lawyer ethics, attorney discipline standards, IOLTA/trust accounts (RPC 1.15A/1.15B), or the Preamble/Fundamental Principles. Do NOT use for: judicial conduct (CJC), bar admission rules (APR), discipline procedure (ELC), CLE rules (APR 11), or rules of professional conduct from other states.
---

# Washington State Rules of Professional Conduct (RPC)

**Effective date of this snapshot:** 2026-05-20.

**Fidelity verdict:** FAITHFUL. Rule numbers, subsection lettering ((a), (b)(2), etc.), bracketed Comment numbers ([1], [2]), and adoption/amendment history lines are preserved verbatim. No multi-column corruption (the body text is single-column throughout). Smart quotes preserved as UTF-8.

## Files

```
rules-of-professional-conduct/
├── README.md   ← you are here
└── rules.md    ← all 67 RPC rules (incl. Preamble, Fundamental Principles, Appendix)
```

## Looking up a rule

```bash
# Full text of a numbered rule (use word boundary so "RPC 1.1" doesn't match "RPC 1.10"):
grep -n -A 200 -E '^## RPC 1\.6$' rules.md

# A rule plus its Comments (most rules run 100–500 lines):
awk '/^## RPC 1\.7$/,/^## RPC /' rules.md | head -500

# Subsection text — search the rule body for "(b)(2)":
grep -n -A 3 -B 1 '(b)(2)' rules.md | head

# The Preamble, Fundamental Principles, or Appendix:
grep -n -A 300 '^## RPC — Preamble and Scope$' rules.md
grep -n -A 100 '^## RPC — Fundamental Principles$' rules.md
grep -n -A 400 '^## RPC — Appendix$' rules.md

# List every rule heading (table of contents):
grep -n '^## RPC' rules.md
```

## Citation format

- `RPC 1.1` — rule number only
- `RPC 1.6(b)(2)` — rule with subsection and sub-subsection
- `RPC 1.7 cmt. [3]` — comment citation (comments are bracketed-numbered in the source)
- `RPC 1.15A` — letter-suffixed rules (1.0A, 1.0B, 1.15A, 1.15B all exist)
- `RPC Preamble [4]` or `RPC Scope [14]` — Preamble and Scope are paragraph-numbered
- `RPC Fundamental Principles` — the non-numbered aspirational statement
- `RPC App.` — the Appendix (Guidelines for Applying the RPCs)

## Caveats

- **Filename-derived sort order.** Rules are ordered by source filename: `01_07_00`, `01_08_00`, `01_09_00`, then `01_0A_00`, `01_0B_00`, then `01_10_00` … This means RPC 1.0A and 1.0B appear between 1.9 and 1.10 in `rules.md`, not at the start of Article 1. Use `grep '^## RPC'` to find the actual line for any rule rather than assuming numeric order.
- **Preamble and Fundamental Principles up top.** Per the source corpus, the Preamble & Scope and the Fundamental Principles (a non-numbered aspirational statement, formerly the 1985 Preamble) are placed at the very top of `rules.md`, before RPC 1.1. The Appendix is placed at the very bottom.
- **RPC 7.2 and RPC 2.2 are [RESERVED].** These rules are intentionally near-empty in the source — not a conversion defect.
- **Adoption/amendment history is inside each rule.** Lines like `[Adopted effective September 1, 1985; Amended effective ...]` appear at the end of each rule's blackletter text and again, where applicable, at the end of individual comments. These are part of the official text.
- **Indentation is whitespace-only.** The body text preserves visual indentation with leading spaces; do not assume markdown list semantics. When quoting, strip the leading spaces.
- **Comments are official commentary, not the rule itself.** When citing, distinguish `RPC 1.7(b)(4)` (blackletter) from `RPC 1.7 cmt. [29]` (commentary). The Washington Supreme Court adopts the rule; comments are explanatory.
