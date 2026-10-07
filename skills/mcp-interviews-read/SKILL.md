---
name: mcp-interviews-read
description: "Pairwise MCP read-only interviews and transcript when permission-gated scopes allow."
---

# mcp-interviews-read (read-only)

**When to use:** After job orientation (and usually after `mcp-funnel-read`). You need interview inventory or a permission-gated transcript for **human** prep and review. Not for auto-scoring interviews.

## Purpose

**Read-only** interview inventory and transcript access (permission-gated). Augment recruiters and interviewers with what they can already see. Do not auto pass/fail from transcript keywords. Transcript insights that change ideal/anti signals should flow to Loop 3 via human-approved persona patches; inventing quotes is a Loop 6 hygiene failure.

## Inputs

- Job / interview identifiers the caller can already see (placeholder UUIDs in public examples)
- Confirmation that transcript permission is granted for this caller
- Optional: hard-screen question bank to compare against what was actually asked

## Outputs

- Interview inventory from `get_job_interviews`
- Transcript text from `get_interview_transcript` when permitted
- Assistive prep or review notes for human interviewers (drafts only)

## Procedure

1. Call `get_job_interviews` for the job the caller can see. Summarize inventory (counts, statuses) without dumping PII into public notes.
2. If the human needs a transcript and permission is granted, call `get_interview_transcript` for one interview id.
3. If permission is denied: stop transcript read; note "permission-gated, unavailable" for the human. Do not invent quotes.
4. Summarize for human review using only transcript content actually returned. Quote sparingly; prefer structured notes mapped to hard-screens when a bank exists.
5. Do not auto pass/fail. If notes suggest persona drift, propose a Loop 3 patch for human approval.
6. Stop at read/assist. No scheduling writes, notes mutate, or outbound send via MCP.

## Worked synthetic example

**Job placeholder:** `job_synth_001`  
**get_job_interviews (synthetic inventory):** 3 interviews listed; statuses scheduled / completed / completed. Placeholder interview id `int_synth_55`.  

**get_interview_transcript (`int_synth_55`) synthetic excerpt:** Candidate describes a pressure-sensor soak test, names a temperature chamber, admits fixture resonance was undiagnosed.  

**Assistive note for human:** "Completed interview `int_synth_55` (placeholder). Strong on soak/metrics narrative; weak on fixture diagnosis. Compare to hard-screens bank: fixture ownership may still be open. Human judgment only; do not auto-fail."  

**Hygiene:** No real candidate name, email, or live interview id in the public example.

## Failure modes / edge cases

- **Invented quotes:** Writing transcript lines that were not returned. Counts against Loop 6 invent metric.
- **Permission bypass:** Retrying or scraping when transcript is gated. Stop; use product permissions.
- **Auto-score:** Keyword pass/fail on transcript. Forbidden.
- **PII publish:** Pasting live transcripts into public skill copy. Synthetic excerpts only.
- **Skipping inventory:** Fetching a guessed interview id without get_job_interviews. Prefer inventory first.

## Forever don'ts

- Read-only only: no scheduling writes, notes mutate, or outbound send.
- Never invent transcript content or resume claims.
- No real candidate PII or live interview IDs in public examples.
- Do not claim this powers Pairwise production scoring or hires for you.
- Do not document write MCP tools.

## Measure this loop

**Loop 6 - MCP read funnel complete** (optional interview branch) and **Loop 2 / 3** when notes refresh screens or personas.

- Hygiene: transcript invent = fail for the invent metric in Loop 6.
- When interviewer notes change must-have questions or persona signals, log toward Loop 2 coverage revisions and Loop 3 refresh cadence.
- See `docs/LOOPS_AND_METRICS.md`.
