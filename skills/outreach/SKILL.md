---
name: outreach
description: >-
  Draft one candidate outreach message (email or LinkedIn) for human review and
  send only. Use when a recruiter explicitly asked for a draft; not for reminders,
  auto-send, or parallel A/B versions.
---

# outreach

**When to use:** A recruiter explicitly asked for outreach or follow-up text (email or LinkedIn) and a human will review and send.

**When not to use:** Reminder-only asks ("don't forget to ping X"); anyone expects auto-send; you already have one draft on the table and the ask is just to "also try another version"; bulk dump of many message variants.

## Purpose

Assist recruiters by producing **one** outreach draft for human review and human send. The skill stops at "awaiting human send." It does not hire, reject, or contact candidates.

This file is also a **skill-craft example**: YAML `name` matches the folder; `description` states when to run (the only line a catalog reader uses to decide); body is generic reusable steps with no assistant-specific channels, repos, or IDs; prefer one tight skill over parallel dumps.

## Inputs

- Candidate / context brief (role, allowed facts, hook). Synthetic names only in public examples.
- Explicit ask to draft (a reminder to outreach is not an ask to draft).
- Channel: email, LinkedIn connect note, or LinkedIn DM (DM only after connection accepted).
- Intended CTA / one ask.
- Optional: existing draft to tighten (typos and clarity only; do not spawn parallel versions).
- Optional: tone prefs and persona / role one-liners that already appear in the brief.

## Outputs

- Exactly one draft (subject + body for email; note or DM body for LinkedIn).
- Completed review checklist.
- Status: **awaiting human send** (never "sent" from this skill).
- Optional outcome log: sent as-is / edited / rejected, with a short reason tag when edited.

## Procedure

1. Confirm the human asked for a draft. If they only asked to remind or queue outreach, stop; do not invent a message.
2. Read the brief. List allowed facts (title, company, mutual context, role hook). Cross out anything not in the brief. Provenance rule: never invent facts.
3. If an existing draft is already on the table, tighten typos and clarity only. Do not produce a second version beside it (one tight artifact beats parallel dumps).
4. Otherwise draft **one** message using only allowed facts. Prefer a specific role or problem hook. Cut any sentence that could go to anyone.
5. Shape by channel:
   - **Email:** about one screen long; concrete subject; exactly one yes/no or clear CTA.
   - **LinkedIn connect note:** 3-4 sentences; shared ground; no pitch; no numbers.
   - **LinkedIn DM:** only after connection accepted. A bare accept is a hold, not a pitch trigger.
6. Enforce **one ask**. No stacked asks. No meeting-time grids unless the brief asked for them.
7. Run the review checklist before handoff:
   - Every factual claim appears in the brief
   - No invented metrics, interviews, or rapport
   - CTA clear; channel voice matches
   - Status set to awaiting human send
8. Hand off. Do not enqueue, schedule, or send. If pressed to auto-send, refuse and restate the human-send rule.
9. After the human acts, optionally log: sent as-is / edited / rejected (short reason tag when edited). Use tags to improve later drafts.

## Worked synthetic example

**Brief (synthetic):**
- Candidate: Jordan Hale, Controls Engineer at Northline Robotics (fake)
- Role: Embedded controls on a mobile platform (client unnamed)
- Hook allowed: Northline ships field robots; role needs bring-up comfort
- Channel: email
- CTA: 20-minute conversation this week
- Ask to draft: yes

**Draft (one only):**
Subject: Controls bring-up seat / quick chat?
Body: Jordan - I am hiring for an embedded controls seat on a mobile platform. Your Controls Engineer work at Northline Robotics sits close to the bring-up this team owns. Open to a 20-minute chat this week?

**Checklist:** Facts from brief ✓ · No invented metrics ✓ · One clear CTA ✓ · Channel voice matches ✓ · Status: awaiting human send ✓

**Outcome log (synthetic):** Human edited (shortened subject) then sent → edited, reason tag `subject-length`.

## Failure modes / edge cases

- **Reminder mistaken for draft ask:** "Don't forget to ping Jordan" is not permission to write the message. Wait for an explicit draft ask.
- **Invented rapport:** "Loved your talk on Kalman filters" when the brief never mentioned it. Delete.
- **Parallel versions:** Operator already has a draft; producing A/B/C wastes review time. Tighten one; do not fork.
- **Auto-send pressure:** Someone says "just send it." Refuse; restate human-send rule.
- **Bare LinkedIn accept treated as pitch trigger:** Hold. Wait for a real DM ask or next brief step.
- **Stacked asks:** Chat plus resume plus intro plus calendar grid. Cut to one ask.
- **Generic flattery:** Sentences that fit any candidate. Replace with a role/problem hook or cut.
- **Overlong essays:** Longer than a short screen invite. Cut; put depth on the call.
- **Wrong channel voice:** Connect note written like a formal offer email. Match channel norms.
- **Recipe pollution:** Baking a specific team's Slack channel, repo path, or agent ID into the skill body. Keep those out; pass them at run time.

## Forever don'ts

- Never auto-send email, LinkedIn, SMS, or any channel. Drafts stop at awaiting human send.
- Never produce parallel versions of the same message when one draft (or an existing draft) is enough.
- Never draft unasked; a reminder is not a request to draft.
- Never invent experience, metrics, interviews, or rapport absent from the brief.
- Never stack asks or propose meeting-time grids unless the brief asked for them.
- Never pitch in a LinkedIn connect note, and never DM-pitch before connection is accepted.
- No real candidate PII in public examples (fake names and placeholder IDs only).
- No named-client exemplars; keep hooks portable across LinkedIn and generic ATS workflows.
- No assistant-specific channels, repos, or IDs hardcoded in the recipe.

## Provenance

Operator-vetted: Recruiting Support HITL outreach practice (never-auto-send, one-draft, claim hygiene, LinkedIn connect-before-DM) plus Cursor skill-authoring craft (when-to-use description, generic reusable steps, no assistant-specific IDs, one tight skill over parallel dumps); rewritten 2026-10-07 for recruiting-skills QUALITY_BAR; not a bulk AI pack.
