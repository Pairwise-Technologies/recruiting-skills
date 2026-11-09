---
name: candidate-ranking
description: >-
  Rank a list of candidates for one role into a short slate for the person who
  decides (a hiring manager, client or panel): engagement gates first, then
  fit, track record, vetting and location in strict order, with a reason, a
  named risk and a confidence for every rank. Use when a recruiter asks "who
  are the best ones to send?", wants a shared slate ordered, or needs a top
  3-5 from a longer list. Works for any role and employment model. Not for
  reading one candidate in depth (use candidate-assessment) or outreach (use
  candidate-outreach).
---

# candidate-ranking

**When to use:** A recruiter has several candidates for one role and must pick and order the few to present. For reviewing a slate already presented against new evidence, use candidate-shortlist-review instead.

**When not to use:** Building the role profile (role-requirements); a deep read of one person (candidate-assessment); outreach (candidate-outreach).

## Purpose

Turn per-candidate reads into an ordered slate the decision maker (hiring manager, client or panel) will want to act on, with the reasoning visible so a human can check and change it. Assistive only: the rank is a draft for the recruiter, never a hire, reject or send decision.

## Inputs

- **Requirements profile** from role-requirements, with its version or date. Rank against the current one.
- **Per-candidate evidence:** resume, profile, screen transcripts or scorecards, recruiter notes. A candidate-assessment read per person is best.
- **Engagement rules:** comp band, location and on-site days, work-authorization rules, and any restrictions from the employment model (non-solicit or cooldown, prior-submission ownership, internal-candidate policy).
- Optional: any tool match score (a tiebreaker only); **calibration notes** (past feedback from this decision maker on earlier slates); submission history for this role.

## Outputs

- **Gate report:** every candidate who failed a gate, and which one. No one drops off silently.
- **Ranked slate** (usually 3-5), then a **not recommended** list with one line each.
- **Gaps:** missing evidence that would change the order.
- **Send snapshot:** order, reasons, confidences, requirements version, date.

## Procedure

1. **Gates, before any ranking.** Fail = out of the slate, listed in the gate report:
   - A restriction in the engagement rules: non-solicit, cooldown, a conflicting prior submission, or the policy on current employees. Apply only the rules the inputs give.
   - Misses a Critical must-have on the evidence. Unknown is not a miss: missing evidence goes under Gaps with low confidence.
   - Work authorization the role truly requires (confirm the rule; a stated preference is not a gate).
   - On-site location the candidate cannot meet and will not relocate for.
   - Comp ask above a hard cap the decision maker stated. Without a stated cap, comp outside the band is a named risk.
2. **Verify the facts you will rank on.** Use the resume, transcript or the candidate's own statement. Public profiles and inferences are lower confidence. Merge or separate same-name duplicates before going on.
3. **Place each candidate on each factor,** in this order, as tiers (strong, adequate, weak), not numbers:
   1. **Fit:** experience and skills against the must-haves. Discount relevant work that is old (stale for this field) and recent drift away from the work (moved into management, founding, sales, compliance). A preferred tool is a plus unless the profile makes it a must-have.
   2. **Track record:** scope, ownership and results of past work at the level this role needs, on evidence. Owned work beats supported work. An employer or school name is not evidence by itself.
   3. **Vetting:** completed a screen or interview and did reasonably well per the transcript or scorecard. A screen for a different role, or one older than about 90 days, is partial. None is unvetted.
   4. **Location:** in the preferred metro, then commutable, then relocating.
4. **Order lexicographically.** A lower factor decides only when the candidates share the same tier on every higher factor. A well-known employer never outranks better fit.
5. **Break remaining ties** with, in order: interest and availability (engaged, notice period, competing offers), level fit (not under or over the role), comp fit, evidence strength, then any tool match score.
6. **Name one risk per candidate:** over-level, comp ask vs band, work authorization to confirm, commute, flight-risk tenure pattern, thin vetting, padded-resume signals, competing offer. No reason and no risk, no rank.
7. **Check the slate as a set.** Give the decision maker real choice; if two are near-duplicates, keep the stronger and note the other as a backup. Use calibration notes to check the slate against profiles this decision maker advanced or rejected before.
8. **Check the order.** If an AI agent ranks, rank again from a shuffled list; if the top 3 change, settle them head to head and say so. For a high-stakes slate, a second ranker can rank blind from the same inputs; send top-3 disagreements to the recruiter with both reasons.
9. **Write the output, run the pre-send checklist, freeze the snapshot.** Save it with the slate (a file or an ATS note) before it is shared. Never edit it afterward; add a dated note instead. Stop; a human decides what goes out.

## Per-candidate format

`rank N: <name>` (confidence: high = every ranking fact verified; medium = one or more inferred but fit verified; low = fit itself inferred)
- **Why:** one line on fit, then track record.
- **Vetted:** yes, partial or no, with the evidence (date, which role, how it went).
- **Location:** metro, and commute or relocation stance.
- **Risk:** the one that most threatens this hire; others after it.

## Pre-send checklist

- Every gate failure is listed with its gate.
- Each fact the decision maker will see is checked against the resume or transcript.
- Comp asks and work authorization are confirmed, not assumed, for every slate member.
- Thin vetting is said plainly; low-confidence ranks are flagged.
- The note the decision maker will see carries the why, not only the name.

## Measuring

- Per slate, track the share of your top 3 the decision maker advanced, how far each candidate got compared with their rank, and interview-to-offer by rank.
- Map each rejection reason to the factor or gate that should have caught it, and feed the snapshot into hiring-retrospective after the search closes.
- Do not change this skill's order from one slate. Change it only after about 5 slates or 20 candidates point the same way. Lessons about one decision maker go in their calibration notes.

## Worked synthetic example

**Role (synthetic):** the Fernvale mid-market Account Executive profile from role-requirements (fictional). Agency direct-hire through Ridgeway Talent (fictional), hybrid 2 days a week in Denver, OTE about $150K (no hard cap stated). Critical: closed full-cycle deals as the named seller. Requirements v2, Nov 1. Seven candidates.

**Gate report:** Marcus Hale works at Fernvale now (current employee, a profile knockout). Jo Brennan was placed by Ridgeway 7 months ago (12-month client-agreement rule). Sam Ortiz has only booked meetings for other sellers and never carried a quota (Critical miss).

**rank 1: Elena Sorensen** (confidence: high)
- **Why:** 3 years closing mid-market HR software deals as the named seller; grew her territory from 6 to 15 accounts.
- **Vetted:** yes, screened for this role Nov 3, named three deals she closed alone.
- **Location:** Denver. **Risk:** asked $160K OTE, just above the band.

**rank 2: Kofi Mensah** (confidence: medium: the region launch is from his public profile, fit is verified)
- **Why:** closes full-cycle deals selling finance software; owned a region from launch.
- **Vetted:** partial, screened in June for an enterprise AE role.
- **Location:** Boulder, commutable. **Risk:** competing offer due next week.

**rank 3: Dana Whitfield** (confidence: low: deal ownership is claimed, not verified)
- **Why:** sells payroll software to finance and HR leads; "142% of quota" has no baseline.
- **Vetted:** no. **Location:** Denver. **Risk:** resume and profile titles disagree.

**Not recommended:** Ana Cole, last carried a quota in 2016, now leads sales enablement (stale, drift).

**Gaps:** Dana has no screen; one on the deals she closed alone could move her up or off the slate.

**Why this order:** Elena and Kofi are both strong on fit and track record, so vetting decides: a current screen beats a partial one. Kofi is above Dana on fit itself: shown in a screen, not only claimed. A shuffled rerun gave the same order.

## Failure modes / edge cases

- Ranking on public-profile claims, then repeating them to the decision maker.
- Treating a preference (a degree, a tool, a work-authorization wish) as a hard requirement, or ignoring a real one.
- Letting employer or school names stand in for track record.
- Frozen snapshot missing or edited after send, so outcomes cannot be measured against it.

## Forever don'ts

- Never hire, reject, submit or contact anyone from this skill.
- Never present a candidate an engagement rule excludes.
- Never invent experience, comp, authorization or interview results; mark them unknown.
- Never rank on prestige or on anything that stands in for a protected trait.
- No numeric scores or weights; no production scoring internals.
- No real candidate or client names in shared examples.

## Provenance

Operator-vetted: a recruiting operator's ranking order (fit, track record, vetting, location) and its lessons from a real search (verify before ranking, partial vetting, comp and authorization as risks, drift and staleness, duplicates), generalized to any role and employment model; gates reuse candidate-assessment's eligibility-first rule; the order check and Measuring are reviewer additions not yet run by an operator; QUALITY_BAR; not a bulk AI pack.
