---
name: wa-gr-general-rules
description: Use when the user asks about, cites, quotes, or compares Washington State General Rules (GR) — the cross-cutting court rules governing all Washington courts (judicial conduct, access to court records, electronic filing, indigency, attorney licensing, interpreters, jury source lists, and similar). Triggers on citations like "GR 14", "GR 15", "GR 22", "GR 31", "GR 33", "GR 36", "GR 37", "GR 39", or phrasings like "general rule 14", "Washington GR", "WA General Rules". Do NOT use for Civil Rules (CR), Criminal Rules (CrR), Rules of Appellate Procedure (RAP), Evidence Rules (ER), Rules of Professional Conduct (RPC), or any local court rules — those have their own per-topic skills.
---

# General Rules (Washington State Courts)

**Effective date of this snapshot:** 2026-05-20.

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Body text, subsection lettering (a/b/c, (1)/(2)/(3)), citation references, and amendment-history brackets are preserved cleanly as a single-column transcript. A few rules contain mandatory pattern forms (GR 39) and a Bluebook-style abbreviations table (GR 14 Appendix) that render as space-aligned text rather than markdown tables — usable for grep and citation but reformat before quoting.

## Files

```
general-rules/
├── README.md   ← you are here
└── rules.md    ← all 58 GR rules, concatenated in rule-number order
```

## Looking up a rule

```bash
# Pull a specific rule plus the next ~80 lines of body
grep -n -A 80 -E '^## GR 14$' rules.md

# Find a rule by subject keyword
grep -ni 'interpreter' rules.md

# List every rule heading (table of contents)
grep -n '^## GR ' rules.md

# Pull a sub-rule (e.g. GR 14.1)
grep -n -A 60 -E '^## GR 14\.1$' rules.md
```

## Citation format

- `GR 14` — top-level rule (e.g. "Format and Style of Papers Presented for Filing").
- `GR 31` — top-level rule (e.g. "Access to Court Records").
- `GR 14.1`, `GR 31.1` — numbered sub-rule.
- `GR 14 Appendix 1`, `GR 26 Standards`, `GR 25 Appendix` — appendices and standards documents that ship with the parent rule.
- Always cite the rule, not the source filename.

## Caveats

- **Rescinded / reserved rules are present.** Several entries (e.g. GR 4, GR 8, GR 11, GR 19) are short stubs marked `[RESCINDED]` or `[RESERVED]`. They are intentionally retained so the numbering matches the official corpus; do not quote them as substantive law.
- **GR 14 Appendix 1** is the Office of Reporter of Decisions Style Sheet — a Bluebook exception list with a two-column TITLE/ABBREVIATION table. Columns are preserved as aligned spaces, not pipe-tables; reformat when quoting.
- **GR 39** embeds the mandatory pattern petition form (Petition re: Legal Financial Obligations) after the rule text. Checkbox glyphs render as `[ ]`. The form is provided for grep/reference only, not for filing.
- **GR 26 Standards** is a separate "Bail Bond Agency Surety Standards" companion document, not a numbered sub-rule. It appears under the `## GR 26 Standards` heading.
- **GR 25 Appendix** is the Mental Proceedings Forms companion. Same caveat as GR 39 — reference only, not for filing.
- **Effective dates** are recorded in bracketed adoption/amendment lines at the end of each rule (e.g. `[Adopted effective ...; amended effective ...]`). Use these to determine whether your question concerns a still-in-force version.
- **Sub-rule numbering:** Sub-rules use canonical citation form (`GR 14.1`, `GR 14.2`, etc.); no leading zeros.
- **Repeated page headers/footers** ("GR N", rule title repeated) appear inline at the top of each section — harmless for grep, strip when quoting.
