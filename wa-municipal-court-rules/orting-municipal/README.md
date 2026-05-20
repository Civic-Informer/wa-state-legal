---
name: wa-orting-municipal-local-rules
description: Use when the user asks about, cites, quotes, or compares Orting Municipal Court local court rules including emergency-rule supplements. Triggers on OMCLR / OMCLCrRLJ / OMCLIR citations attached to Orting. Do NOT use for other WA municipal courts, state-level rules, Superior Court local rules, RCW, or WAC.
---

# Orting Municipal Court Local Court Rules

**Source:** https://www.courts.wa.gov/court_rules/?fa=court_rules.localmunbycrt&lmun=s27&lcrt=Orting  
**Snapshot date:** 2026-05-20

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS. All nine Orting PDFs are image-only scans; the consolidated text comes from OCR and contains visible recognition noise (e.g. 'dit' for '1.1', 'pe' for '1.3', 'hooked' for 'booked', minor punctuation drift). Body structure, rule numbering, and dates are preserved.

## Files

```
orting-municipal/
├── README.md   ← you are here
└── rules.md    ← base rules + 8 emergency rule supplements
```

## Emergency rules — read carefully

This court's `rules.md` is a stack: base rules followed by 8 emergency rule supplements in chronological order (ER01 first, ER08 last). **Supplement(s) override or supplement the base** — when answering a question, check whether a later ER addresses the same rule before relying on the base text.

## Looking up a rule

```bash
# Find the rule in the base section
grep -n -A 60 -E 'OMCLR ?[0-9]' rules.md
# See whether any ER touches the same rule
grep -niE 'emergency.*rule|ER0[0-9]|OMCLR ?30' rules.md
```

## Citation format

- Base rule: `Orting Municipal Court OMCLR 1.1`
- Emergency rule: `Orting Municipal Court Rule 2.0 (Emergency Rule 04, filed 2025-04-03) or Orting Municipal Court OMCLR 2.1 (Emergency Rule 08, filed 2026-03-31)`

## Caveats

- All Orting PDFs are scanned (image-only) and were OCR'd before consolidation; expect OCR noise (e.g. 'dit' for '1.1', 'pe' for '1.3', 'hooked' for 'booked'). ER01–ER04 are single-page bail-schedule (Rule 2.0) amendments. ER05 is a full restatement adopted effective July 7, 2025 that supersedes all prior local rules and ERs; ER06, ER07, ER08 are subsequent revisions of that same restatement.
- ER05–ER08 each carry the same `(Adopted effective July 7, 2025)` trailer on every rule; ER05 is the original adoption and ER06/ER07/ER08 are subsequent re-issues with edits. When citing the operative current text, prefer ER08.
- ER01 through ER04 only restate Rule 2.0 (Release of Accused / Bail Schedule); they were each superseded by ER05 (the full restatement) and are retained for historical reference.
