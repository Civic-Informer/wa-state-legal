---
name: wa-lower-kittitas-district-court-rules
description: Use when the user asks about, cites, quotes, or compares Lower Kittitas County District Court (Washington) local court rules — any LCRLJ / LIRLJ / LCrRLJ / LARLJ / LMAR / LGR rule attached to this court. Do NOT use for Superior Court LOCAL rules (sibling skill: wa-county-superior-court-rules/), municipal-court LOCAL rules (sibling skill: wa-municipal-court-rules/), the statewide CRLJ/IRLJ/CrRLJ/ARLJ/RALJ rules (sibling skill: wa-state-court-rules/), RCW (sibling skills: wa-rcw-1-50/ and wa-rcw-51-100/), or WAC (sibling skill: wa-administrative-code/).
---

# Lower Kittitas County District Court — Local Court Rules

**Source:** 11 documents (provenance only — do not refetch). See `rules.md` header for the full list.
**Snapshot date:** 2026-05-20  

**Fidelity verdict:** PARTIAL. Lower Kittitas does not publish a consolidated base ruleset. Only individual rule PDFs (LCrR 4.5 plus three forms, LCrR 7.2(f), LGR 17(a)(7), LGR 30, LGR 30(b)(4), LIR 3.1, LIR 3.5(f), LIR 6.6(e)) are on the county website. Any rule outside these eight is not in this snapshot.

## Files

```
lower-kittitas/
├── README.md   ← you are here
└── rules.md    ← consolidated district court rules (11 individual rule PDFs joined; no separate base ruleset is published)
```

## Looking up a rule

```bash
grep -n -E '^\s*(LCrR|LGR|LIR) ?[0-9]' rules.md
```

## Citation examples

- `Lower Kittitas County District Court LCrR {rule number}`
- `Lower Kittitas County District Court LGR {rule number}`
- `Lower Kittitas County District Court LIR {rule number}`

## Caveats

- Multi-file: this court has a base rules document plus 10 supplement(s) (emergency rules / amendments). Supplements may modify or supersede specific rules — read the base first, then each supplement in order.
- Lower Kittitas does not publish a consolidated base ruleset. Each rule (LCrR 4.5, LCrR 7.2(f), LGR 17(a)(7), LGR 30, LGR 30(b)(4), LIR 3.1, LIR 3.5(f), LIR 6.6(e)) is its own PDF on the county website. URLs use heavy percent-encoding (`%20`, `%28`, `%29`); preserved verbatim in the source-document filenames on disk.
