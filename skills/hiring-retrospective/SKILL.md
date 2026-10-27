---
name: hiring-retrospective
description: >-
  Run a blameless retrospective on a finished, stalled or partly finished
  search: compare how the requirements were written with who was hired, who
  was interviewed and how the interviews went, then read the funnel and the
  timeline. Returns a short report and at most 3 evidence-backed suggestions
  to reach the right candidate faster next time. Use when a search closes,
  is cancelled or reset, or when a team asks why a search took so long.
  Works from a full pipeline down to only a job description and the hire, or
  a single interview result. Not for judging one candidate or a hire's
  performance.
---

# hiring-retrospective

**When to use:** A search ended (hire, cancellation, reset) or has run long enough to learn from, and the team wants to know what to change before the next similar search.

**When not to use:** Reading one candidate (use candidate-assessment); writing a new profile from scratch (use role-requirements); reviewing the hire's job performance; triaging a live pipeline.

## Purpose

Find where the process gave a slow or wrong signal, and turn that into a few small changes for next time. The outcome is the ground truth: the person hired, or the person the team said yes to. The retro measures the gap between the plan (the requirements and the process) and that outcome. It looks at steps and records, not at people. Assistive only: findings and suggestions are a draft for the recruiter and hiring team to accept or drop.

## Inputs

Use whatever exists. Mark what is missing; never fill a gap with a guess presented as fact.

- **Requirements:** the job description, intake notes, a role-requirements profile, and every later revision with its date.
- **Outcome anchor:** who was hired or said yes to, and why. For a search with no hire: the strongest finalist and why they left the process. With a single interview result: that interview's decision.
- **Interview results:** scorecards, screen notes, debrief notes, written rejection reasons.
- **Candidate list:** stage reached and exit reason per candidate (team rejected, candidate declined, withdrew, no reply).
- **Dates:** search opened, requirements agreed or changed, each candidate's entry and stage moves, interviews, feedback recorded, offer, acceptance.
- Optional: a 90-day signal (did the hire reach the first outcomes?), used only to test whether the requirements predicted the outcome, not to rate the hire.

Keep candidate data minimal. Replace names with labels (C1, C2) and keep only stage, dates, and the evidence line that matters.

## Input tiers

Name the tier at the top of the report. Every finding carries a confidence: **high** (two or more independent records, or a pattern across many candidates), **medium** (one record, or a small sample), **low** (one data point or an inference; treat it as a hypothesis to test next search).

| Tier | What you have | Can conclude | Cannot conclude |
|---|---|---|---|
| A, full | Candidates with stages, interview results, timestamps | Requirement fit, interview signal, pass-through rates, stage waits, time to first good candidate | Whether the requirements predicted results, unless a 90-day signal exists; never the hire's quality |
| B, partial | Some of the above: interviewed set without dates, or dates without interview notes | Requirement fit for the interviewed set; whichever of signal or timeline the data covers | Funnel rates; anything about stages with no record |
| C, minimal | A job description and the hire, or a single interview result | Low confidence only. With a hire: Did not matter and Missing. With a single interview result: Missing only | Patterns, rates, timelines, Held, Drifted, Misweighted, the underrated and overrated lists |

## Procedure

Tier B: skip whichever of steps 2, 5 and 6 have no records. Tier C: skip steps 2, 5 and 6; run step 3 (Tier C tags only) and step 4 (single-interview path only).

1. **Scope.** State what ended, the outcome anchor, the tier, and the one question the team most wants answered, if stated; otherwise use: what most delayed reaching the outcome anchor?
2. **Rebuild the timeline.** List dated events as days from search open (Day 0): requirements agreed, each revision, first candidate shown, first candidate the team advanced, hire entered pipeline, interviews, feedback, offer, acceptance. Prefer written records over memory, and mark inferred dates.
3. **Requirements against the outcome.** Put the requirements (or a reconstructed profile built with role-requirements, marked reconstructed) beside the hire and the interviewed set. Tag each requirement:
   - **Held:** the hire met it, and it separated advanced candidates from rejected ones.
   - **Did not matter:** the hire lacked it, the team waived it, or every candidate had it (every candidate having it may still mean a valid floor).
   - **Missing:** a reason that decided outcomes in debriefs or rejections, but no requirement named it.
   - **Drifted:** it changed during the search. Note when, why, and whether the change was written down.
   - **Misweighted:** the right idea at the wrong tier (required vs preferred, or whatever tiers the profile uses).
   Tier C: low confidence only. With a hire, Did not matter and Missing. With a single interview result, Missing only.
   Then check two lists. Underrated: candidates the team liked who fit the written requirements poorly. Overrated: candidates who fit on paper and were rejected, especially several for the same reason. Name the requirement behind each. Use existing reads; do not re-assess candidates.
4. **Interview signal.** For each stage with results: did it record evidence tied to a requirement, or only an impression? Did a yes at this stage predict the final decision? Look for repeated checks of the same thing, knockouts found late that an earlier step could have caught, missing or late feedback, and disagreements settled by time pressure. With one interview result, name the requirement the decision turned on, whether the profile had it, and whether a resume or screen could have shown it earlier.
5. **Funnel.** Count candidates per stage and compute pass-through only on candidates who finished a stage; leave active ones out. Under about 20 candidates, lead with patterns, not percentages. Group exit reasons. A pass rate near 0% or 100% is a flag: check whether the stage, the candidate pool or the requirement is the cause. Compare where volume came from with where the hire came from.
6. **Timeline.** Compute what the dates allow: time to agreed requirements, time to first candidate shown, time to first good candidate (the first one the team advanced past screen), time to hire (hire entered pipeline to acceptance), time to fill (search open to acceptance), and feedback lag per stage. Find the longest wait that was not the candidate's choice. If the hire entered late, assess, as a low-confidence hypothesis, whether the final requirements written on Day 0 would have surfaced the hire sooner.
7. **Suggestions, at most 3.** Each one is a single concrete change: a requirement edit with its tier, an intake or interview step, or a timing rule. Tie it to finding numbers, give its confidence, and say how the next search will show it worked. Prefer the requirement edit that explains the most rejections and the fix for the longest wait. Add one or two lines on what worked, so the team keeps it.
8. **Blameless pass and hand-off.** Rewrite any line that faults a person so it names the step or the missing record instead. Requirement edits feed role-requirements for the next similar search; do not edit a live profile from this skill.

## Output

1. **Header:** outcome, tier, records used, records missing.
2. **Timeline:** one table of Day N events, if any dates exist.
3. **Findings:** numbered, each with confidence and evidence, grouped by requirements, interview signal, funnel, timeline.
4. **Suggestions:** at most 3, as in step 7.
5. **Keep:** what worked.
6. **To learn more next time:** the one record that would have raised confidence most.

## Worked synthetic example

**Search (synthetic):** Battery Test Engineer at Example Battery Co. (fictional). Tier B: candidate list with stages and dates, interview notes for the final four, no post-hire data. Requirements: 5+ years; cell design experience (required); Python test automation (preferred).

**Timeline:** Day 0 search opens. Day 21 first candidate shown. Day 30 hiring manager says "we want bench testers, not designers" in a call; the profile is not updated. Day 44 hire (C7) enters. Day 58 team interview. Day 66 feedback recorded. Day 75 offer accepted.

**Findings:**
1. Drifted, high: the Day 30 shift to bench testing was never written into the requirements, and sourcing kept matching design profiles for two more weeks (call note plus the next six candidates shown).
2. Did not matter, medium: C7 had no cell design work and was hired. Two of three team-interview rejections read "designer, not hands-on."
3. Missing, medium: hands-on bench work decided every final-round outcome, but no requirement named it.
4. Misweighted, low: Python test automation was preferred, yet it was the strongest line in C7's debrief. A low-cost hypothesis: make it required next search and see whether it separates finalists.
5. Timeline, medium: 8 days of feedback lag after the team interview was the longest wait not caused by a candidate.

**Suggestions:**
1. Replace "cell design experience (required)" with "hands-on cell or pack testing at the bench (required)". Evidence: 1 to 3. Confidence: medium. Check: next search, most team-interview rejections cite a written requirement.
2. When the hiring manager changes the bar, update the written requirements the same day. Evidence: 1. Confidence: high. Check: no gap between a stated change and the profile.
3. Agree a 2-business-day feedback rule at intake. Evidence: 5. Confidence: medium. Check: feedback lag per stage in the next retro.

**Keep:** the team interview gave specific, requirement-level reasons.

**To learn more next time:** a 90-day check against the first outcomes.

**Tier C variant:** with only the job description and C7's resume, the retro reports one finding: C7 had no cell design work and was hired (did not matter, low). To learn more next time: the final-round rejection reasons and dates, which would show whether cell design separated candidates and when the bar moved.

## Failure modes / edge cases

- Generic advice ("communicate better") with no link to a record from this search.
- Percentages on a handful of candidates presented as firm.
- Reading a search with no hire as a sourcing failure when the requirements kept moving.
- Calling a late hire bad luck before checking when the requirements caught up with what the team wanted.
- Blaming selection for a problem that started at intake, or that came from a business change mid-search.

## Forever don'ts

- Never judge a candidate's worth, or re-decide a hire or rejection.
- Never name or fault an individual interviewer, recruiter or manager; describe the step.
- Never invent dates, counts, reasons or feedback; mark them missing.
- Never contact candidates or edit live requirements from this skill.
- No numeric scores or weights; no production scoring internals.
- Synthetic examples only; no real candidate or client names.

## Provenance

Adapted from blameless postmortem practice (Google SRE book; Etsy Debriefing Facilitation Guide) and a coding-session retro skill (retro in mattpocock/skills: every finding traced to a record, proposals only). Funnel and time definitions follow published ATS documentation and SHRM. Composes with role-requirements and candidate-assessment.
