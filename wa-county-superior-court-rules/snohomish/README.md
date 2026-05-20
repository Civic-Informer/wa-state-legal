---
name: wa-snohomish-county-local-rules
description: Use when the user asks about Snohomish County (Washington) Superior Court local rules — the Everett-seated court. Snohomish uses SCL- prefixes — SCLCR (civil), SCLSPR (special proceedings, includes family/dependency), and related families. Snohomish has 9 emergency rule supplements alongside the main rule set — invoke this skill when the user asks about any Snohomish rule whose current text might be governed by a supplement.
---

# Snohomish County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2025 (main rules). Each emergency rule supplement has its own effective date inside the file.

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Body text, lettered/numbered subsections, summary-judgment carve-outs, electronic-filing URLs, and amendment-history brackets are preserved verbatim. Two specific defects to know about — see Caveats. Cite from `local-rules.md` and the unique supplements directly.

## Files

```
snohomish/
├── README.md                       ← you are here
├── local-rules.md                  main consolidated local rules
├── emergency-rule-01.md            ER01  ← UNIQUE
├── emergency-rule-02.md            ER02  ← UNIQUE (Rule 30 — Electronic Filing, eff. 8/13/2025)
├── emergency-rule-03.md            ER03  (DUPLICATE of ER01)
├── emergency-rule-04.md            ER04  (DUPLICATE of ER02)
├── emergency-rule-05.md            ER05  ← UNIQUE (Rule 41 — Dismissal, eff. 3/30/2026)
├── emergency-rule-06.md            ER06  ← UNIQUE (Rule 94.04 — Family Law, eff. 3/30/2026)
├── emergency-rule-07.md            ER07  ← UNIQUE (Rule 0.02 — Court Organization, eff. 5/1/2026)
├── emergency-rule-08.md            ER08  (DUPLICATE of ER01)
└── emergency-rule-09.md            ER09  (DUPLICATE of ER02)
```

## Snohomish's prefix convention

Snohomish uses **SCL- prefixes** throughout:

| Snohomish prefix | Domain                                |
|------------------|---------------------------------------|
| SCLCR            | Civil rules                           |
| SCLSPR           | Special Proceedings (incl. family/dependency) |
| SCLCrR           | Criminal                              |
| SCLGR            | General                               |
| SCLAR / SCLMAR   | Arbitration                           |

## ⚠️ Duplicate-content caveat

The upstream server published byte-identical PDFs at several emergency-supplement URLs. Only **5 unique emergency documents** exist in this directory: ER01, ER02, ER05, ER06, ER07. The duplicates are retained because courts.wa.gov lists them as distinct numbered supplements with different posting dates, but the operative content is the same.

When searching emergency supplements, read only the 5 unique files:

```bash
ls emergency-rule-0{1,2,5,6,7}.md
```

## Critical: always check the supplements

A Snohomish rule answered only from `local-rules.md` is incomplete. Supplements override or amend specific rules. Right pattern:

```bash
# Every occurrence of SCLCR 30 across main + unique supplements
for f in local-rules.md emergency-rule-0{1,2,5,6,7}.md; do
  grep -niH -E 'SCLCR ?30\b|Rule ?30\b' "$f"
done

# Subject scan of unique supplements
for n in 01 02 05 06 07; do
  echo "=== emergency-rule-${n}.md ==="; head -15 "emergency-rule-${n}.md"
done
```

If a supplement covers the rule the user asked about, **the supplement controls**. Cite both: main rule for context, supplement for current operative text.

## Citation format

- Main rule: `Snohomish County SCLCR 7(b)(9)(a)`
- Main rule: `Snohomish County SCLSPR 98.16(e)`
- Emergency supplement: `Snohomish County SCLCR 30 (Emergency Rule 02, eff. 8/13/2025)`

## Caveats

- **Duplicates** (see above) — only 5 of the 9 emergency files contain unique content.
- **One known body-text defect:** a phone number "(425) 388-3587" in SCLCR 7(b)(9)(a) renders in markdown as "(425) 3883587" (hyphen lost at line-break). If the user needs to dial a Snohomish court phone number from a rule, double-check digits.
- **One known structure defect:** at one location a "(iii)" subsection marker is concatenated onto the end of "(ii)" rather than on its own line — content intact, just visually flattened. Around the "Working Copies" / "Unified Family Court" dependency rules.
- Standard machine-conversion artifacts (TOC noise, page footers inline) appear at the top of `local-rules.md`.
