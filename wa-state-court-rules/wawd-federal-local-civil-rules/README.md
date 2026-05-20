---
name: wawd-local-civil-rules
description: Use when the user asks about, cites, quotes, or compares the Local Civil Rules of the U.S. District Court for the Western District of Washington (W.D. Wash., federal court seated in Seattle and Tacoma). Triggers on "WAWD", "W.D. Wash.", "Western District of Washington", "federal court Seattle", "federal court Tacoma", and citation forms like `WAWD LCR 7(d)(3)`, `WAWD LCR 5(g)`, `LCR 26`, `LCR 39.1`, `LCR 83.3`. Do NOT use for Washington state Superior Court rules (CR / CrR / GR), King County local rules (LCR/LR/LCrR under state CR), the Eastern District of Washington (E.D. Wash.), or the Ninth Circuit Rules — those are different rule sets even though the abbreviations overlap.
---

# WAWD — U.S. District Court for the Western District of Washington, Local Civil Rules

**Effective date of this snapshot:** 2026-05-20.

**This is a FEDERAL court rule set.** W.D. Wash. is a U.S. District Court, not a state court. Its "LCR" numbering parallels the Federal Rules of Civil Procedure (LCR 7 ↔ Fed. R. Civ. P. 7, LCR 56 ↔ Fed. R. Civ. P. 56, etc.). Do not conflate with Washington state Superior Court CR, or with King County LCR.

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Body text, subsection lettering ((a), (b), (1), (2), (A), (B)), and rule numbering preserved cleanly. Some running page footers and centered "LCR N" banner headings ended up inline before cleanup; the consolidated markdown promotes recognizable `LCR N` banners to `## LCR N` headings. A handful of cross-reference mentions of `LCR N` inside the body became second-level headings too — harmless for grep, just be aware the heading count exceeds the rule count.

## Files

```
wawd-federal-local-civil-rules/
├── README.md   ← you are here
└── rules.md    ← entire consolidated WAWD Local Civil Rules document
```

WAWD publishes its local civil rules as a single bundled document, so this markdown is not split per rule — one document, internal `## LCR N` headings.

## Looking up a rule

```bash
# Pull a specific rule with surrounding context
grep -n -A 80 -E '^## LCR 7$' rules.md
grep -n -A 120 -E '^## LCR 26$' rules.md
grep -n -A 80 -E '^## LCR 56$' rules.md

# Subsection-level lookup (e.g., the meet-and-confer requirement in LCR 37)
grep -n -B 2 -A 8 'LCR 37(a)' rules.md

# Topic search across the whole rule set
grep -ni 'noting date' rules.md
grep -ni 'attorney.s fees' rules.md
grep -ni 'mediation' rules.md
```

## Coverage (rules present in this snapshot)

LCR 1, 2, 3, 4, 4.1, 5, 5.1, 5.2, 6, 7, 7.1, 8, 9, 10, 11, 15, 16, 16.1, 17, 23, 23.1, 23.2, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 39.1 (court-referred arbitration), 39.2 (mediation), 40, 41, 42, 43, 47, 51, 54, 55, 56, 56.1, 65, 65.1, 66, 67, 72, 73, 77, 78, 79, 80–83 (reserved), 83.1, 83.2, 83.3.

LCR numbering is harmonized with the Federal Rules of Civil Procedure; gaps (e.g., no LCR 12 between LCR 11 and LCR 15) are intentional — that subject is fully governed by the corresponding FRCP rule with no local supplement.

## Citation format

- `WAWD LCR 7(d)(3)` — Western District local civil rule, with subsection.
- `WAWD LCR 5(g)` — sealing / redaction provision.
- `W.D. Wash. LCR 26(f)` — long-form jurisdiction-prefixed citation.
- `LCR 39.1(c)(3)` — short form when WAWD context is already established.

When citing alongside a parallel federal rule: `Fed. R. Civ. P. 56; WAWD LCR 56(b)`.

## Caveats

- **Federal, not state.** If the user is asking about a King County or Pierce County state-court matter, this is the wrong rule set — they want CR / KCLR / PCLR.
- **Snapshot only.** WAWD periodically amends its local rules; for filing-critical work, the user should confirm against the canonical source dated after 2026-05-20.
- **Fee schedule is not embedded.** Both LCR 3 and LCR 79 reference an external "Fee Schedule … available on the court's website." The dollar amounts themselves are not reproduced in this snapshot.
- **Sample forms (LCR 37 submission template, etc.) at the tail of the document** were laid out in a multi-column legal-pleading style and appear here as a column of line-numbered fragments. Use them for keyword search only — they are not authoritative as a filing format. Reference LCR 37 in the rule body itself for the actual requirements.
- **Running page footers** ("Page N of M", court name) appear interleaved between paragraphs in places. Strip them when quoting.
- **`## LCR N` heading count > rule count.** Cross-reference mentions of `LCR N` that appeared on their own line in the original layout were also promoted to headings. Anchor on the first occurrence (or rely on the leading paragraph naming the rule) when reading a specific rule.
