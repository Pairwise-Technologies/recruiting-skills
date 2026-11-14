---
name: interview-transcript-review
description: >-
  Extract the evidence from one screen or interview transcript against a
  role-requirements profile: what the candidate showed, what they only
  claimed, what was never asked, and how the interview itself was run. Use
  when a recruiter has a transcript or detailed notes and needs a checked
  debrief before candidate-assessment, a slate update or a shared summary.
  Works for any role. Gives no verdict. Not for writing an interview guide.
---

# interview-transcript-review

**When to use:** A recruiter has a screen or interview transcript (or detailed notes) and wants the evidence pulled out and checked before anyone judges the candidate.

**When not to use:** Writing an interview guide; the verdict on a candidate (use candidate-assessment, with this debrief as an input); ordering a list (use candidate-ranking).

## Purpose

One conversation is easy to over-read: a topic never reached becomes a "miss", a headline number becomes a fact, and a transcription error becomes a red flag. This skill separates what was shown from what was claimed or never asked, and checks the interview as well as the candidate. Assistive only: it gives no verdict and does not advance, reject or contact anyone.

## Inputs

Use whatever exists. A partial transcript still gets a read, with lower confidence.

- The transcript or detailed notes: who was present, the length, and whether it ended early.
- The **role-requirements profile**, especially must-haves tagged **screen**.
- Optional: what the interview was meant to cover; the resume or a prior candidate-assessment read, so contradictions can be named; the interviewer's own notes.

## Outputs

- **Coverage:** each screen-tagged must-have and each knockout marked asked, partly asked or not asked.
- **Evidence table:** per axis, a short quote or close paraphrase with its timestamp, and a basis: **verified** (walked through what they did, how and why, with specific detail), **claimed** (stated, including self-reported results), **inferred** (implied, or a "how I would do it" answer), **disputed** (sources disagree) or **no evidence**.
- **Interview checks:** transcript problems, leading or off-limits questions, misstatements to the candidate, and interviewer opinions kept apart from evidence.
- **Confidence** per axis, and **open items:** at most 3 things still to find out, not a script.
- Optional **shareable summary** for the decision maker.

## Procedure

1. **Check that the transcript may be used.** The candidate must have been told about the recording, and about any AI analysis, as the operator's process and local rules require. If that is unknown, ask before going on.
2. **Inventory the conversation.** Length, speakers, early end, missing segments, or questions the candidate declined. An incomplete interview or transcript is a fact, not a hidden fail.
3. **Map coverage.** For each screen-tagged must-have and each knockout, record whether it was asked. Not asked is no evidence, never a miss; neither is a gap on a not-required item.
4. **Extract evidence.** Quote briefly, with a timestamp, and tag the basis. A number with no baseline, or a title with no substance behind it, is claimed. Compare with the resume and list contradictions.
5. **Check the transcript before relying on it.** Confirm each quote that hurts the candidate against the audio or the notes, and confirm the speaker label on strong answers too: an "answer" may be the interviewer talking. Speech-to-text drops and swaps words, more for some accents than others. If the sources still disagree, tag the quote disputed, use neither version, and make it an open item.
6. **Check the interview, not only the candidate.** Note must-haves the interviewer skipped, leading questions that handed over the answer, and off-limits questions or remarks (age, family, health, religion, origin and similar). Flag them for whoever owns interview quality in your process, and leave the answers out of the evidence. Also flag anything the interviewer told the candidate that contradicts the approved terms, pay, location or sponsorship, so a human can correct it. Keep the interviewer's adjectives ("sharp", "not a culture fit"), firsthand or relayed, as opinion apart from evidence; ask which job-related behavior they meant.
7. **Do not over-read.** Tone, nerves, accent, grammar, filler words and short answers are not evidence of skill. Never infer emotion, honesty or personality. Leave out protected details the candidate volunteered. Lower confidence instead of filling gaps.
8. **Write the debrief:** coverage, evidence table, interview checks, confidence and open items. For a shareable summary (decision maker or hiring channel), keep only evidence about the work: no interviewer opinions, internal debate, interview-check flags or protected details.
9. **Protect independent judgment.** On a panel, do not share this debrief or the summary with interviewers who have not yet submitted their own feedback.
10. **Hand off and stop.** candidate-assessment owns the verdict; if asked "should we move forward?", name what still blocks it. If the person is already on a presented slate, flag candidate-slate-review.

## Worked synthetic example

**Inputs (synthetic):** Dana Whitfield, 28-minute screen on 7 November for the Fernvale mid-market AE profile (fictional). Candidate told about recording and AI notes at booking. Two speakers, no gaps; time ran out before deal ownership.

**Coverage:** discovery and forecasting (skills) asked; closed deals as the named seller (Critical, screen) not asked; team and environment (screen) not asked; knockouts (work authorization, Denver days) asked, both met.

| Axis | Evidence | Basis |
|---|---|---|
| Skills: discovery | 12:40, walked through their first-call agenda with finance leads, step by step | Verified |
| Ownership depth | 08:15, "I did 142% of quota last year", no quota size or deal count | Claimed |
| Ownership depth: closed alone | Not asked; time ran out | No evidence |
| Skills: forecasting | 16:05, transcript reads "I don't own the forecast"; the audio says "I do own the forecast" | Claimed (corrected) |

**Interview checks:** at 21:30 the interviewer asked whether they have children "because of the on-site days". Off-limits: flagged, answer excluded; the job-related question is whether the two Denver days work for them. Interviewer note "seems sharp" kept as opinion.

**Confidence:** low on ownership depth, the Critical axis; medium on discovery.

**Open items:** which deals they closed alone; quota size; when their title changed.

**Shareable summary:** Screened 7 November. Explained a concrete first-call process with finance buyers. Quota attainment stated without a baseline; deal ownership not yet covered.

**Handoff:** candidate-assessment for the verdict; candidate-slate-review, because Dana is on the presented slate.

## Failure modes / edge cases

- Treating "not asked" as "cannot do it".
- Rewriting a claim as verified, especially a headline metric with no baseline.
- Acting on a transcription error or a mislabeled speaker.
- Halo or first impression: one strong answer colors every axis. Read each axis on its own.
- Comparing the candidate with the last interview instead of with the profile.
- Opinions, flags or protected details leaking into the shareable summary.

## Forever don'ts

- Never advance, reject or contact a candidate, or give a hire verdict, from this skill.
- Never invent quotes, results or reasons for leaving.
- Never infer emotion, honesty, personality or protected traits; never use accent, grammar or fluency as evidence unless the role requires that language skill.
- Never script the next interview; list only what is still unknown.
- No numeric scores or weights; no production scoring internals.
- No real candidate or client names in shared examples.

## Provenance

Operator-vetted: a recruiting operator's transcript-read method (coverage first, shown vs claimed, not asked is no evidence, shareable notes kept free of internal opinion), used on live screens and generalized to any role; interview-check and independent-judgment rules draw on `docs/SOURCES.md`; QUALITY_BAR; not a bulk AI pack.
