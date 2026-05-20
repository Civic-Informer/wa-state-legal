---
name: wa-king-county-local-rules
description: Use when the user asks about King County (Washington) Superior Court local rules — the Seattle / Kent-seated court. Triggers on any "King" + local rule abbreviation (LGR, LCR, LCAR, LGALR, LCrR, LMPR, LJuCR, LRALJ, LFLR). King uses the bare LCR / LFLR / LGR / etc. family — no county prefix. The single consolidated rule document covers all sections and is current through September 1, 2025 amendments.
---

# King County Superior Court — Local Court Rules

**Effective date of this snapshot:** Effective September 1, 2025.

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. Body text, subsection lettering, all-caps notice blocks, dollar figures, citation references, and amendment markers are preserved verbatim against the source PDF. Cite directly from `local-rules.md`. Caveats below are about running-footer noise and TOC blobs — see Caveats.

## Files

```
king/
├── README.md         ← you are here
└── local-rules.md    ← the full 2025 King County Superior Court Local Rules, all sections
```

This single file contains all of King's local rules — LGR, LCR, LCAR, LGALR, LCrR, LMPR, LJuCR, LRALJ, and LFLR. No per-rule splits in this skill bundle. (Per-rule HTML scrapes exist outside this bundle but were excluded because they trail the consolidated document on amendments and have CMS-markup noise.)

## Rule sets covered

| Abbreviation | Rule set                                                                  |
|--------------|---------------------------------------------------------------------------|
| LGR          | Local General Rules                                                       |
| LCR          | Local Civil Rules                                                         |
| LCAR         | Local Civil Arbitration Rules                                             |
| LGALR        | Local Guardian Ad Litem Rules                                             |
| LCrR         | Local Criminal Rules                                                      |
| LMPR         | Local Mental Proceedings Rules                                            |
| LJuCR        | Local Juvenile Court Rules                                                |
| LRALJ        | Local Rules for Appeal of Decisions of Courts of Limited Jurisdiction     |
| LFLR         | Local Family Law Rules                                                    |

King uses the **bare abbreviations** (LCR, LFLR, etc.) — no county prefix.

## Looking up a rule

```bash
# King LCR 7 (motions)
grep -n -A 80 -E '^\s*\*?\*?LCR 7\b' local-rules.md

# King LCR 7(b)(4)(B) — Scheduling Oral Argument on CR 56 Motions
grep -n -B 2 -A 6 'CR 56 Motions' local-rules.md

# King LFLR 10 (financial provisions)
grep -n -A 100 -E '^\s*\*?\*?LFLR 10\b' local-rules.md

# King LGR 14 (hyperlinks)
grep -n -A 15 -E '^\s*\*?\*?LGR 14' local-rules.md

# Section-wide scan of LFLR
grep -niE '^\s*\*?\*?LFLR ?[0-9]+' local-rules.md
```

## Citation format

- `King County LCR 7(b)(4)(B)`
- `King County LFLR 10(b)(3)`
- `King County LCrR 3.1`
- `King County LGR 29`

## Caveats

- **Running footers interleave with rule text.** The document's footer ("Local Rules of the Superior Court for King County · Effective September 1, 2025 · Page N") and image placeholders (`==> picture [W x H] intentionally omitted <==`) appear mid-paragraph roughly every 50-60 markdown lines. **When quoting, strip these out** — they split rule text but are not part of the rule.
- **TOC blobs at top.** Lines ~13-21 and ~133-153 are giant single-line concatenated TOC entries. Never quote rule text from those; jump past them to the actual section headings.
- **Stray double-slash whitespace** can appear mid-list (`the other // // party.` style). Treat as a line-wrap artifact and reflow when quoting.
- **[Rescinded] / [Reserved] entries** are intentionally short. Don't expect body text for those rules.
