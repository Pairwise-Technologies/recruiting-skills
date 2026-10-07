# AGENTS.md

Skills live at `skills/<skill-name>/SKILL.md`. One folder per skill, one `SKILL.md` per folder. Do not create `.cursor/skills` or `.claude/skills` duplicates. Do not add plugin packaging.

Each `SKILL.md` starts with YAML frontmatter:

```yaml
---
name: <skill-name>        # must match the folder name
description: "<one line: what it does and when to use it>"
---
```

Before adding a skill:

- Pass every row in `docs/QUALITY_BAR.md`
- Cite provenance (operator-vetted procedure or named reference fork)
- Prefer one skill per PR

Hard rules: augment recruiters only; never hire or screen "for you"; scores/ranks are assistive drafts; never auto-send outreach; synthetic examples only (no real PII, UUIDs, or live profile URLs); no em-dashes; keep playbooks portable (LinkedIn / generic ATS), not locked to one product.
