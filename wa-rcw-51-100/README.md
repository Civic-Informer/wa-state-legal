# Washington Revised Code (RCW) — Titles 51–91

This directory holds an offline snapshot of the second half of the Revised Code of Washington — 42 Titles spanning numeric Titles 51–91 plus the lettered variants in that range (62A, 70A, 71A, 79A) — together with a Claude Code skill (`rcw-51-100`) that navigates and cites them. The companion first-half corpus (Titles 1–50 plus 9A/23B/28A-C/29A-B/30A-B/35A/50A-B) lives in the sibling directory [`../wa-rcw-1-50/`](../wa-rcw-1-50/) as the skill `rcw-1-50`; the split is a packaging convenience driven by directory size, not a substantive division of Washington law.

This `wa-rcw-51-100/` directory contains the consolidated markdown statute text plus per-Title README playbooks and a router `SKILL.md`; the body text was produced by `pdftotext -layout` over the Washington State Legislature's official Combined Title PDFs (the canonical full-text source) and has been spot-checked against the source for fidelity. The original source PDFs and HTML archive are not redistributed with this skill bundle; provenance URLs for human re-derivation appear in `SKILL.md`.

To use it, copy or symlink `wa-rcw-51-100/` into `~/.claude/skills/rcw-51-100/` (or rename to taste), and likewise install `../wa-rcw-1-50/` as `rcw-1-50/`. Claude picks each skill up automatically whenever a user cites or paraphrases Washington statute — `RCW 51.32.030`, `RCW 59.18.030`, `RCW 62A.9A-313`, `Chapter 82.04 RCW`, "workers' compensation in Washington," "Washington landlord-tenant act," "UCC Article 9," "B&O tax," "water rights," etc. — routing to this half whenever the relevant Title number is 51–91 (or one of the lettered variants in this range). On a match, Claude reads this directory's `SKILL.md`, routes to the relevant Title's `README.md`, and answers from the on-disk markdown. The skill is offline-only — it does not (and should not) fetch from the web; the local files are authoritative and are dated 2026-05-20.

**Scope:**

- **In:** 42 RCW Titles — numeric Titles 51–91 plus lettered Titles 62A, 70A, 71A, 79A.
- **In:** 891 chapters of full statute body text (not just TOCs) — every section, subsection, definition, history note, and cross-reference the Legislature publishes in its 2025 "Complete Title" PDFs for these Titles.
- **Out:** RCW Titles 1–50 and lettered variants 9A / 23B / 28A / 28B / 28C / 29A / 29B / 30A / 30B / 35A / 50A / 50B — sibling skill at [`../wa-rcw-1-50/`](../wa-rcw-1-50/).
- **Out:** WAC implementing regulations — sibling skill at `../wa-administrative-code/`.
- **Out:** Washington state-wide court rules (Civil Rules, Rules of Professional Conduct, appellate rules) — sibling skill at `../wa-state-court-rules/`.
- **Out:** Washington county Superior Court local rules — sibling skill at `../wa-county-superior-court-rules/`.
- **Out:** Washington district court local rules — sibling skill at `../wa-district-court-rules/`.
- **Out:** Washington municipal court local rules — sibling skill at `../wa-municipal-court-rules/`.
- **Out:** Federal statutes (USC), federal regulations (CFR), and case law interpreting the RCW.
- **Out:** Title numbers `56`, `62`, `75` — these are reserved/replaced by lettered variants or successor Titles (Title 56 → 57; Title 62 → 62A; Title 75 → 77) or never reassigned by the Legislature.
- **Out:** Pre-2025 historical RCW versions and the underlying session laws (chapter laws) — only the codified 2025 snapshot is archived.
