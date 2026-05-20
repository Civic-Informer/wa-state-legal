# Washington Revised Code (RCW)

This directory holds an offline snapshot of every Title of the Revised Code of Washington — 100 Titles spanning numeric Titles 1-91 and all 16 lettered Titles (9A, 23B, 28A/B/C, 29A/B, 30A/B, 35A, 50A/B, 62A, 70A, 71A, 79A) — together with a Claude Code skill that navigates and cites them. This `wa-rcw/` directory contains the consolidated markdown statute text plus per-Title README playbooks and a root router; the body text was produced by `pdftotext -layout` over the Washington State Legislature's official Combined Title PDFs (the canonical full-text source) and has been spot-checked against the source for fidelity. The original source PDFs and HTML archive are not redistributed with this skill bundle; provenance URLs for human re-derivation appear in `SKILL.md`.

To use it, copy or symlink `wa-rcw/` into `~/.claude/skills/rcw/` (or rename to taste). Claude picks the skill up automatically whenever a user cites or paraphrases Washington statute — `RCW 4.16.080`, `RCW 9A.36.011`, `Chapter 62A.9A RCW`, "Washington statute of limitations," "B&O tax," "wrongful death in Washington," etc. On a match, Claude reads the root `SKILL.md`, routes to the relevant Title's `README.md`, and answers from the on-disk markdown. The skill is offline-only — it does not (and should not) fetch from the web; the local files are authoritative and are dated 2026-05-20.

**Scope:**

- **In:** all 100 published RCW Titles (numeric 1-91 + 16 lettered) — civil procedure, evidence, crimes, criminal procedure, corrections, public records, courts, family law, real property, commerce, UCC, common schools, higher ed, financial institutions, public health, environment, water rights, taxes, etc.
- **In:** 2,764 chapters of full statute body text (not just TOCs) — every section, subsection, definition, history note, and cross-reference the Legislature publishes in its 2025 "Complete Title" PDFs.
- **Out:** WAC implementing regulations — sibling skill at `../wa-administrative-code/`.
- **Out:** Washington state-wide court rules (Civil Rules, Rules of Professional Conduct, appellate rules) — sibling skill at `../wa-state-court-rules/`.
- **Out:** Washington county Superior Court local rules — sibling skill at `../wa-county-superior-court-rules/`.
- **Out:** Washington district court local rules — sibling skill at `../wa-district-court-rules/`.
- **Out:** Washington municipal court local rules — sibling skill at `../wa-municipal-court-rules/`.
- **Out:** Federal statutes (USC), federal regulations (CFR), and case law interpreting the RCW.
- **Out:** Title numbers `28`, `29`, `30`, `45`, `56`, `62`, `75` — these are reserved/replaced by lettered variants (28A/B/C, 29A/B, 30A/B) or never assigned by the Legislature.
- **Out:** Pre-2025 historical RCW versions and the underlying session laws (chapter laws) — only the codified 2025 snapshot is archived.
