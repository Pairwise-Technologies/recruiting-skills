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

Skill names run from least specific to most specific, so a sorted list groups related skills together. The first word is the thing the skill works on; each later word narrows it.

```
candidate-assessment
candidate-outreach
domain-engineering-hardware
domain-engineering-software
role-requirements
```

- **Core skills** (`role-*`, `candidate-*`): `<object>-<task>`. They are role-neutral and work for any job.
- **Domain skills** (`domain-<field>-<area>`): hold the role-specific knowledge a core skill needs for one field, such as typical must-haves, how adjacent experience transfers, and inflation signals. A core skill loads a matching domain skill when one exists and still works without it.
- Keep domain names at two levels. Add a third (`domain-engineering-hardware-sensors`) only when one domain skill grows too large to stay tight.
- Lowercase and hyphens only, at most 64 characters, and the name matches the folder.
- Choose names to last. Renaming a published skill breaks everyone who points at it.

## Hard rules

- Human in the loop: assistive drafts only; never hire/reject/"screen for you"
- Never auto-send outreach, LinkedIn DMs, or email
- Synthetic examples only (no real candidate PII, live profile URLs, pipeline UUIDs, or named-client exemplars)
- No production scoring internals or "how to game" a rank
- No em-dashes

## Docs

- [`docs/QUALITY_BAR.md`](docs/QUALITY_BAR.md): what a skill must contain before it lands here
- [`docs/SOURCES.md`](docs/SOURCES.md): books and concepts the skills draw on

## Adding a skill

1. Write `skills/<name>/SKILL.md` against `docs/QUALITY_BAR.md`
2. Cite provenance: original operator procedure (with how it was vetted) **or** explicit fork/adapt from a named reference
3. Open a PR with one skill (or a tiny related set). Prefer tiny.

## License

[MIT](LICENSE)
