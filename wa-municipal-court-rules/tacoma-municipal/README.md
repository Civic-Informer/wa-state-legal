---
name: wa-tacoma-municipal-court-rules
description: Use when asked about Tacoma Municipal Court (TMC) — but note the base TMCLCR rules are not published online; only 2025-2026 emergency rules and the shared Pierce County District Court emergency rules are available in this corpus. The 2026 TMC emergency rule does contain substantive TMCLGR / TMCLCR rule text (scope, photography, presiding judge, eFiling, release of accused, motions, etc.) effective 3/30/26 — use it as the primary Tacoma source, but for any base rule not covered there, the user must contact the court clerk.
---

# Tacoma Municipal Court — Available Local Rules (Emergency Only)

**Effective date of this snapshot:** 2026-05-20.

**Fidelity verdict:** PARTIAL. The base TMCLCR / TMCLGR / TMCLIR rule set is missing because **it is not published online by the City of Tacoma** (see callout below). What *is* captured — the 2026 TMC emergency rule (which carries substantial rule text adopted 3/30/26), the 2026 and 2025 Pierce County District Court emergency rules, and the city's municipal-court landing page — is faithfully transcribed via `pdftotext -layout` (PDFs) and pandoc HTML conversion. Subsection lettering, citation references, and adoption-date stamps survive.

## Base TMCLCR rules are NOT in this corpus

As of 2026-05-20, Tacoma Municipal Court publishes only its **emergency** local rules online. Base TMCLCR is not posted in any form on `tacoma.gov` or `cms.tacoma.gov`. The discovery wave verified this by:

1. Searching the saved index HTML for `TMCLCR`, `TMCR`, `LCR \d`, `CrRLJ \d`, `Local Rule \d` — only emergency-rule hits.
2. Probing obvious base-rule URLs (`cms.tacoma.gov/muni%20court/tmclcr.pdf` and variants) — all soft-404.
3. Probing alternate sub-page URLs (`/court-rules/`, `/local-rules/`, etc.) — all HTTP 404.
4. Cataloguing every `.pdf` and `.docx` link on the index page — none point to a base/general TMCLCR document.

**For base-rule text, the user must request a copy from the court clerk.**

## Files

```
tacoma-municipal/
├── README.md
└── rules.md     ← header + base-rules-missing callout + 3 emergency PDFs + city index page
```

`rules.md` is built by concatenating four source files in this order:

1. **Tacoma Municipal Court — 2026 Emergency Local Rule** — `2026_tmc_emergencylocalrule03.30.26.pdf` (the most substantive Tacoma-specific document; despite the "emergency" label it contains rule text adopted 3/30/26 covering TMCLGR 1.1/16.1/29.1/30.1 and TMCLCR 1.7.1/1.8.1/2.2.1/3.1.1/3.2.1/3.3.1/3.4.1/3.4.2/3.4.3/3.6.1/4.2.1/4.5.1/8.2.1/8.2.2)
2. **Pierce County District Court — 2026 Emergency Local Rule (applies to TMC)** — `2026_pd_emergencylocalrule03.30.26.pdf`
3. **Pierce County District Court — 2025 Emergency Local Rule** — `2025_pd1_emg_local_rule_9-30-25.pdf`
4. **City Municipal Court Index Page (context only)** — `municipal-court-index.html`

## Citation forms

| Prefix     | Domain                                       |
|------------|----------------------------------------------|
| TMCLGR     | Tacoma Municipal Court Local General Rules   |
| TMCLCR     | Tacoma Municipal Court Local Criminal Rules  |
| LARLJ      | Local Administrative Rules for Courts of Limited Jurisdiction (Pierce County District Court emergency rule set) |

Note: Pierce County District Court uses `LARLJ 7` for its standing-committees emergency rule, which sets up the Municipal Court of Tacoma Judicial Committee.

## Looking up a rule

```bash
# Any TMCLGR / TMCLCR rule by number (will only hit if present in the 2026 emergency rule)
grep -n -A 30 -iE 'TMCLGR ?1\.1' rules.md
grep -n -A 30 -iE 'TMCLCR ?3\.2\.1' rules.md

# Pierce County District Court emergency rule
grep -n -A 40 -iE 'LARLJ ?7' rules.md

# Confirm whether a rule citation is in the corpus at all (will return nothing if base-only)
grep -n -iE 'TMCLCR ?[0-9.]+' rules.md
```

## Caveats

- **BASE RULES MISSING.** This is the single most important caveat. If the user asks about a TMCLCR rule that does not appear in the 2026 emergency rule text, **do not invent or paraphrase** — point them to the court clerk. Do not infer base rules from neighboring Pierce County District Court rules; the 2026 TMC emergency rule explicitly states (TMCLGR 1.1(a)) "The other provisions of the Pierce County District Court local rules are not applicable to Tacoma Municipal Court."
- **Emergency vs. base.** Everything in this corpus is labeled "emergency" by the issuing court. The 2026 TMC document is the closest thing to a base-rule snapshot but is still formally an emergency rule.
- **Pierce County District Court rules are included** because they share administration with TMC under the LARLJ 7 standing-committee structure. They are not Tacoma rules.
- **City index page is context only.** It contains court hours, payment info, and forms — not rule text. Don't grep it expecting rule body.
- **Offline-only.** Do not refetch from tacoma.gov or cms.tacoma.gov.
