# recruiting-skills

Agent Skills for recruiting operators, from [Pairwise](https://pairwise.ai).

These skills augment recruiters. They do not hire, reject, or screen "for you", and they do not power Pairwise production scoring. Anything that looks like a score, rank, or flag is an assistive draft for human review. Outreach is drafted for a human to send, never auto-sent.

## Layout

```
skills/<skill-name>/SKILL.md
```

Each skill is one folder with one `SKILL.md`: YAML frontmatter (`name`, `description`) followed by a markdown body. The same tree works in Cursor and Claude Agent Skills environments. Point your agent at `skills/`, or copy the skill folders you want into your own skills directory.

## Skills

**Screening playbooks**

- [`domain-fit-over-score`](skills/domain-fit-over-score/SKILL.md): flag mid/low assistive scores when title + company signal strong domain fit, for human dig-deeper
- [`hard-screens-interviewable`](skills/hard-screens-interviewable/SKILL.md): turn must-haves into interviewable questions with probe depth
- [`ideal-anti-persona`](skills/ideal-anti-persona/SKILL.md): build ideal and anti-persona cards from likes and shipped profiles, not the JD alone
- [`sourcing-plays`](skills/sourcing-plays/SKILL.md): near-miss pairs, empty-filter vs empty-pool, employer/problem search, lab-to-grad
- [`draft-for-human-send`](skills/draft-for-human-send/SKILL.md): outreach drafts for human review and send only

**Read-only Pairwise MCP kit**

- [`mcp-session-whoami`](skills/mcp-session-whoami/SKILL.md): confirm session and read scope
- [`mcp-job-discovery`](skills/mcp-job-discovery/SKILL.md): dashboards and service requests
- [`mcp-funnel-read`](skills/mcp-funnel-read/SKILL.md): stage summary, one stage, one application
- [`mcp-interviews-read`](skills/mcp-interviews-read/SKILL.md): interview inventory and transcript (permission-gated)

The MCP kit is read-only, forever. It does not return resume PDF text; never invent resume claims. All examples in this repo are synthetic.

## Docs

- [`docs/MCP_KIT.md`](docs/MCP_KIT.md): MCP kit scope, tools, and hard limits
- [`docs/LOOPS_AND_METRICS.md`](docs/LOOPS_AND_METRICS.md): human-in-the-loop loops each skill feeds
- [`docs/QUALITY_BAR.md`](docs/QUALITY_BAR.md): what a skill must contain to land here

## License

[MIT](LICENSE)
