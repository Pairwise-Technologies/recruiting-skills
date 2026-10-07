---
name: mcp-job-discovery
description: "Pairwise MCP read-only dashboards and service-request discovery."
---

# mcp-job-discovery (read-only)

**When to use:** After `mcp-session-whoami` succeeds. You need to orient on active jobs and one job's guidance before a funnel or interview read.

## Purpose

**Read-only** discovery of active jobs and service-request detail the caller can already see. Produces human-oriented orientation notes, not a scored shortlist and not an auto-screen.

## Inputs

- Authenticated read-only session (`mcp:read`), confirmed via `mcp-session-whoami`
- Optional filters the product already exposes for dashboards / service requests

## Outputs

- Active jobs + stage counts from `get_dashboards`
- Job list from `list_service_requests`
- One-job detail (title, guidance, locations) from `get_service_request`
- Orientation notes for the human operator (which job to funnel-read next)

## Procedure

1. Call `get_dashboards` for active jobs + stage counts.
2. Call `list_service_requests` for the job list the caller can see.
3. Pick one job the human cares about. Call `get_service_request` for title, guidance, locations.
4. Write a short orientation note: job title, stage heat (from counts), guidance highlights. No invented hiring-team rosters.
5. Remind: guest packs are **web URLs** in the Pairwise UI, not MCP tools.
6. Hand off to `mcp-funnel-read` with the chosen job identifier the caller can already see (placeholder IDs only in public examples).

## Worked synthetic example

**Synthetic dashboard snippet:**

| Job (fake title) | Placeholder id | Stage heat (illustrative) |
|------------------|----------------|---------------------------|
| Sensor Characterization Engineer | `job_synth_001` | Applied high; Interview low |
| Controls Engineer (Mobile) | `job_synth_002` | Applied medium |

**get_service_request (`job_synth_001`) synthetic:** title as above; locations "Bay Area / hybrid"; guidance mentions fixture ownership and metrics reporting.

**Orientation note:** "Start funnel-read on Sensor Characterization (`job_synth_001`). Guidance stresses fixture + metrics; pair later with hard-screens-interviewable. Guest pack if needed: paste URL in UI, not MCP."

## Failure modes / edge cases

- **Empty dashboards:** Caller has no job visibility. Stop; fix access in product. Do not invent jobs.
- **Guest-pack MCP myth:** Searching for a guest-pack tool. There is none; use web URL in UI.
- **Real UUID leakage:** Copying live job IDs into public skill examples. Use `job_synth_*` placeholders.
- **Treating counts as scores:** Stage counts are funnel heat, not candidate quality scores.

## Forever don'ts

- Read-only only: no write, claim, share, or send.
- Do not document or invent guest-pack MCP tools.
- No real job UUIDs, ATS deep links, or hiring-team maps in public examples.
- Do not imply job discovery auto-screens or ranks for hire.
- Do not claim this kit powers Pairwise production scoring.

## Measure this loop

**Loop 6 - MCP read funnel complete** (orientation step).

- Contributes to sessions that can finish summary → list → application without inventing jobs or resume claims.
- Discovery that invents a job id or guest-pack tool counts as a failed hygiene session.
- See `docs/LOOPS_AND_METRICS.md`.
