---
name: interview-feedback
description: >-
  Write your own feedback for one interview you ran, from your notes or the
  transcript: evidence per requirement, concerns, a rating you choose, and
  what the next round should probe, in your own voice. Use when an
  interviewer or recruiter asks for help turning their own interview notes
  into clear, fair, paste-ready feedback. Works for any role. On request only.
  Not for writing feedback for an interview someone else ran, and not for the
  hire decision.
---

# interview-feedback

**When to use:** You ran a screen or interview, you have notes or a transcript, and you want help writing your feedback before you submit it.

**When not to use:** Feedback for an interview you did not run, or on behalf of any other interviewer (their feedback is theirs to write or not); a neutral debrief of someone else's transcript (use interview-transcript-review); the overall verdict across all evidence (candidate-assessment); ordering several candidates (candidate-ranking).

## Purpose

Interview feedback is often a gut call with no evidence, or a transcript dump with no judgment. This skill helps the interviewer write feedback that ties each point to a requirement and to what the candidate actually said, keeps "weak answer" apart from "not asked", and leaves the rating to the interviewer. Assistive only: it drafts; the interviewer edits and submits, and no one is advanced or rejected by this skill.

## Inputs

- **Your notes or the transcript** of the interview. Not your memory of it alone: if there are no notes, write down what you remember first and mark it as recall.
- **The role-requirements profile** (must-haves, tiers, knockouts) or the scorecard your process uses. Each item becomes one row. If none exists, build a draft one with role-requirements and mark it draft.
- **Confirmed role terms** (employment type, duration, location, pay basis), if you discussed them.
- Optional: what earlier rounds already covered, the rating scale your process uses, and a few past feedback notes you wrote, to match your length and tone.

## Outputs

- **Paste-ready feedback:** a short summary in your words, evidence per item, concerns, a rating you choose and next-round probes.
- **Private notes for you** (never pasted): terms you may have misstated, off-limits moments, and anything left out of the feedback and why.

## Procedure

1. **Check the inputs.** Confirm the interview, the role, and that you ran it. If you use a recording or transcript, confirm the candidate was told about the recording and any AI analysis, as your process and local rules require; if unknown, work from your own notes. If the transcript is missing or partial, say so and work from your notes at lower confidence. Never invent what was said.
2. **Map evidence to each item.** For each must-have or scorecard item: a short quote or close paraphrase (with a timestamp if you have one), its basis (verified: walked through in specific detail; claimed; not asked), and a read (strong, adequate, weak, not covered). An item a screen cannot show (for example one tagged resume) is "not for this interview". Check speaker labels: a strong "answer" may be your own words. If the transcript and your notes disagree on a quote, mark it disputed, check the recording, and use neither version until you have; the read stays open.
3. **Keep the gates honest.** Only confirmed must-haves and knockouts can drive a negative read. Preferred or unconfirmed items can add, never subtract. Not asked is not covered, never weak. A knockout you never asked about is an item to confirm, not a pass or a fail.
4. **Skip what earlier rounds covered,** unless you learned something new about it.
5. **Concerns, at most 3,** each tied to a quote. A must-have you did not reach is a gap to name, not a weakness in the candidate.
6. **Strip what does not belong.** If notes or ratings from another interviewer were pasted in, do not use them. Leave out tone, nerves, accent, fluency (unless the role needs the language), guesses about honesty or personality ("quiet", "culture fit"), and anything about protected traits the candidate volunteered. If you asked something off-limits, move it to your private notes and leave the answer out.
7. **Terms check (private).** Compare what you told the candidate about duration, conversion, pay, location and start with the confirmed terms. Note any mismatch and the correct wording so you can fix it with the candidate.
8. **Choose your rating** on your process's scale (or advance, hold, pass). The skill may say what the evidence supports; you pick. Add a one-line reason and how confident you are.
9. **Next round should probe:** 2-3 topics, each tied to a weak or uncovered must-have. Topics, not a script.
10. **Write it in your voice** (match length and words from your past notes if given), then stop. You submit.

## Output format

Give the Private block separately, after the paste-ready text, never inside it. If your system takes plain text, write one line per item instead of the table.

```
Feedback: <candidate label> · <interview type> · <date>
Rating: <your rating> (confidence <low/medium/high>): <one line>
Summary: <3-5 plain sentences>
| Item | Evidence | Basis | Read |
Concerns: <at most 3>
Next round should probe: <2-3 topics, with why>
Private (do not paste): <terms mismatch, off-limits moments, exclusions>
```

## Worked synthetic example

**Interview (synthetic):** you screened Dana Whitfield for the Fernvale mid-market Account Executive profile (fictional), 28 minutes, transcript available.

- Discovery with finance buyers: walked through their first-call agenda step by step (verified) → strong.
- Closed deals as the named seller (Critical): "142% of quota", no quota size; deals closed alone not reached (claimed / not asked) → not covered.
- Multi-threading with procurement (strong-plus): not discussed → left out, not a negative.
- Private terms check: you said "it's a one-year contract"; confirmed terms are direct hire with no set duration. Correct it with the candidate.
- Summary: clear, concrete discovery process with finance buyers. Quota attainment stated without a baseline. Deal ownership, the Critical item, not yet covered.
- Concerns: 1. "142% of quota" with no quota size or deal count (claimed only).
- Your rating: advance, confidence medium: discovery shown; ownership still open, not a negative. Probe next round: two deals closed alone, start to signature; quota size and team split.

## Failure modes / edge cases

- Writing a verdict on a topic you never asked about.
- A preferred tool or an unconfirmed item quietly becoming a reason to pass.
- One great or bad answer coloring every row (halo).
- Comparing with the last candidate instead of the profile.
- Private notes (terms errors, off-limits answers) ending up in the pasted text.
- Reading a colleague's feedback before writing your own, so yours echoes theirs.

## Forever don'ts

- Never write feedback for an interview you did not run or on behalf of another interviewer, and never chase or remind anyone to submit theirs.
- Never submit feedback, change a stage, or contact the candidate from this skill.
- Never invent quotes, ratings or terms; write "not discussed".
- Never infer emotion, honesty, personality or protected traits.
- The skill computes no numeric scores or weights; if your process uses a numeric scale, you pick the number. No production scoring internals.
- Synthetic examples only; no real candidate or client names.

## Provenance

From a recruiting operator's screen-feedback practice (evidence per scorecard item, shown vs claimed vs not asked, concerns tied to quotes, private terms check, interviewer keeps the rating), generalized to any role and process; the on-request, own-interview form has not yet been run end to end by an operator; aligns with interview-transcript-review on basis tags and over-reading; QUALITY_BAR; not a bulk AI pack.
