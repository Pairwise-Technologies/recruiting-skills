# QUALITY_BAR

A skill in this repo is an **operator-runnable playbook**, not a vibe outline. Someone who has never seen the skill should be able to run it end-to-end from the file alone: when to use it, what to gather, what steps to take, what a good output looks like, and what usually goes wrong.

Skills **augment recruiters**. They do not hire, reject, or screen "for you." Score/rank language is always assistive draft language.

## Completeness checklist (every skill)

| Section | Required content |
|---------|------------------|
| Frontmatter | `name` (matches folder, follows the naming convention in `README.md`) and `description` |
| Title + when to use | 1-2 lines: skill id and the trigger situation |
| Purpose | Why this skill exists; assistive framing explicit |
| Inputs | Concrete artifacts the operator must have |
| Outputs | Concrete artifacts produced (drafts, flags, notes - not hire decisions) |
| Procedure | Numbered, concrete, operator-usable steps |
| Worked synthetic example | One end-to-end example with fake names / placeholder IDs |
| Failure modes / edge cases | What usually breaks or misleads |
| Forever don'ts | Hard bans (see hygiene below) |
| Provenance | One short line: operator-vetted (how) **or** adapted from `<named reference>` with what changed |

Target length: roughly 60-120 lines. Tight but real.

## Voice and hygiene

- No em-dashes. Use commas, periods, colons, or hyphens.
- Synthetic examples only. No real UUIDs, candidate PII, or live profile URLs.
- No named-client exemplars.
- No production scoring internals or "how to raise/game" a rank.
- Portable: LinkedIn / generic ATS framing. Do not require a specific product UI or proprietary API.
- Never auto-send outreach.

## Landing bar

Do not land a skill unless:

1. It passes the checklist above, **and**
2. It is either rewritten by a human operator against a real loop, **or** clearly forked/adapted from a named strong reference with attribution.

Bulk AI-generated packs fail this bar by default.
