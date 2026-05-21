---
name: wa-yakima-district-court-rules
description: Use when the user asks about, cites, quotes, or compares Yakima County District Court (Washington) local court rules — any LCRLJ / LIRLJ / LCrRLJ / LARLJ / LMAR / LGR rule attached to this court. Do NOT use for Superior Court LOCAL rules (sibling skill: wa-county-superior-court-rules/), municipal-court LOCAL rules (sibling skill: wa-municipal-court-rules/), the statewide CRLJ/IRLJ/CrRLJ/ARLJ/RALJ rules (sibling skill: wa-state-court-rules/), RCW (sibling skills: wa-rcw-1-50/ and wa-rcw-51-100/), or WAC (sibling skill: wa-administrative-code/).
---

# Yakima County District Court — Local Court Rules

**Source:** 22 documents (provenance only — do not refetch). See `rules.md` header for the full list.
**Snapshot date:** 2026-05-20  

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. OCR-derived from scanned-image PDF; isolated character substitutions possible (1/I/l, 0/O, vertical bar `|` for `I`). Substantive rule body has been spot-checked against the source.

## Files

```
yakima/
├── README.md   ← you are here
└── rules.md    ← consolidated district court rules (22 individual rule PDFs joined; no separate base ruleset is published)
```

## Looking up a rule

```bash
grep -n -E '^\s*(LCRLJ|LIRLJ|LCrRLJ|LARLJ) ?[0-9]' rules.md
```

## Citation examples

- `Yakima County District Court LCRLJ {rule number}`

## Caveats

- Multi-file: this court has a base rules document plus 21 supplement(s) (emergency rules / amendments). Supplements may modify or supersede specific rules — read the base first, then each supplement in order.
- Includes Moxee and Union Gap Municipal Courts.
- Yakima publishes individual rules as separate PDFs via the county's CivicEngage DocumentCenter. The slugs in the URLs sometimes contain typos (e.g., `L-RALJ-62` is actually `L-ARLJ 6.2`). 6 of the 22 source PDFs are scanned images and have been OCR'd — these are the ones with bare numeric-only filenames and very short text bodies; rule bodies have been verified against the originals.
