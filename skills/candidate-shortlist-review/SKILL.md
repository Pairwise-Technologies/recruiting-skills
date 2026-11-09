---
name: candidate-shortlist-review
description: >-
  Review an already-presented shortlist when new evidence arrives, and draft
  keep, watch or withdraw recommendations plus short why-fit notes the
  decision maker may see. Use after a slate has been shared and a screen,
  resume update or new fact comes in, or when a recruiter asks who should
  stay on the slate. Works for any role and employment model. Not for the
  first ranking of a longer list (use candidate-ranking) or for building the
  role profile.
---

# candidate-shortlist-review

**When to use:** Candidates have already been presented, and the recruiter needs to review the live slate after new evidence (a screen, a resume, a note) or do a quality pass on what the decision maker can already see.

**When not to use:** Building the role profile (role-requirements); first-time ordering of a longer list (candidate-ranking); folding new hiring-team feedback into the profile itself (role-requirements-tuning first); outreach (candidate-outreach).

## Purpose

Keep a presented slate honest as evidence changes. Recommend withdraw only on a confirmed mismatch or a new gate failure; treat missing evidence as a watch, not a withdraw. Draft a short why-fit note the decision maker may see. Assistive only: a human decides what is withdrawn or updated.

## Inputs

- The **current presented slate** and, if one exists, the frozen send snapshot from candidate-ranking (order, reasons, requirements version, date).
- The **current role-requirements profile**. If feedback may have changed the bar, run role-requirements-tuning first and use that version.
- **New evidence,** any subset: transcripts or interview-transcript-review debriefs, scorecards, resume updates, eligibility facts, the candidate's own updates.
- **Engagement rules:** non-solicit, cooldown, prior-submission, current-employee, location, work-authorization and any stated hard cap, as given in the inputs.

## Outputs

- **Per-candidate recommendation:** keep, watch or withdraw, with one reason and a confidence (high, medium, low).
- **Why-fit notes** (optional, for people who stay): a short evidence-backed note the decision maker may see.
- **What would change a watch:** the one next fact worth getting.
- A list of profile questions that appeared during the review, handed to role-requirements-tuning rather than solved here.

## Procedure

1. **Confirm the bar.** Rank and review against the current confirmed profile only. Do not add a new gate that is not on that profile, even if it "feels" relevant. Preferences stay preferences.
2. **Re-apply gates and Critical must-haves.** A new confirmed knockout (current employee of the hiring company, a client-agreement restriction, a stated hard cap, a Critical miss now in evidence) can support a withdraw recommendation. Unknown is not a miss: missing resume text, a thin profile or an interview not yet held is a watch or a keep, with lower confidence.
3. **Read new interview evidence with care.** Use interview-transcript-review when a transcript exists. An incomplete screen, or one with no usable signal on a must-have, is a watch (or "get the missing signal"), not an automatic withdraw. A screen that produced a clear, confirmed mismatch with a Critical must-have can support withdraw. Refusal to engage with the interview is a process issue for the human to weigh, said plainly, not rewritten as a skills miss.
4. **Watch vs withdraw.** Seniority, location, tool preferences and thin but allowed evidence stay on watch unless they are confirmed knockouts. Withdraw is for confirmed mismatches and gate failures only.
5. **Write why-fit notes for people who stay,** when the decision maker will see them. A few sentences, tied to evidence, no invented praise, no interviewer emails or internal debate, no numeric scores. If evidence is still thin, say what is known and what is still open, or skip the note rather than guess.
6. **Do not invent a story from silence.** No new comment from the decision maker is not a reason to withdraw or to keep. If you need the profile updated, stop and hand off to role-requirements-tuning.
7. Write the recommendations and stop. A human decides what is withdrawn, updated or left as is.

## Worked synthetic example

**Role (synthetic):** Fernvale mid-market AE, requirements v2 (fictional). Slate already presented: Elena Sorensen, Kofi Mensah, Dana Whitfield.

**New evidence:** Dana's 7 November screen (see the interview-transcript-review example) did not reach deal ownership; discovery looked solid; the quota number is still unverified. A new eligibility check shows a fourth person, later added, still works at Fernvale.

**Dana Whitfield: watch** (confidence: low). The screen added some skill signal but did not confirm or disprove the Critical ownership must-have. Not a withdraw. **What would change this:** a follow-up on deals she closed alone. **Why-fit note:** Mid-market payroll sales to finance and HR buyers. A recent screen covered discovery; ownership of closed deals is still to be confirmed.

**Elena Sorensen: keep** (confidence: high). No new negative evidence. Why-fit note already sent with the slate; no change.

**Kofi Mensah: keep** (confidence: medium). No new evidence. Leave the existing note.

**Withdraw recommendation:** the later add who is a current Fernvale employee (eligibility gate). List them in the output with that gate.

## Failure modes / edge cases

- Inventing a new knockout (a preferred tool, an unconfirmed "nice to have," a guess about seniority) and withdrawing on it.
- Treating missing evidence, a missing resume, or silence from the decision maker as a fail.
- Withdrawing after an incomplete screen that never reached the must-have question.
- Putting interviewer emails or internal debate into a why-fit note.
- Updating the live slate without noticing the requirements version has changed.

## Forever don'ts

- Never withdraw, unshare, reject or contact a candidate from this skill; recommendations are for a human.
- Never add a requirement that is not on the confirmed profile.
- Never treat silence or missing evidence as a decision.
- Never invent fit, interview results or motivation.
- No numeric scores or weights; no production scoring internals.
- No real candidate or client names in shared examples.

## Provenance

Operator-vetted: a recruiting operator's post-presentation review practice (withdraw only on confirmed mismatches, missing evidence is a watch, do not invent gates, why-fit notes stay evidence-backed and free of internal-only fields), used on live shared slates and generalized to any role and employment model; QUALITY_BAR; not a bulk AI pack.
