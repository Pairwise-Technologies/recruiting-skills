---
name: mcp-funnel-read
description: "Pairwise MCP read-only funnel: summary then list stage then one application; no resume PDF invent."
---

# mcp-funnel-read (read-only)

**When to use:** After `mcp-session-whoami` + `mcp-job-discovery`. You need pipeline context for human review (including when keyword screens miss specialized eng). Not for automated scoring or stage moves.

## Purpose

**Read-only** funnel walk: stage counts → one stage's candidates → one application detail. Feeds human review and playbooks such as `domain-fit-over-score`. Completing this recipe **without inventing resume/PDF claims** is the Loop 6 success condition.

## Inputs

- Job / pipeline identifier the caller can already see (placeholder UUID in public examples)
- Target stage name for Level 2
- Optional query/include filters for `list_pipeline_candidates`

## Outputs

- Stage count summary (Level 1)
- Paged candidate list for one stage (Level 2)
- One application detail card (Level 3); **no resume PDF body** via MCP
- Assistive notes for human review only (no hire/reject decisions)

## Procedure

1. **Level 1:** Call `get_pipeline_summary` for per-stage counts.
2. **Level 2:** Call `list_pipeline_candidates` for **one** stage, with pagination and any query/include filters you need. Do not pull every stage in one blind dump when you only need one stage for the task.
3. **Level 3:** Call `get_pipeline_application` for one application detail the human flagged.
4. If resume body is required: **open the PDF in the Pairwise UI**. MCP does not return resume PDF body text today.
5. LinkedIn supplement only if that link is already on the application. Never invent resume claims from title/company alone.
6. Write assistive notes for the human (e.g. handoff into domain-fit-over-score). Stop. No claim, share, stage-move, notes mutate, or send via MCP.

## Worked synthetic example

**Job placeholder:** `job_synth_001` (Sensor Characterization Engineer)  
**Level 1 (synthetic counts):** Applied 42 · Screen 11 · Interview 3 · Offer 0  

**Level 2 (Applied, page 1, synthetic rows):**

| Fake name | Title | Company | Notes for human |
|-----------|-------|---------|-----------------|
| Alex Rivera | Test Engineer | Northlake Sensing Labs | Domain-fit flag candidate; open PDF in UI |
| Jordan Lee | Characterization Engineer | Generic SaaS Co | Title match only; verify modality |

**Level 3:** `get_pipeline_application` on Alex's placeholder application id `app_synth_1001`. Card shows title/company/location and application fields. **No PDF text in MCP response.**  

**Operator action:** Open PDF in Pairwise UI. Draft domain-fit note only from card + PDF actually read.  
**Loop 6 log:** Funnel complete = yes; PDF invent = no; PII invent = no.

## Failure modes / edge cases

- **PDF invent:** Filling "resume says X" when MCP returned no PDF body. Failure for Loop 6.
- **Skipped levels:** Jumping to one application without summary/list context. Incomplete session.
- **Write drift:** Trying to stage-move after reading. Forbidden; use product UI.
- **Real IDs in public copy:** Pasting live UUIDs into examples. Use `job_synth_*` / `app_synth_*`.
- **Multi-stage firehose:** Pulling all stages when the question is one stage. Prefer one-stage list.

## Forever don'ts

- Read-only only: no claim, share, stage-move, notes, or send.
- No resume PDF body text via MCP; never invent resume claims.
- No real job/application UUIDs or PII in public examples.
- Do not treat outputs as Pairwise production scores or hire/reject decisions.
- Do not imply agents screen for you.

## Measure this loop

**Loop 6 - MCP read funnel complete** (completion gate).

- Primary: % of kit sessions that finish summary → list → application without PII invent / PDF invent.
- Sample floor: ~10 kit sessions before tightening this file's failure modes.
- Write-back: invent patterns → update steps and forever-don'ts here and in `docs/MCP_KIT.md` (human-approved).
- See `docs/LOOPS_AND_METRICS.md`.
