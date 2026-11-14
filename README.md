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
candidate-ranking
candidate-slate-review
domain-engineering-hardware
hiring-retrospective
interview-transcript-review
role-job-description
role-requirements
```

- **Core skills** (`role-*`, `candidate-*`) are `<subject>-<task>` and role-neutral.
- **Domain skills** (`domain-<field>-<area>`) hold field-specific knowledge a core skill loads when one matches.

## Skills

- [`candidate-assessment`](skills/candidate-assessment/SKILL.md): Read one candidate against a role-requirements profile from any amount of evidence: per-axis reads, an authenticity call, and a verdict with its confidence.
- [`candidate-outreach`](skills/candidate-outreach/SKILL.md): Draft one cold outreach (initial + follow-up) for one candidate, for a human to review and send, or decide not to contact them.
- [`candidate-ranking`](skills/candidate-ranking/SKILL.md): Rank candidates for one role into a short slate for the person who decides: engagement gates first, then fit, track record, vetting and location in strict order, each rank with a reason, a risk and a confidence.
- [`candidate-slate-review`](skills/candidate-slate-review/SKILL.md): Review a slate already presented when anything changes, candidate side first: keep, watch or pull submission for each person, with why-fit notes and short updates drafted for a human to send.
- [`domain-engineering-hardware`](skills/domain-engineering-hardware/SKILL.md): Field knowledge for hardware engineering searches: transfer rules, ownership cues and inflation signals. Loads with the core skills.
- [`hiring-retrospective`](skills/hiring-retrospective/SKILL.md): Blameless retro of a finished or stalled search: requirements against the hire and the interviewed set, interview signal, funnel and timeline, with at most 3 suggestions.
- [`interview-transcript-review`](skills/interview-transcript-review/SKILL.md): Extract the evidence from one screen or interview transcript against a role-requirements profile: what was shown, claimed or never asked, and how the interview was run. No verdict.
- [`role-job-description`](skills/role-job-description/SKILL.md): Write a public job description from a role-requirements profile: the work and outcomes first, a short required list that traces to the profile, and only the sections the inputs support.
- [`role-requirements`](skills/role-requirements/SKILL.md): Break a role into mission, outcomes and a tiered requirements profile, with knockouts and open questions, before reading candidates; update it as confirmed feedback arrives.

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

Copyright (c) 2026 Pairwise. Licensed under [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](LICENSE).

You may use, share and adapt these skills, including at work and for commercial purposes, if you:

- **Credit Pairwise:** `recruiting-skills by Pairwise (https://github.com/Pairwise-Technologies/recruiting-skills), CC BY-SA 4.0`, and say if you changed anything.
- **Share alike:** release adapted versions under CC BY-SA 4.0 (or a compatible license), so they stay open.

Contributions to this repo are accepted under the same license.

**Trademarks:** the license covers the content only. It grants no rights to the Pairwise name or logo. Do not use them to suggest that a copy or adaptation comes from, or is endorsed by, Pairwise.
