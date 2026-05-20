---
name: wac-167-drug-abuse-prevention-office
description: Use when looking up Title 167 WAC (DRUG ABUSE PREVENTION OFFICE). NOTE: this title has no active chapters in the 2025 archive — sections were either repealed or recodified elsewhere. Use to confirm a section is no longer in this title.
---

# Title 167 WAC — DRUG ABUSE PREVENTION OFFICE

**Effective date of this snapshot:** 2026-05-20.

**Fidelity verdict:** N/A — NO ACTIVE CHAPTERS. This title's chapter list is empty in the 2025 archive (all sections repealed or recodified into other titles, or the agency has no current rules).

## What this corpus contains

This is the on-disk archive of this Title from the Washington State Legislature's 2025 WAC Archive. **The 2025 archive contains no active chapters for this Title** — confirmed by both the chapter HTML index (which lists no chapters) and the absence of any combined-chapter PDFs (`combined_chapter_pdfs/WAC_{TITLE}-*_CombinedChapter.pdf`) for this Title. Sections were either repealed, recodified elsewhere, or the agency has no current rules. Consult the official source if you need to confirm a historical citation.


## Files

```
167-drug-abuse-prevention-office/
├── README.md   <- you are here
└── rules.md    <- consolidated chapter section indexes for Title 167 (0 chapters)
```

## Looking up a chapter or section

```bash
# All sections in a specific chapter
grep -n -A 200 '^## WAC 167-' rules.md | less

# A specific chapter
grep -n -A 200 '^## WAC 167-NN ' rules.md  # replace NN with chapter number

# A specific section by number anywhere in the title
grep -n 'WAC 167-NNN-NNN' rules.md  # replace NNN-NNN with section
```

## Citation format

- Chapter: `chapter 167-NN WAC` or `WAC 167-NN`
- Section: `WAC 167-NN-NNN`

## Caveats

- **No active chapters.** Confirmed by both the chapter HTML index and the absence of combined-chapter PDFs in the 2025 archive.
- The `rules.md` file is a stub recording this fact for future grep/audit.
- Snapshot effective date: 2026-05-20. The WAC is amended continuously; check the official source if currency matters.
- This corpus is offline-only. Never refetch from the web.

