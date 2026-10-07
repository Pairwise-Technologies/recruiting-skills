---
name: hard-screens-interviewable
description: "Turn must-have hard screens into interviewable questions with probe depth for specialized recruiting."
---

# hard-screens-interviewable

**When to use:** The role has hard must-haves that a keyword screen cannot prove (hands-on characterization, fixture design, controls bring-up, lab methods). You need interviewable questions before the screen, not after a useless "yes."

## Purpose

Turn each hard must-have into at least one **interviewable question** with probe depth, so specialized eng survivors can show depth and weak keyword matches get exposed. Outputs are interviewer aids and assistive rubric drafts for **human judgment only**. Interviewer notes feed persona refresh (Loop 3). This does not auto-score interviews or hire for you.

## Inputs

- Role must-haves (hard screens) as a numbered list
- Domain context (sensors, char, controls, embedded, etc.)
- Optional: existing interview outline; ideal/anti persona signals
- Optional: prior interviewer notes from the same role family (synthetic in public examples)

## Outputs

- Question bank mapped 1:1 to each hard screen
- Probe depth notes (fixture / method / metrics / tradeoffs) for humans to ask
- Assistive pass/fail rubric **draft** for interviewer notes (human judgment only)
- Coverage checklist: which must-haves still lack an interviewable Q

## Procedure

1. List must-haves that boolean search cannot prove (hands-on work, judgment calls, lab methods).
2. For each must-have, draft one concrete primary ask. Prefer "walk the last time you…" over "do you have experience with…".
3. Add 2-3 follow-ups that force specificity (fixture, excitation, metrics reported, what failed, what you would change).
4. Write a one-line assistive rubric draft per question: what a strong answer cites vs a shallow answer. Mark it **draft for human interviewer**.
5. Attach the bank to the interview plan. Do not auto pass/fail from transcript keywords.
6. After interviews, harvest notes: which questions discriminated, which got "yes but useless." Propose persona patches (Loop 3) and revise this bank (Loop 2).

## Worked synthetic example

**Must-haves (synthetic role: Sensor Characterization Engineer):**
1. Hands-on sensor characterization (not only datasheet reading)
2. Fixture or bench setup ownership
3. Clear metrics reporting to cross-functional partners

**Question bank (excerpt):**

| Must-have | Primary ask | Follow-ups | Rubric draft (human) |
|-----------|-------------|------------|----------------------|
| Hands-on char | "Walk me through the last sensor you characterized end to end." | What stimulus? What did you measure? What surprised you? | Strong: names device class, stimulus, metrics, one failure. Shallow: only "ran tests" / datasheet talk |
| Fixture ownership | "Describe the fixture or bench you used. What did you build vs inherit?" | How did fixture error show up in data? | Strong: ownership + error sources. Shallow: "used the lab setup" |
| Metrics reporting | "What metrics did you report, to whom, and what decision did they drive?" | Which metric was noisy and how did you handle it? | Strong: metric → audience → decision. Shallow: vague "shared results" |

**Coverage:** 3/3 must-haves have an interviewable Q → hard-screen coverage 100% for this run.

## Failure modes / edge cases

- **"Yes but useless":** Questions answerable with a vague yes. Rewrite to demand a walked example.
- **Coaching the game:** Publishing ideal answers that candidates can memorize. Keep rubrics interviewer-side.
- **Transcript auto-score:** Keyword-matching transcripts for pass/fail. Forbidden; human judgment only.
- **Overlong banks:** More than one primary ask per must-have without time. Prefer depth on fewer questions.
- **Missing domain:** Must-have is "culture fit" only. This skill is for hard technical screens; park soft screens elsewhere.

## Forever don'ts

- Do not invent candidate answers or claim transcript content you did not read.
- Do not publish real interview transcripts or candidate PII.
- Do not auto-pass/fail from assistive rubrics without human review.
- Never claim agents screen or hire on the client's behalf.
- No scoring-model internals or fraud thresholds.

## Measure this loop

**Loop 2 - Hard-screen → interviewable Q** (see `docs/LOOPS_AND_METRICS.md`).

- Primary: hard-screen coverage (% must-haves with an interviewable Q).
- Also: draft accept / edit / reject rate on the question bank.
- Downstream: interviewer notes that change likes/signals → Loop 3 persona refresh.
- Sample floor: one full must-have list per role; revise bank after 3+ interviews using it.
- Write-back: questions that flopped → revise this file; durable signals → propose `ideal-anti-persona` patch.
