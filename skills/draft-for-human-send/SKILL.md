---
name: draft-for-human-send
description: "Draft candidate outreach for human review and send only; never auto-send email or LinkedIn."
---

# draft-for-human-send

**When to use:** You need outreach or follow-up text (email, LinkedIn, etc.) and a human will review and send. Never when anyone expects auto-send from a skill or agent.

## Purpose

Produce outreach or follow-up **drafts** strictly for human review and human send. Claim hygiene is part of the skill: every factual claim must be traceable to the brief. This skill stops at "awaiting human send." Sending is always a separate human action.

## Inputs

- Candidate / context brief (synthetic examples only in public copy)
- Channel (email / LinkedIn / other) and tone prefs
- Call-to-action the recruiter intends
- Optional: persona one-liner and role one-liner (no invented candidate history)

## Outputs

- Draft message text plus subject/opener variants
- Review checklist completed (facts claimed, PII, overpromises)
- Explicit status: **awaiting human send** (never "sent" from this skill)

## Procedure

1. Read the brief. List allowed facts (title, company, mutual context, role hook). Cross out anything not in the brief.
2. Draft a short message using only allowed facts. Prefer specific role/problem hooks over generic flattery.
3. Produce 2 subject/opener variants max unless the recruiter asked for more.
4. Run the review checklist:
   - Every experience claim appears in the brief
   - No metrics invented
   - No fake interview or PDF quotes
   - No real PII in public/shared drafts beyond what the operator already intended to send
   - CTA is clear and human-owned
5. Mark status **awaiting human send**. Do not enqueue, schedule, or call any send/write MCP tool (this kit documents none).
6. Log human outcome: sent as-is / edited / rejected (Loop 5). Capture edit reason tags when edited or rejected.

## Worked synthetic example

**Brief (synthetic):**
- Candidate: "Taylor Brooks", currently "Firmware Engineer" at "Harbor Devices" (fake)
- Role: Embedded controls on a mobile robot seat (client unnamed in public copy)
- Hook allowed: Harbor Devices ships handheld sensing hardware; role needs bring-up comfort
- Channel: email
- CTA: 20-minute conversation this week

**Draft A (synthetic):**
Subject: Controls bring-up seat / quick chat?  
Body: Taylor - I am hiring for an embedded controls seat on a mobile robot product. Your Firmware Engineer work at Harbor Devices sits close to the bring-up work this team owns. Open to a 20-minute chat this week?

**Checklist:** Title+company from brief ✓ · No invented metrics ✓ · CTA clear ✓ · Status: awaiting human send ✓

**Outcome log (synthetic):** Human edited (shortened subject) then sent → count as **edit** for Loop 5, reason tag `subject-length`.

## Failure modes / edge cases

- **Invented rapport:** "Loved your talk on Kalman filters" when the brief never mentioned it. Delete.
- **Auto-send pressure:** Operator asks the agent to "just send it." Refuse; restate human-send rule.
- **Overlong essays:** Drafts longer than a short screen invite. Cut; put depth in the call.
- **Wrong channel voice:** LinkedIn note written like a formal offer email. Match channel norms.
- **PII in public examples:** Real emails/phones in the skill file. Use fakes only.

## Forever don'ts

- Never auto-send email, LinkedIn, SMS, or in-app messages.
- Never invent experience, metrics, or interviews the brief did not contain.
- No real candidate PII in public examples (fake names / placeholder IDs only).
- Do not imply Pairwise agents hire or screen for the client.
- Do not document write MCP tools for send.

## Measure this loop

**Loop 5 - Draft-for-human-send** (see `docs/LOOPS_AND_METRICS.md`).

- Primary: draft accept / edit / reject rate (sent as-is / edited / rejected).
- Optional later: edit distance on accepted edits.
- Sample floor: ~15 drafts on one channel before proposing checklist/tone patches.
- Write-back: recurring edit reason tags → update review checklist and example shape in this file (human-approved).
