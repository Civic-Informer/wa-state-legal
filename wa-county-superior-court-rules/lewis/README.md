---
name: wa-lewis-county-local-rules
description: Use when the user asks about Lewis County (Washington) Superior Court local rules — the Chehalis-seated court. Lewis uses bare LCR / LCrR / LAR / LMAR / LSPR (no county prefix). Triggers on "Lewis County" + any local-rule citation, motion-day question, or family-law / arbitration procedural question. **CAUTION:** Lewis's published rules are still the 2019 effective version. A 2026 proposed revision is in public comment but has not taken effect — flag the staleness on every cite.
---

# Lewis County Superior Court — Local Court Rules

**Effective date of this snapshot:** September 1, 2019. (Lewis has not republished its consolidated local rules since 2019. A 2026 revision is currently open for public comment.)

**Fidelity verdict:** FAITHFUL WITH MINOR CAVEATS — but **temporally stale**. The conversion is clean; the source itself is six years old. Treat every Lewis citation with a "verify against current practice" note.

## Files

```
lewis/
├── README.md       ← you are here
└── local-rules.md  ← consolidated rule body (2019 snapshot)
```

## Rule sets covered

| Abbrev | Rule set |
|--------|----------|
| LAR    | Local Administrative Rules |
| LCR    | Local Civil Rules |
| LMAR   | Local Mandatory Arbitration Rules |
| LSPR   | Local Special Proceedings Rules |

Citations are bare — no Lewis-specific prefix.

## Looking up a rule

```bash
# LCR 7 (motions)
grep -n -A 60 -E '^\s*LCR ?7\b' local-rules.md

# LMAR (arbitration)
grep -niE '^\s*LMAR ?[0-9.]+' local-rules.md
```

## Citation format

- `Lewis County LCR 7(b) (eff. Sept. 1, 2019)`
- Always include the effective-date qualifier when citing Lewis — the 2019 snapshot may not reflect current practice.

## Caveats

- **2019 SNAPSHOT.** This is the latest officially published Lewis County ruleset, but it is six years old. A 2026 revision is in public comment (through approximately June 10, 2026) but is not yet effective. Always flag staleness; for active litigation, the user should verify with the Lewis County Clerk before citing.
- **No state-rule text.** State CR / CrR / MAR are referenced but not included.
