---
name: wa-kitsap-county-local-rules
description: Use when the user asks about Kitsap County (Washington) Superior Court local rules — the Port Orchard-seated court. Kitsap uses KCL- prefixes — KCLCR (civil), KCLAR (arbitration), KCLFLR (family law), KCLCrR (criminal), KCLGR (general), KCLSPR (special proceedings). Kitsap also has 8 emergency rule supplements active alongside the main rule set — invoke this skill when the user asks about any Kitsap rule whose current text might depend on a supplement.
---

# Kitsap County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025 (main rules). Each emergency rule supplement has its own effective date inside the file.

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Body text, lettered/numbered subsections, ALL-CAPS warning blocks, phone numbers, email addresses, and amendment trailers are preserved verbatim. Source-PDF tracked-edit strikethroughs survive in markdown as `~~text~~` artifacts (e.g., `noted ~~n~~ ot later`, `docket ~~s~~`); ignore these when quoting. Cite from `local-rules.md` and the supplements directly.

## Files

```
kitsap/
├── README.md                       ← you are here
├── local-rules.md                  main consolidated local rules
├── emergency-rule-01.md            ER01
├── emergency-rule-02.md            ER02
├── emergency-rule-03.md            ER03
├── emergency-rule-04.md            ER04
├── emergency-rule-05.md            ER05
├── emergency-rule-06.md            ER06
├── emergency-rule-07.md            ER07
└── emergency-rule-08.md            ER08
```

## Kitsap's prefix convention

Kitsap uses **KCL- prefixes** throughout:

| Kitsap prefix | Domain                                |
|---------------|---------------------------------------|
| KCLCR         | Civil rules                           |
| KCLAR         | Arbitration                           |
| KCLFLR        | Family law                            |
| KCLCrR        | Criminal                              |
| KCLGR         | General                               |
| KCLSPR        | Special Proceedings                   |
| KCLJuCR       | Juvenile                              |

## Critical: always check the supplements

A Kitsap rule answered only from `local-rules.md` is incomplete. Supplements amend specific rules without restating the rest. Right pattern:

```bash
# Every occurrence of KCLCR 7 across main + all 8 supplements
grep -rni -E 'KCLCR ?7\b' .

# Quick subject scan of all supplements
for f in emergency-rule-*.md; do echo "=== $f ==="; head -10 "$f"; done
```

If a supplement covers the rule the user asked about, **the supplement controls** (it's an emergency amendment). Cite both: main rule for context, supplement for current operative text.

## Citation format

- Main rule: `Kitsap County KCLCR 7(b)(1)(A)`
- Main rule: `Kitsap County KCLCR 77(k)(11)(B)(i)`
- Emergency supplement: `Kitsap County KCLCR 7 (Emergency Rule 4)` — name both the rule and the supplement number. State the supplement's effective date if it's printed in the file.

## Caveats

- **Always check the supplements** for the rule in question — see above.
- **Eight supplements in this snapshot** (ER01–ER08). If a user references a Kitsap "ER09" or later, it post-dates this snapshot.
- **Tracked-edit strikethrough artifacts** (e.g., `~~n~~ ot`, `docket ~~s~~`) appear in `local-rules.md` because the source PDF showed them. Read past the strikethroughs — the rule text is what comes after.
- **Duplicated TOC.** The table of contents appears twice at the top (once as a flowing list, once as a markdown table). Skip the TOC when answering body-text questions.
- **Running headers/footers** ("Rule N — page banner", "pg. N") appear inline between paragraphs. Strip them when quoting.
- **Hyperlinks rendered as plain text** — expected.
