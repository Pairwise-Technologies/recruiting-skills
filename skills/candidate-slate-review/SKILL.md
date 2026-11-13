---
name: candidate-slate-review
description: >-
  Review a slate already presented to a decision maker (hiring manager,
  client or panel) when anything changes: the candidate's interest, offers,
  comp or notice, new screens, or a new gate. Recommends keep, watch or pull
  submission for each person, and drafts why-fit notes and short updates for
  a human to send. Use after a slate is shared, or when a recruiter asks
  who should stay on it. Works for any role and employment model. Not for the
  first ranking of a list (use candidate-ranking).
---

# candidate-slate-review

**When to use:** A slate has been presented, and something has changed since: a screen, a candidate update, a dated risk coming due, or a new fact about eligibility.

**When not to use:** First ordering of a longer list (candidate-ranking); changing the bar itself (role-requirements); outreach to new candidates (candidate-outreach).

## Purpose

Keep a presented slate honest over time. Most slates change because of the candidate (interest cools, an offer arrives, comp moves), not because of new evidence about skills. Recommend pulling a submission only on a confirmed reason, treat missing evidence as an open item, and keep everyone informed through drafts a human sends. Assistive only: a human decides every status change.

## Inputs

- The **presented slate** and the frozen send snapshot from candidate-ranking: order, reasons, named risks with dates, requirements version.
- The **current role-requirements profile**. If feedback changed the bar, update it with role-requirements first.
- **Candidate status:** last contact, interest, other processes and offer deadlines, comp or notice changes, logged contact attempts.
- **New evidence:** interview-transcript-review debriefs, candidate-assessment reads, scorecards, resume updates.
- **Engagement rules and consent:** what each candidate agreed may be shared, and any non-solicit, cooldown or prior-submission rules.

## Outputs

- **Per candidate:** keep, watch or pull submission (in-house: remove from the slate), with the main reason, any deadline, and your confidence in the recommendation (high, medium, low). **Watch** means something could change the status soon: a dated risk not yet checked, no reply, or new doubt about a Critical must-have. Name the one fact that would settle it. A must-have simply not yet screened is a keep with an open item.
- **Status log:** dated reason for each change, and who started any exit: candidate withdrew, submission pulled, or decision maker declined.
- **Why-fit notes** for everyone who stays (keep or watch), when the decision maker will see them.
- **Drafts for a human to send:** an update to the decision maker; a short note to each candidate whose status changed or whose dated risk needs a check-in.
- **Profile questions** that came up, handed to role-requirements.

## Procedure

1. **Confirm the bar.** Review against the current profile version. If it changed since the snapshot, say so. Never add a gate the profile does not have.
2. **Candidate side first.** For each person: still interested, other offers and their deadlines, counteroffer risk, comp or notice changes. Re-check every named risk in the snapshot, dated ones first. A candidate who has not replied after the logged attempts your process sets is a watch ("confirm interest"), not a pull.
3. **Representation.** Check that consent covers what you plan to share (resume, screen findings, comp, other offers and their deadlines). If consent is unknown, share only work evidence already shared, and flag it to confirm. Look for new conflicts (another submission, a direct application); flag them for a human, and pull only when an engagement rule requires it.
4. **Gates and Critical must-haves.** Re-apply the profile's knockouts and the engagement rules. A confirmed knockout supports a pull. Unknown is not a miss: list unconfirmed gates to check.
5. **New evidence.** Use the debrief or assessment, not the raw transcript. Evidence from another source (a work sample) counts; name the source. An interview that never reached a must-have leaves it an open item; a disputed quote or new doubt about a Critical must-have is a watch. A confirmed miss on a Critical must-have supports a pull. A refusal to engage is a process issue for the human to weigh.
6. **Same pass for everyone.** Every slate member gets the same checks. Never compare two people on an axis only one of them was assessed on. The slate's mix is never a reason for one person's status.
7. **Recommend** keep, watch or pull for each person. No new comment from the decision maker is not a reason either way.
8. **Why-fit notes** for keeps and watches: start from the snapshot's Why line and update it. 2-4 sentences on why this person fits, the strongest evidence, and what is still open. Share only what the candidate agreed to. Never protected details, salary history, interviewer opinions, internal debate or scores. If evidence is thin, say what is known and what is open.
9. **Draft the updates,** one line per change: what changed for the decision maker, and any candidate deadline that needs their decision; a clear, kind note to any candidate whose status changed, and a check-in for any dated risk. Never send them.
10. **Log the dated reasons and stop.** A human decides what changes. If pulls or withdrawals leave the slate thin, rerun candidate-ranking and freeze a new snapshot; never edit the old one.

## Worked synthetic example

**Slate (synthetic):** Fernvale mid-market AE, requirements v2 (fictional). Sent 4 November: Elena Sorensen, Kofi Mensah, Dana Whitfield; Jordan Ellis added 6 November as a backup. Review on 10 November.

**Elena Sorensen: keep** (confidence: high). Still engaged; OTE ask unchanged at $160K, the named risk. She agreed to share her resume and comp ask. **Why-fit note:** Elena has closed mid-market HR software deals as the named seller for 3 years and grew her territory from 6 to 15 accounts. A 3 November screen confirmed three deals she closed alone. Open: her OTE ask is just above the band.

**Kofi Mensah: watch** (confidence: medium). The snapshot's dated risk came due: his other offer expires 14 November, and he would wait for Fernvale only with an interview this week. He agreed to share the deadline with the hiring team. **Next fact:** an interview date by 13 November. **Why-fit note:** Kofi closes full-cycle deals selling finance software and owned a region from launch. Open: a screen for this role.

**Dana Whitfield: keep, open item** (confidence: medium). The 7 November screen confirmed discovery skills but never reached deal ownership, the Critical must-have. Nothing new casts doubt on it, so it stays open: not a watch or a pull. **Next fact:** which deals they closed alone. **Why-fit note:** Dana sells payroll software to finance and HR leads and showed a clear discovery process in a screen. Open: which deals they closed alone.

**Jordan Ellis: candidate withdrew** (accepted another offer, 9 November). No pull needed; log it.

**Draft to the decision maker:** "Kofi has another offer due 14 November; an interview this week keeps him in play. Jordan accepted another role and is off the slate. Dana's ownership question is still open; we are scheduling a short follow-up."

**Draft to Jordan:** "Congratulations on the new role, and thank you for your time with Fernvale. I would be glad to stay in touch."

## Failure modes / edge cases

- Reviewing skills evidence only, while an offer deadline quietly passes.
- Pulling someone after an incomplete screen, a missing resume line, or silence.
- Inventing a gate (a preferred tool, a guess about seniority) and pulling on it.
- Sharing details the candidate did not agree to share.
- Updating the slate without noticing the requirements version changed.

## Forever don'ts

- Never pull, reject or contact anyone, or send a note, from this skill.
- Never add a requirement that is not on the current profile.
- Never treat silence or missing evidence as a decision.
- Never invent fit, interview results or motivation.
- No numeric scores or weights; no production scoring internals.
- No real candidate or client names in shared examples.

## Provenance

Operator-vetted: a recruiting operator's post-presentation review practice (pull only on confirmed reasons, missing evidence is an open item, no invented gates, why-fit notes backed by evidence), used on live shared slates and generalized to any role and employment model; QUALITY_BAR; not a bulk AI pack.
