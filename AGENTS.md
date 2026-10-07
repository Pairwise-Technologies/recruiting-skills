# AGENTS.md

Skills live at `skills/<skill-name>/SKILL.md`. One folder per skill, one `SKILL.md` per folder. Do not create `.cursor/skills` or `.claude/skills` copies.

Each `SKILL.md` starts with YAML frontmatter:

```yaml
---
name: <skill-name>        # must match the folder name
description: "<one line: what it does and when to use it>"
---
```

When adding or changing a skill:

- Follow the checklist in `docs/QUALITY_BAR.md`.
- Tie it to a loop in `docs/LOOPS_AND_METRICS.md`.
- List it in `README.md` and `docs/INDEX.md`.
- MCP kit skills stay read-only and use only tools in `docs/MCP_KIT.md`.

Hard rules: skills augment recruiters and never hire or screen "for you"; scores and ranks are assistive drafts for human review; outreach is never auto-sent; synthetic examples only (no real PII, UUIDs, or guest pack URLs); no em-dashes.
