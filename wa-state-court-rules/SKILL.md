---
name: wa-court-rules
description: Use when the user asks about, cites, quotes, or compares a Washington State court rule — any rule under CR, CrR, GR, ER, RPC, CRLJ, CrRLJ, RALJ, ARLJ, RAP — or a U.S. District Court for the Western District of Washington (WAWD) Local Civil Rule. Triggers on any rule abbreviation from those sets, on phrases like "civil rule X," "criminal rule X," "evidence rule X," "appellate rule X," "rule of professional conduct," "general rule," or court-of-limited-jurisdiction questions. Do NOT use for county/district/municipal local rules (those live in the sibling corpora `wa-county-superior-court-rules/`, `wa-district-court-rules/`, and `wa-municipal-court-rules/`), the RCW (sibling skills `wa-rcw-1-50/` and `wa-rcw-51-100/`), the WAC (sibling `wa-administrative-code/`), or rules of other federal districts.
---

# Washington State + WAWD Court Rules

This skill answers questions from a curated, on-disk markdown corpus of:
- **Washington State** court rules (Supreme Court promulgated).
- **U.S. District Court, Western District of Washington (WAWD)** Local Civil Rules.

The markdown files in this directory ARE the authoritative source for this skill. Cite directly from them. This is a snapshot dated 2026-05-20; if currency could matter for a filing-critical question, recommend the user reverify against the official publishing court.

This is the router. **This is the only SKILL.md in the bundle.** Each rule set has a `README.md` (not a SKILL.md) — these aren't separately registered skills; they're per-rule-set playbooks this router instructs you to read. For any rule-set-specific question, read that rule set's `README.md` first — it documents the rules covered, the fidelity assessment, citation conventions, and any per-rule caveats.

## Glossary of rule-set abbreviations

The rule-set abbreviations (CR, CrR, GR, …) are what the rules call themselves — lawyers cite them verbatim, so the abbreviations appear in every citation, heading, and grep example below. The directories are named in plain English so you can see at a glance what's in them.

| Abbrev | Stands for                                                       | What it governs (one line)                                                |
|--------|------------------------------------------------------------------|---------------------------------------------------------------------------|
| CR     | **C**ivil **R**ules (Superior Court)                             | Civil procedure in state Superior Court — pleadings, motions, discovery, trial. |
| CrR    | **Cr**iminal **R**ules (Superior Court)                          | Criminal procedure in state Superior Court — arraignment, pleas, trial, sentencing. |
| GR     | **G**eneral **R**ules                                            | Court administration applying to all WA courts — recordings, conduct, accommodations. |
| ER     | Rules of **E**vidence                                            | What evidence is admissible — relevance, hearsay, privilege, witnesses, opinions. |
| RPC    | **R**ules of **P**rofessional **C**onduct                        | Lawyer ethics — competence, confidentiality, conflicts, advertising.      |
| CRLJ   | **C**ivil **R**ules for Courts of **L**imited **J**urisdiction   | Civil procedure in **district / municipal** courts (not Superior).        |
| CrRLJ  | **Cr**iminal **R**ules for Courts of **L**imited **J**urisdiction| Criminal procedure in district / municipal courts.                        |
| RALJ   | **R**ules for **A**ppeal from courts of **L**imited **J**urisdiction | Appealing a district/municipal decision **up to** Superior Court.   |
| ARLJ   | **A**dministrative **R**ules for courts of **L**imited **J**urisdiction | Court administration in district / municipal courts.                |
| RAP    | **R**ules of **A**ppellate **P**rocedure                         | Appealing Superior Court decisions to the Court of Appeals or Supreme Court. |
| WAWD   | **W**estern District of **W**ashington (federal)                 | The federal trial court for western WA — Seattle/Tacoma seats. **Federal**, not state. |

"Courts of Limited Jurisdiction" = district courts (county-level small-claims/misdemeanor) and municipal courts (city-level traffic/misdemeanor). "Superior Court" = state trial court of general jurisdiction (felonies, big civil, family law).

## Routing

| Rule set | Read first                                                  | Court level                                  | Rules |
|----------|-------------------------------------------------------------|----------------------------------------------|-------|
| **CR**   | `superior-court-civil-rules/README.md`                      | State Superior Court (civil)                 | 96    |
| **CrR**  | `superior-court-criminal-rules/README.md`                   | State Superior Court (criminal)              | 65    |
| **GR**   | `general-rules/README.md`                                   | All Washington courts (general)              | 58    |
| **ER**   | `rules-of-evidence/README.md`                               | All Washington courts (evidence)             | 67    |
| **RPC**  | `rules-of-professional-conduct/README.md`                   | All WA-licensed lawyers                      | 67    |
| **CRLJ** | `civil-rules-limited-jurisdiction/README.md`                | State District / Municipal (civil)           | 82    |
| **CrRLJ**| `criminal-rules-limited-jurisdiction/README.md`             | State District / Municipal (criminal)        | 76    |
| **RALJ** | `appeals-from-limited-jurisdiction/README.md`               | Superior Court (appellate role)              | 45    |
| **ARLJ** | `administrative-rules-limited-jurisdiction/README.md`       | State District / Municipal (administrative)  | 16    |
| **RAP**  | `rules-of-appellate-procedure/README.md`                    | State Court of Appeals / Supreme Court       | 180   |
| **WAWD** | `wawd-federal-local-civil-rules/README.md`                  | **Federal** — U.S. District Court W.D. Wash. | bundled |

**Routing rule:** when the user names a rule abbreviation, go to that rule set's `README.md` first. The per-set README documents the citation convention, fidelity verdict, and any caveats — read it before quoting.

**Court level matters.** CR ≠ CRLJ. CrR ≠ CrRLJ. WAWD LCR ≠ state CR ≠ King County LCR. If the user is vague about which court, ask before answering — applying the wrong rule set to a case is a substantive error.

## Directory layout

```
wa-state-court-rules/                                 ← this is the skill root
├── SKILL.md                                          ← this file (the only SKILL.md in the bundle)
├── superior-court-civil-rules/
│   ├── README.md                                     (rule-set playbook)
│   └── rules.md                                      (96 CR rules)
├── superior-court-criminal-rules/                    (same shape — 65 CrR rules)
├── general-rules/                                    (same shape — 58 GR rules)
├── rules-of-evidence/                                (same shape — 67 ER rules)
├── rules-of-professional-conduct/                    (same shape — 67 RPC rules)
├── civil-rules-limited-jurisdiction/                 (same shape — 82 CRLJ rules)
├── criminal-rules-limited-jurisdiction/              (same shape — 76 CrRLJ rules)
├── appeals-from-limited-jurisdiction/                (same shape — 45 RALJ rules)
├── administrative-rules-limited-jurisdiction/        (same shape — 16 ARLJ rules)
├── rules-of-appellate-procedure/                     (same shape — 180 RAP rules + forms)
└── wawd-federal-local-civil-rules/                   (same shape — WAWD federal local civil rules)
```

Every per-rule-set folder has exactly two files: `README.md` (the playbook) and `rules.md` (the consolidated rule text). All paths in this skill are **relative** to this directory.

## Looking up a rule (single rule set)

Headings inside each `rules.md` use the rule set's own abbreviation as the anchor — that's the citation form lawyers use, so it stays as-is regardless of the parent directory name.

```bash
# CR 56 (summary judgment) — Superior Court civil
grep -n -A 60 -E '^## CR 56\b' superior-court-civil-rules/rules.md

# CrR 3.1 (right to counsel) — Superior Court criminal
grep -n -A 60 -E '^## CrR 3\.1\b' superior-court-criminal-rules/rules.md

# ER 404(b) (other crimes/wrongs)
grep -n -A 30 -E '^## ER 404\b' rules-of-evidence/rules.md

# RAP 2.5 (raising error on appeal)
grep -n -A 60 -E '^## RAP 2\.5\b' rules-of-appellate-procedure/rules.md

# RPC 1.6 (confidentiality)
grep -n -A 60 -E '^## RPC 1\.6\b' rules-of-professional-conduct/rules.md

# WAWD LCR 7 (motions)
grep -n -A 60 -E '^## LCR 7\b' wawd-federal-local-civil-rules/rules.md
```

## Cross-rule-set search

```bash
# Find a term across every rule set (run from this directory)
grep -rni 'summary judgment' --include='rules.md' .

# Find every "rule 56" no matter the prefix
grep -rniE '^## (CR|CrR|CRLJ|CrRLJ|RAP) ?56\b' --include='rules.md' .

# Anywhere the WAC or RCW is cross-referenced
grep -rniE '(RCW|WAC) [0-9]+\.[0-9]+' --include='rules.md' .
```

## Citation format

Match the convention each rule set uses. The directory name is for human navigation; **citations always use the rule set's own abbreviation** (CR, CrR, ER, RPC, …):

- `CR 56(c)` — Washington Superior Court Civil Rule 56(c)
- `CrR 3.1(b)(2)` — Superior Court Criminal Rule 3.1(b)(2)
- `GR 31(e)` — General Rule 31(e)
- `ER 404(b)` — Rule of Evidence 404(b)
- `RPC 1.6(b)(2)` — Rule of Professional Conduct 1.6(b)(2)
- `CRLJ 56(c)` — Civil Rule for Limited Jurisdiction 56(c)
- `CrRLJ 3.1` — Criminal Rule for Limited Jurisdiction 3.1
- `RALJ 6.3.1` — Rule for Appeal of LJ Decision 6.3.1
- `ARLJ 11` — Administrative Rule for LJ 11
- `RAP 2.5(a)(3)`, `RAP 18.1`, `RAP Form 17` — Rule of Appellate Procedure
- `WAWD LCR 7(d)(3)` — Federal local civil rule, W.D. Wash. (always prefix `WAWD` so the reader doesn't confuse it with state CR or King County LCR)

Always quote rule text verbatim from the relevant `rules.md` and report the file path so the reader can verify.

## Fidelity status of this corpus

A fidelity check was performed per rule set. Every set is at least FAITHFUL WITH MINOR CAVEATS — safe to cite body text from. Per-set caveats live in each rule set's `README.md`.

| Rule set | Verdict                          | Notable caveat                                                                  |
|----------|----------------------------------|---------------------------------------------------------------------------------|
| CR       | FAITHFUL                         | Each rule's centered banner heading survives in body — strip when quoting       |
| CrR      | FAITHFUL WITH MINOR CAVEATS      | CrR 4.2 plea form has space-aligned headers; CrR 3.1 Standards is companion doc |
| GR       | FAITHFUL WITH MINOR CAVEATS      | Multiple [RESCINDED]/[RESERVED] stubs; GR 14 Appendix table is space-aligned    |
| ER       | FAITHFUL                         | ER 803(a)(6)/(8) defer to RCW (not in corpus); centered-caps banners in body    |
| RPC      | FAITHFUL                         | Fundamental Principles placed semantically (not alphabetically) at top of rules.md |
| CRLJ     | FAITHFUL WITH MINOR CAVEATS      | Several [RESERVED] slots; range entries (e.g. 27–37) appear as single combined headings |
| CrRLJ    | FAITHFUL WITH MINOR CAVEATS      | CrRLJ 4.2 DUI sentencing table is text-present but column-degraded              |
| RALJ     | FAITHFUL                         | RALJ 6.3.1 was renumbered from 6.3A in 2002; RALJ 2.7 [RESERVED]                |
| ARLJ     | FAITHFUL                         | ARLJ 1 and ARLJ 7 are rescinded (preserved with notices)                        |
| RAP      | FAITHFUL WITH MINOR CAVEATS      | Form layouts (e.g. Form 17 PRP) ASCII-flattened — layouts not authoritative for filing |
| WAWD     | FAITHFUL WITH MINOR CAVEATS      | Sample LCR 37 pleading form flattened; fee schedule not embedded                |

## Universal notes

- **Snapshot date: 2026-05-20.** If currency matters (e.g. recent amendments), recommend the user verify against the canonical source.
- **County / district / municipal local rules are not in this corpus.** They live in three sibling corpora, each its own skill: `wa-county-superior-court-rules/` (Superior Court local rules — Pierce, King, Kitsap, Snohomish, Whatcom, Mason, Island, Thurston, etc.), `wa-district-court-rules/` (district-court local rules), and `wa-municipal-court-rules/` (municipal-court local rules). State-promulgated CR/CrR/CRLJ/CrRLJ in this corpus set the floor; county/city local rules add the local overlay.
- **RCW (Revised Code of Washington) and WAC (Washington Administrative Code) are not in this corpus.** They are cross-referenced inside many rules; the statutory and regulatory text itself lives in the sibling corpora `wa-rcw-1-50/` (skill `rcw-1-50`, RCW Titles 1–50 plus lettered variants) and `wa-rcw-51-100/` (skill `rcw-51-100`, RCW Titles 51–91 plus lettered variants), and `wa-administrative-code/`.
- **Other federal districts** (E.D. Wash., D. Idaho, D. Oregon) and **Ninth Circuit Rules** are not here. WAWD only.
- **"[Reserved]" and "[Rescinded]" entries are intentional**, not omissions. They keep rule numbering aligned with the official rule set.
- **This corpus is offline.** Do not fetch from the web to answer questions — the markdown is the source of truth for this skill.
