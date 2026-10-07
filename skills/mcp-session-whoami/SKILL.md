---
name: mcp-session-whoami
description: "Pairwise MCP read-only whoami session and scopes check before other funnel tools."
---

# mcp-session-whoami (read-only)

**When to use:** Before any pipeline, job, or interview read in this kit. Confirm the session is authenticated with read scope and that you know what the caller can already see.

## Purpose

**Read-only** session / scopes check via `whoami`. Establishes go/no-go for the rest of the MCP kit. Does not grant hire/screen authority. Does not document write scopes.

## Inputs

- Authenticated Pairwise MCP session (operator-connected with **mcp:read** or equivalent)

## Outputs

- Caller identity / scope summary from `whoami` (as returned; do not invent fields)
- Go/no-go for further read-only kit skills
- Short note of visible-job posture (only what whoami / product already exposes)

## Procedure

1. Call `whoami`.
2. Confirm read scope is present. If a workflow seems to need write scopes, **stop**: this kit never documents writes (claim, share, stage-move, notes, send).
3. Note which visibility the session already has. Do not request broader access from inside a skill body.
4. If go: continue to `mcp-job-discovery` or `mcp-funnel-read`. If no-go: fix auth in product/settings with the human operator; do not scrape tokens or bypass OAuth.
5. Keep public logs/examples free of real account identifiers (synthetic only).

## Worked synthetic example

**Call:** `whoami`  
**Synthetic response shape (fields illustrative, not a live dump):**

- account: `recruiter@example-operator.test` (fake)
- scopes: `mcp:read`
- note: can see jobs already visible in product for this caller

**Decision:** Go for read-only kit. Proceed to job-discovery.  
**Anti-pattern:** "Scopes include write; I will claim and share from the agent." Forbidden in this kit.

## Failure modes / edge cases

- **Missing auth:** whoami fails. Fix connection; do not invent a session.
- **Write temptation:** Operator asks to stage-move via MCP. Refuse; point to product UI and forever-don'ts.
- **PII in examples:** Pasting real emails from whoami into the public skill file. Use fakes.
- **Skipping whoami:** Jumping straight to funnel-read and discovering empty visibility late. Run whoami first.

## Forever don'ts

- Read-only only: do not request or document write scopes in this kit.
- Do not dump full PII or internal routing from session payloads into public logs/examples.
- No real account identifiers in public examples (synthetic only).
- Do not imply whoami grants hire/screen authority.
- Do not claim this powers Pairwise production scoring.

## Measure this loop

**Loop 6 - MCP read funnel complete** (prerequisite step).

- Contributes to: % of kit sessions that finish funnel recipe without PII invent / PDF invent.
- A session that skips whoami and later invents visibility counts against the metric.
- See `docs/LOOPS_AND_METRICS.md`.
