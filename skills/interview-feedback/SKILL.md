---
name: interview-feedback
description: >-
  Turn notes or a transcript from one screen or interview into clear,
  evidence-based feedback: evidence per requirement, concerns tied to quotes,
  topics for the next round, and a check of the writer's own rating against
  the evidence. Use when an interviewer or recruiter wants help writing
  feedback before it goes into an ATS, a spreadsheet or a message. Works for
  any role and process. Not for the hire decision (use candidate-assessment).
---

# interview-feedback

**When to use:** Someone has notes or a transcript from a screen or interview and wants clear feedback to submit.

**When not to use:** A neutral debrief with no feedback (interview-transcript-review); the verdict across all evidence (candidate-assessment); ordering candidates (candidate-ranking).

## Purpose

Interview feedback is often a gut call with no evidence, or a transcript dump with no judgment. This skill ties each point to a requirement and to what the candidate said, keeps "weak answer" apart from "not asked", and checks the writer's rating against the evidence without choosing it. Usually the person who ran the interview writes their own feedback; the skill works for whoever asks. Assistive only: it drafts, and a person edits and submits.

## Inputs

- **Notes or a transcript** of the interview. If there is only memory, write it down first and mark it as recall.
- **The role-requirements profile** or the scorecard the process uses. If none exists, draft one with role-requirements and mark it draft.
- **The writer's rating or lean,** on the process's scale, if they have one.
- Optional: confirmed role terms (pay, duration, location), to check what the candidate was told; what earlier rounds covered; a few past feedback notes, to match length and tone.

## Outputs

- **Paste-ready feedback:** plain text, one line per item, with a summary, the rating, concerns and next-round topics.
- **Rating check:** whether the evidence supports the writer's rating, and any mismatch.
- **Private flags,** given separately, one line each.

## Procedure

1. **Name the material.** The interview, the role, and whose notes or transcript these are. When writing for someone else, use only their material, write in their voice, and say in one line whose notes these are and who drafted them; never fill in their views from other notes. If it is unknown whether the candidate was told about a recording or AI analysis, flag it and go on.
2. **Get the evidence.** With a transcript, run interview-transcript-review first and use its coverage, evidence table and interview checks. With notes only, map each must-have or scorecard item: a short quote or close paraphrase, a basis (verified: walked through in specific detail; claimed; not asked) and a read (strong, adequate, weak, not covered). Where one item is partly claimed and partly not asked, use the weaker basis.
3. **Keep the gates honest.** Only confirmed must-haves and knockouts can drive a negative read; preferred items add, never subtract. Not asked is not covered, never weak; an unasked knockout reads "to confirm" and goes into next-round topics. A disputed quote stays out until checked. Skip what earlier rounds covered unless something new came up.
4. **Leave out what is not evidence:** tone, nerves, accent or fluency (unless the role needs the language), guesses about honesty or personality ("quiet", "culture fit"), and protected details the candidate volunteered. Leave out other interviewers' notes and ratings unless asked to combine them.
5. **Concerns,** usually up to 3, each tied to a quote or a named gap in an answer. A must-have never reached is a gap to name, not a weakness.
6. **Next round:** the debrief's open items, or with notes only the must-haves not covered, as up to 3 topics in the feedback's voice. Topics, not a script.
7. **Check the rating.** If the writer has not given a rating, ask for it before offering any view. Then check it against the evidence, and flag a rating that rests on an item not asked, a preferred item, or something left out in step 4. With no rating yet, say which ratings the evidence supports, without picking one. The writer decides.
8. **Private flags,** one line each, no instructions: an off-limits question or remark (from the debrief's interview checks, or the writer's own account); anything told to the candidate that differs from the confirmed terms, with the confirmed wording; what was left out and why.
9. **Write it** in the writer's voice (match past notes if given), then stop. A person submits.

## Output format

```
Feedback: <candidate label> · <interview type> · <date> · from <whose notes>
Rating: <writer's rating> (confidence <low/medium/high>): <one line>
Summary: <3-5 plain sentences>
<item>: <evidence> (<basis>) → <read>
Concerns: <usually up to 3>
Next round: <topics, with why>
```

Confidence: high when every item behind the rating is verified; medium when some are claimed; low when a Critical item or knockout is still open.

Then, separately and never inside the paste-ready text: `Rating check:` and `Private:` lines. Use a table instead of item lines where the system takes one.

## Worked synthetic example

**Interview (synthetic):** Dana Whitfield, 28-minute screen on 7 November for the Fernvale mid-market Account Executive profile (fictional). Transcript and an interview-transcript-review debrief are available. The screener's rating: advance, strong yes.

```
Feedback: Dana Whitfield · recruiter screen · 7 Nov · from the screener's transcript
Rating: advance, strong yes (confidence low): clear discovery process; deal ownership still open.
Summary: Walked through a concrete first-call process with finance buyers. Says they own the forecast. Stated 142% of quota without a quota size. Deal ownership, the Critical item, was not reached.
Discovery with finance buyers: first-call agenda, step by step (verified) → strong
Closed deals as the named seller (Critical): not reached (not asked) → not covered
Forecasting: "I do own the forecast", corrected from the audio (claimed) → adequate
Concerns: 1. "142% of quota" with no quota size or deal count.
Next round: which deals they closed alone, start to signature; quota size and team split; when their title changed.
```

**Rating check:** advance is supported; "strong yes" is not yet. The only verified read is a Medium-tier skill, and the Critical item is open.

**Private:** off-limits question at 21:30 (children, "because of the on-site days"), from the debrief; answer left out. Left out: the interviewer's "seems sharp" (opinion). Multi-threading with procurement (strong-plus) was not discussed; left out, not a negative.

## Failure modes / edge cases

- A negative read on a topic never asked.
- A preferred tool or unconfirmed item quietly becoming a reason to pass.
- One great or bad answer coloring every row (halo), or comparing with the last candidate instead of the profile.
- Offering a rating before the writer gives theirs, so it anchors them.
- Private flags ending up in the pasted text.

## Forever don'ts

- Never submit feedback, change a stage, or contact anyone from this skill.
- Never invent quotes, ratings, terms or another person's views; write "not discussed".
- Never infer emotion, honesty, personality or protected traits.
- The skill computes no numeric scores or weights; on a numeric scale, the writer picks the number. No production scoring internals.
- Synthetic examples only; no real candidate or client names.

## Provenance

From a recruiting operator's screen-feedback practice (evidence per scorecard item, shown vs claimed vs not asked, concerns tied to quotes, private terms check, the writer keeps the rating), generalized to any role and process; not yet run end to end by an operator in this form; the evidence step reuses interview-transcript-review; QUALITY_BAR; not a bulk AI pack.
