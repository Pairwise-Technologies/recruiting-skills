# MCP kit - read-only Pairwise MCP companion

**When to use:** You already have Pairwise product visibility and want an optional **read-only** MCP companion beside the screening playbooks. Not required to use the playbooks.

## Purpose

Optional **read-only** Pairwise MCP kit for operators (`mcp:read` or equivalent). **Not** the Pairwise product. **Does not** power Pairwise production scoring. Every skill in this package is read-only.

Skills augment recruiters. They do not hire, reject, or screen for you. Score/rank-looking outputs from downstream playbooks remain assistive drafts for human review.

## Auth / scope

- OAuth with **mcp:read only** (or equivalent read scope).
- Tools only return what the authenticated caller can already see.
- This kit does not document write, claim, share, stage-move, notes, or send.

## Guest packs

Guest pipeline packs are **web URLs**, not MCP tools. Open them in the Pairwise UI. There is no "guest pack" MCP tool.

## Hard limits

- **No resume PDF body text** via MCP. Open the PDF in the Pairwise UI.
- Supplement from LinkedIn only when that link is already on the application.
- **Never invent resume claims.**
- Score- or rank-looking outputs are drafts for a human recruiter, not Pairwise-approved decisions.
- Examples are **synthetic** (fake titles, fake names, placeholder IDs).

## Tools safe to document (read-only)

| Tool | Use |
|------|-----|
| `whoami` | Session / scopes check |
| `get_dashboards` | Active jobs + stage counts |
| `list_service_requests` / `get_service_request` | Job list + one job (title, guidance, locations) |
| `get_pipeline_summary` | Per-stage counts (funnel Level 1) |
| `list_pipeline_candidates` | One stage, pagination, query/include filters (Level 2) |
| `get_pipeline_application` | One application detail (Level 3) |
| `get_job_interviews` / `get_interview_transcript` | Interview inventory + transcript (permission-gated) |
| `get_notifications` | Caller's notification feed |

## Skills and suggested order

1. [`mcp-session-whoami`](../skills/mcp-session-whoami/SKILL.md) - confirm read scope and visibility
2. [`mcp-job-discovery`](../skills/mcp-job-discovery/SKILL.md) - orient on active jobs
3. [`mcp-funnel-read`](../skills/mcp-funnel-read/SKILL.md) - `get_pipeline_summary` → `list_pipeline_candidates` (one stage) → `get_pipeline_application`, without inventing PDF/resume claims
4. [`mcp-interviews-read`](../skills/mcp-interviews-read/SKILL.md) - only when interview inventory/transcript is needed and permitted
5. Hand context into screening playbooks (`domain-fit-over-score`, etc.) for human review drafts

## Forever don'ts

- Do not document write/mutate: claim, share, stage move, notes, email/LinkedIn send, labeling.
- Do not dump PII; no real UUIDs, guest pack URLs, or ATS deep links in examples.
- Do not invent resume PDF contents or experience claims.
- Do not imply this kit powers production scoring or agents that hire/screen for you.

## Measure this loop

**Loop 6 - MCP read funnel complete** (see `LOOPS_AND_METRICS.md`): % of kit sessions that finish the funnel recipe without PII invent / PDF invent.
