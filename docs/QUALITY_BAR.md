# QUALITY_BAR

A skill in this repo is an **operator-runnable playbook**, not a vibe outline. Someone who has never seen the skill should be able to run it end-to-end from the file alone: when to use it, what to gather, what steps to take, what a good output looks like, what usually goes wrong, and which loop it feeds.

Two packages stay distinct:

1. **Screening playbooks** - recruiting operator skills (assistive drafts for human review).
2. **Read-only Pairwise MCP kit** - optional companion for reading pipeline data the caller can already see.

Skills **augment recruiters**. They do not hire, reject, or screen "for you." Score/rank language is always assistive draft language. MCP stays forever read-only.

## Completeness checklist (every skill)

| Section | Required content |
|---------|------------------|
| Frontmatter | `name` (matches folder) and `description` |
| Title + when to use | 1-2 lines: skill id and the trigger situation |
| Purpose | Why this skill exists; assistive framing explicit |
| Inputs | Concrete artifacts the operator must have |
| Outputs | Concrete artifacts produced (drafts, flags, notes - not hire decisions) |
| Procedure | Numbered, concrete, operator-usable steps |
| Worked synthetic example | One end-to-end example with fake names / placeholder IDs |
| Failure modes / edge cases | What usually breaks or misleads |
| Forever don'ts | Hard bans (see hygiene below) |
| Measure this loop | Named loop + metric(s) from `LOOPS_AND_METRICS.md` |

MCP kit skills additionally:

- Say **read-only** in the title or first purpose line
- Name only tools from the table in `MCP_KIT.md`
- Remind: no resume PDF via MCP; never invent resume claims; guest packs are web URLs

Target length: roughly 60-120 lines. Tight but real.

## Voice and hygiene

- No em-dashes. Use commas, periods, colons, or hyphens.
- Synthetic examples only. No real UUIDs, guest pack URLs, candidate PII, or live LinkedIns.
- No named-client exemplars or experiments.
- No scoring-model internals, fraud thresholds, production KPIs, or "how to raise/game Pairwise score."
- No write/mutate MCP surface.
