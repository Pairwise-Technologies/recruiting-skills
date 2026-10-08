# recruiting-skills

Public Agent Skills for recruiting operators.

This repo starts nearly empty on purpose. v0 ships the layout convention and the quality gate only. Skills land one at a time after they are operator-vetted or adapted from a named strong reference (with attribution). Bulk AI packs do not ship here.

Skills **augment** recruiters. They do not hire, reject, or screen "for you." Anything that looks like a score, rank, or flag is an assistive draft for human review. Outreach is drafted for a human to send; never auto-sent.

This repo is **not** locked to any one ATS, recruiting product, or employment model (agency, contract, in-house). Playbooks should work on a LinkedIn / generic ATS hiring pipeline. Platform-specific MCP tooling lives in a separate repo.

## Layout

```
skills/<skill-name>/SKILL.md
```

Each skill is one folder with one `SKILL.md`: YAML frontmatter (`name`, `description`) followed by a markdown body. Same tree works in Cursor and Claude Agent Skills environments. Point your agent at `skills/`, or copy the folders you want into your own skills directory.

Convention inspired by [mattpocock/skills](https://github.com/mattpocock/skills) (layout only).

## Naming

Skill names run from least specific to most specific, so a sorted list groups related skills together. The full rule, which applies to any skill we write, is in [`docs/SKILL_NAMING.md`](docs/SKILL_NAMING.md). In this repo:

```
candidate-assessment
candidate-outreach
domain-engineering-hardware
role-requirements
```

- **Core skills** (`role-*`, `candidate-*`) are `<subject>-<task>` and role-neutral.
- **Domain skills** (`domain-<field>-<area>`) hold field-specific knowledge a core skill loads when one matches.

## Skills

- [`candidate-assessment`](skills/candidate-assessment/SKILL.md): Read one candidate against a role-requirements profile from any amount of evidence: per-axis reads, an authenticity call, and a verdict with its confidence.
- [`candidate-outreach`](skills/candidate-outreach/SKILL.md): Draft one cold outreach (initial + follow-up) for one candidate, for a human to review and send, or decide not to contact them.
- [`role-requirements`](skills/role-requirements/SKILL.md): Break a role into mission, outcomes and a tiered requirements profile, with knockouts and open questions, before reading candidates.

## Hard rules

- Human in the loop: assistive drafts only; never hire/reject/"screen for you"
- Never auto-send outreach, LinkedIn DMs, or email
- Synthetic examples only (no real candidate PII, live profile URLs, pipeline UUIDs, or named-client exemplars)
- No production scoring internals or "how to game" a rank
- No em-dashes

## Docs

- [`docs/QUALITY_BAR.md`](docs/QUALITY_BAR.md): what a skill must contain before it lands here
- [`docs/SKILL_NAMING.md`](docs/SKILL_NAMING.md): how skills are named
- [`docs/SOURCES.md`](docs/SOURCES.md): books and concepts the skills draw on

## Adding a skill

1. Write `skills/<name>/SKILL.md` against `docs/QUALITY_BAR.md`
2. Cite provenance: original operator procedure (with how it was vetted) **or** explicit fork/adapt from a named reference
3. Open a PR with one skill (or a tiny related set). Prefer tiny.

## License

[MIT](LICENSE)
