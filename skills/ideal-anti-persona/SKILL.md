---
name: ideal-anti-persona
description: "Build ideal and anti-persona cards from likes and shipped profiles, not the JD alone."
---

# ideal-anti-persona

**When to use:** You are opening or refreshing a screen and the JD alone will mislead (buzzwords, keyword soup). You have client likes, advanced profiles, or clear pass reasons to learn from (use synthetic exemplars in any public/shared copy).

## Purpose

Build **ideal** and **anti** persona cards from what the hiring team actually advances and passes, not from the JD alone. Personas are assistive checklists for human screeners. They do not auto-score, auto-reject, or replace recruiter judgment.

## Inputs

- Client "liked" / advanced profile patterns (synthetic exemplars only in public copy)
- Pass / soft-no reasons where available (conceptual tags, not live PII)
- JD must-haves and nice-to-haves (secondary input)
- Optional: interviewer notes from `hard-screens-interviewable` runs

## Outputs

- Ideal persona card: recurring signals that correlate with advance
- Anti-persona card: recurring signals that correlate with pass
- Assistive checklist for human screeners (one page)
- Refresh note: what changed since the last persona version

## Procedure

1. Gather like/ship and pass exemplars. In public skill copy, keep them synthetic. Internally, strip PII before any shared paste.
2. Extract recurring **domain** signals: modality, stack, company type, seniority shape. Separate these from JD buzzwords.
3. Build the ideal card: 5-8 signals max, each observable on a summary card or short screen.
4. Mirror with anti-signals from passes (wrong modality, title cosplay, company type mismatch, seniority mismatch). Stay conceptual; no numeric score cutoffs.
5. Cross-check against the JD: note where persona and JD disagree; persona wins for screen priority unless the client explicitly overrides.
6. Publish the persona pair for human use on the board. Schedule a refresh when likes shift (Loop 3).
7. When hard-screen interviewer notes contradict the cards, propose a patch; human approves before editing this file.

## Worked synthetic example

**Role (synthetic):** Controls Engineer for mobile robots  
**Liked patterns (synthetic, anonymized shape):**
- Shipped motor control or state estimation on real hardware (not only sim)
- Companies: robotics OEMs, autonomy startups, industrial automation
- Titles: Controls Engineer, Embedded Controls, Robotics Software (controls-heavy)

**Pass patterns (synthetic):**
- Pure web/backend with "robotics interest"
- Only coursework, no bring-up story
- Title "Robotics Engineer" at a pure AI research lab with no hardware loop

**Ideal card (draft):**
- Evidence of closed-loop control on hardware
- Comfortable reading traces / logs from bring-up
- Company type: ships physical robots or motion systems
- Can walk a tuning story (gains, limits, what broke)

**Anti card (draft):**
- Portfolio is demos/sim only with no hardware constraint story
- Keyword match on "ROS" without controls depth
- Seeking research-only roles when this seat is product bring-up

**Refresh note:** "v2 after three client likes shifted toward embedded controls over perception-heavy profiles."

## Failure modes / edge cases

- **JD-only trap:** Building personas from the posting without likes. Invalid for this skill.
- **Overfit to one rockstar:** One advanced profile becomes the whole ideal. Require recurring signals.
- **PII leak:** Real names, LinkedIns, or UUIDs in public cards. Strip; use synthetic shapes.
- **Auto-reject misuse:** Treating anti-persona as a hard bot reject. Humans decide.
- **Stale cards:** Likes shifted weeks ago and nobody refreshed. Check cadence metric.

## Forever don'ts

- Do not publish real candidate names, LinkedIns, or live pipeline UUIDs.
- Do not treat JD text as the sole source of truth over client likes.
- Do not imply personas auto-score or auto-reject candidates.
- No named-client exemplars or exception tables in public copy.

## Measure this loop

**Loop 3 - Ideal / anti-persona refresh** (see `docs/LOOPS_AND_METRICS.md`).

- Primary: persona refresh cadence (when client likes shift).
- Also: draft accept / edit / reject rate on proposed persona patches.
- Upstream: Loop 2 interviewer notes; Loop 1 domain-fit reason tags.
- Sample floor: refresh when 3+ new like/pass exemplars contradict the cards, or on a weekly check for hot roles.
- Write-back: approved patch → update cards in this file; cross-link new signals into domain-fit / hard-screen examples when useful.
