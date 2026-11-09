---
name: role-requirements-tuning
description: >-
  Fold confirmed hiring-team or decision-maker feedback into an existing
  role-requirements profile, and leave unconfirmed comments and silence out of
  the bar. Use when feedback arrives on a candidate, a slate or the role
  itself, or when the team is rejecting people who looked right on paper.
  Works for any role and employment model. Not for chasing feedback, writing
  the public job post, or reviewing the live slate in detail.
---

# role-requirements-tuning

**When to use:** The hiring team or decision maker has given feedback on the role or on presented candidates, and the requirements profile needs a careful update.

**When not to use:** Chasing, nudging or inventing feedback that was not given; writing or rewriting the public posting (use role-job-description after the profile is updated); a detailed keep or withdraw pass on the live slate (use candidate-shortlist-review after the profile is updated); building the first profile (use role-requirements).

## Purpose

Move the bar only as far as the new evidence supports. Confirmed, generalizable feedback updates tiers, must-haves or knockouts. Vague impressions, one-person reactions and silence stay out of the profile, or go to open questions. Assistive only: the updated profile is a draft for the recruiter and hiring team to confirm.

## Inputs

- The **current role-requirements profile**, with its version or date, and any changelog.
- The **feedback itself:** what was said, who said it, when, and whether it was about the role or about a specific person. Quotes or close notes beat a paraphrase.
- What has already been presented or interviewed, so person-specific comments can be seen in context.
- Employment model and engagement rules, in case eligibility comments appear.
- Optional: the frozen send snapshot from candidate-ranking; interview debriefs.

## Outputs

- **Profile delta:** what changed, what was considered and left unchanged, and what is still open, each with the feedback that drove it.
- An **updated profile** (or a marked-up copy) with a new version and date.
- **Handoffs:** whether the public JD now disagrees and should go through role-job-description; what candidate-shortlist-review should do with people already presented; what candidate-ranking should optimize for on the next slate.

## Procedure

1. **Inventory the feedback.** Split it into four buckets:
   1. Confirmed role changes (they said the bar itself should change).
   2. Reactions to one person (liked, disliked, or mixed, about that person).
   3. Vague impressions with no actionable bar ("not quite right," "let's see more").
   4. Silence: no reply, no thumbs, no comment.
2. **Silence is not a signal.** Do not raise, lower or add a requirement because feedback did not arrive. Do not draft a nudge from this skill. If a decision is blocked, say "still waiting," not "they must not want X."
3. **Do not promote a one-person reaction into a role-wide knockout** unless the decision maker clearly generalized it. "We liked how Elena closed alone" can support keeping ownership depth Critical; it does not, by itself, add "must look like Elena" or a new years-of-experience gate.
4. **Preferences stay preferences** until someone states a hard rule. A comment about a tool, a company, a degree or a title is not a knockout unless they said it is required or disqualifying.
5. **Update the profile surgically.** Change only the axes the confirmed feedback touches. Record the source and date in a short changelog. If the new bar conflicts with the live posting, list a JD disagreement. If evidence is still too thin to change a tier, add an open question instead of guessing.
6. **Hand off, then stop.** Run role-job-description only if the posting would now misstate the bar. Run candidate-shortlist-review on the live slate against the new version (watches and withdraws may change). Run candidate-ranking for any next slate, using the new profile and these calibration notes. A human confirms the profile before it becomes the bar.

## Worked synthetic example

**Role (synthetic):** Fernvale mid-market AE, requirements v2, 1 November (fictional). Slate presented: Elena, Kofi, Dana. **Feedback, 10 November, hiring manager:** "Elena is what we mean: she could name deals she closed alone. Dana felt early. No comment on Kofi yet. We are not requiring payroll experience."

**Bucketed:** Elena's comment is a person-specific reaction that also restates a Critical already on the profile (closed deals as the named seller). Dana "felt early" is vague on the axis (ownership vs years vs presence). Silence on Kofi is not a signal. "Not requiring payroll" is a confirmed role change: payroll stays preferred, not required (already the profile, now confirmed).

**Delta, v3, 10 November:**
- Changed: none to knockouts; changelog notes payroll explicitly confirmed as not required, in case the JD still implies it.
- Unchanged: ownership depth stays Critical; no new years-of-experience gate from "Dana felt early."
- Open: what "early" meant for Dana (deal ownership, years, or presence), to ask if it comes up, not to invent a knockout now.

**Handoffs:** role-job-description, only if the live post still lists payroll as required. candidate-shortlist-review: do not withdraw Kofi for silence; Dana stays a watch until ownership is verified. candidate-ranking for a next slate: keep emphasizing evidenced deal ownership, not a new seniority cutoff.

## Failure modes / edge cases

- Treating silence or missing thumbs as a no, or as approval.
- Turning one rejected (or one loved) candidate into a new must-have that the decision maker did not state.
- Promoting a preference to a knockout.
- Rewriting the whole profile when only one axis was mentioned.
- Chasing the hiring team for comments from this skill.
- Changing the live slate here instead of handing off to candidate-shortlist-review.

## Forever don'ts

- Never chase, nudge or invent hiring-team feedback.
- Never treat silence as a preference or a decision.
- Never add a knockout the decision maker did not state.
- Never present the updated profile as a hire or reject of any person.
- No numeric scores or weights; no production scoring internals.
- No real candidate or client names in shared examples.

## Provenance

Operator-vetted: a recruiting operator's calibration practice (fold only confirmed, generalizable feedback; silence is not a signal; do not invent gates from one-person reactions; never chase comments), used on live searches and generalized to any role and employment model; QUALITY_BAR; not a bulk AI pack.
