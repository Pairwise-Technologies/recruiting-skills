---
name: outreach
description: >-
  Draft high-response cold outreach (one initial message + one follow-up) for an
  individual engineering candidate, or decide not to contact them. Use when a
  recruiter pastes a LinkedIn profile or resume and asks how to reach out, wants
  a stronger draft, asks whether to include the JD, or asks whether to contact at
  all (e.g. they work at the client). Not for bulk pipeline triage, auto-send,
  reminders without a draft ask, or parallel A/B versions.
---

# outreach

**When to use:** A recruiter asked for outreach or follow-up text for one candidate (email or LinkedIn) and a human will review and send. Also use to decide whether contact is appropriate.

**When not to use:** Reminder-only asks; auto-send expected; bulk triage across a tracker; spawning parallel versions beside an existing draft.

## Purpose

Produce **one** initial message and **one** follow-up for a specific candidate and role, plus short judgment notes. Pick the best angle and commit. Assistive only: drafts stop at awaiting human send. Never hire, reject, or contact candidates from this skill.

Skill-craft: YAML `name` matches the folder; `description` is the catalog when-to-use line; body is generic reusable steps with no assistant-specific channels, repos, or IDs; prefer one tight skill over parallel dumps.

## Inputs

- **Candidate**: LinkedIn profile or resume text (pasted). LinkedIn URLs often cannot be fetched; work from pasted text.
- **Role**: client (or hiring org), team, location, engagement type (contract/FTE), scope. Reuse a role brief from the thread when present. If location or engagement type is missing, ask once.
- **Operator context**: job-hunting, overqualified, relocation, personal connection, compensation room. Treat as the strategy brief.
- **Channel**: email, LinkedIn connect note, or LinkedIn DM (DM only after connection accepted).
- Optional: existing draft to tighten (typos/clarity only; do not fork).

## Outputs

- One-line verdict when important (e.g. do not contact).
- Exactly one **initial** draft and one **follow-up**.
- Notes: 3-5 judgment bullets (lever, verify-before-send, likely objections).
- Completed review checklist; status **awaiting human send**.

## Procedure

1. Confirm an explicit draft ask (or "should we contact?"). A reminder to ping is not permission to write.
2. **Pre-flight.** If one fails, say so plainly and do not draft (conditional draft only when asked):
   - **Employed by the client.** Vendor non-solicitation is common; FTE-to-contractor at the same company is usually a downgrade. Profiles go stale: if they left, check rehire/cooling-off first.
   - **Personal connection.** Omit if unwanted. Never invent discovery stories; never reference how private info was learned. Advise acknowledging if the candidate raises it; disclose internally if they advance.
   - **Mismatched role facts.** Flag when outreach is pointless.
3. **Read the candidate** from the profile only: 2-3 specific hooks (projects, not adjectives); archetype; risks to address implicitly (overqualification, modality gaps, relocation). Never mention gaps or job-hopping as evaluation.

| Archetype | Signals | Primary lever | Comp line? |
|---|---|---|---|
| Active seeker / early career | Recent grad, PhD candidate, looking | Role fit + specifics | No |
| Mid/senior, possibly between roles | Long specialist career, gap or change | Scope + compensation room | Light hint ("what we can offer") |
| Senior passive | Long tenure at one large employer | Comp + methodology ownership | Explicit hint only if the operator can truly beat total comp |

4. If an existing draft is on the table, tighten only. Do not fork.
5. Write the **initial** (~90-120 words for email):
   - **Subject**: `<Domain> role with <Client> <team> (<Location>)`.
   - **Identity, one line**: who the operator is and that they place engineers with the client's teams (vendor/placement framing). Never "join our team" if that blurs agency vs client.
   - **Hook** → **role facts** (engagement, scope, location up front) → **ask** conditioned on the real filter.
6. Shape by channel: email ~one screen, one CTA; LinkedIn connect note 3-4 sentences, shared ground, no pitch; LinkedIn DM only after accept (bare accept is a hold).
7. Write the **follow-up** (~1 week if no reply). Must add something new:
   - Active/mid: new info + binary low-friction ask with an explicit out.
   - Senior passive: relationship; soft ask.
   - Active seeker: JD link can be the new information.
8. **JD sharing**: default out of the initial. Exceptions: active seekers in follow-up; anyone who asks; always check the public posting matches the message.
9. Run the checklist, then hand off. Do not enqueue, schedule, or send. If pressed to auto-send, refuse.

## Hard rules

- No compensation figures, rates, or contract terms. Hints only, per archetype.
- No calendar links in cold outreach.
- No filler openers, promo language, or exclamation points.
- Do not invent role facts; flag unverified claims as verify-before-send.
- One ask. No stacked asks or meeting-time grids unless the brief asked.
- Plain voice; sign for the operator.

## Review checklist

- Every factual claim appears in the brief
- No invented metrics, interviews, or rapport
- CTA clear; channel voice matches
- Status set to awaiting human send

## Worked synthetic example

**Brief (synthetic):** Jordan Hale, Controls Engineer at Northline Robotics (fake). Role: embedded controls for client Apex Mobility (fake), contract, Bay Area. Hook: Northline field-robot bring-up. Channel: email. Mid-career, open to relocate. Ask to draft: yes.

**Verdict:** Clear to contact (not employed by Apex).

**Initial:**
Subject: Embedded controls role with Apex Mobility robotics (Bay Area)
Body: Jordan - I place engineers with Apex Mobility's robotics teams. Your Controls Engineer work at Northline on field-robot bring-up sits close to the embedded controls seat they need on a mobile platform (contract, Bay Area). If relocation is on the table, open to a short call?

**Follow-up:** One new scope detail (flag verify-before-send) + binary ask with out.

**Checklist:** Facts ✓ · No invented metrics ✓ · One CTA ✓ · Channel matches ✓ · awaiting human send ✓

## Failure modes / edge cases

- Reminder mistaken for draft ask; client-employed candidate drafted anyway.
- Invented rapport or role ownership; parallel A/B beside an existing draft.
- Auto-send pressure; bare LinkedIn accept treated as pitch trigger.
- JD in initial causing silent self-opt-out.
- Named-client or product-UI coupling; assistant IDs/repos hardcoded in the recipe.

## Forever don'ts

- Never auto-send. Drafts stop at awaiting human send.
- Never draft unasked; never fork parallel versions when one is enough.
- Never invent experience, metrics, interviews, or rapport.
- Never pitch in a LinkedIn connect note; never DM-pitch before accept.
- No real candidate PII in public examples; no named-client exemplars as required.
- No assistant-specific channels, repos, or IDs; no bulk pipeline triage here.

## Provenance

Operator-vetted: candidate-outreach method (pre-flight, archetypes, initial + follow-up, JD guidance) folded with Recruiting Support HITL (never-auto-send, one-draft, claim hygiene, channel shapes) and skill-authoring craft (when-to-use description, generic steps, no assistant IDs, one tight skill); portability-scrubbed for recruiting-skills 2026-10-07; QUALITY_BAR; not a bulk AI pack.
