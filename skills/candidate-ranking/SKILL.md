---
name: candidate-ranking
description: >-
  Rank a list of candidates for one role into a short slate to present to the
  hiring manager or client: hard gates first, then fit, candidate quality,
  vetting and location in strict order, with a reason, a named risk and a
  confidence for every rank. Use when a recruiter asks "who are the best ones
  to send?", wants a shared pack ordered, or needs a top 3-5 from a longer
  list. Works for any role and employment model. Not for reading one
  candidate in depth (use candidate-assessment) or deciding who to contact.
---

# candidate-ranking

**When to use:** A recruiter has several candidates for one role and must pick and order the few to present, or order a pack already shared.

**When not to use:** Building the role profile (role-requirements); a deep read of one person (candidate-assessment); outreach (candidate-outreach).

## Purpose

Turn per-candidate reads into an ordered slate the hiring manager will want to act on, with the reasoning visible so a human can check and change it. Assistive only: the rank is a draft for the recruiter, never a hire, reject or send decision.

## Inputs

- **Requirements profile** from role-requirements, with its version or date. Rank against the current one.
- **Per-candidate evidence:** resume, profile, screen transcripts or scorecards, recruiter notes. A candidate-assessment read per person is best.
- **Engagement facts:** comp band, location and on-site days, work-authorization rules, client-agreement rules (non-solicit, submission ownership).
- Optional: any tool match score (a tiebreaker only); **client calibration notes** (past feedback on earlier shares, kept per client, separate from this skill); submission history for this client.

## Outputs

- **Gate report:** every candidate who failed a gate, and which one. No one drops off silently.
- **Ranked slate** (usually 3-5), then a **not recommended** list with one line each.
- **Gaps:** missing evidence that would change the order.
- **Send snapshot:** order, reasons, confidences, requirements version, date.

## Procedure

1. **Hard gates, before any ranking.** Fail = out of the slate, listed in the gate report:
   - Current employee of the hiring company, or inside a non-solicit or cooldown.
   - Already submitted to this client, by you or another agency (conflict).
   - Misses a Critical must-have on the evidence. Unknown is not a miss: missing evidence goes under Gaps with low confidence.
   - Work authorization the role truly requires (confirm the rule; a stated preference is not a gate).
   - On-site location the candidate cannot meet and will not relocate for.
   - Comp ask above a hard cap the client stated. Without a stated cap, comp outside the band is a named risk.
2. **Verify the facts you will rank on.** Use the resume, transcript or the candidate's own statement. Public profiles and inferences are lower confidence. Merge or separate same-name duplicates before going on.
3. **Place each candidate on each factor,** in this order, as tiers (strong, adequate, weak), not numbers:
   1. **Fit:** experience and skills against the must-haves. Discount relevant work that is old (stale for this field) and recent drift away from the work (moved into management, founding, sales, compliance). A preferred tool is a plus unless the profile makes it a must-have.
   2. **Quality:** strength of schools and previous employers, and the scope of work done there.
   3. **Vetting:** completed a screen or interview and did reasonably well per the transcript or scorecard. A screen for a different role, or one older than about 90 days, is partial. None is unvetted.
   4. **Location:** in the preferred metro, then commutable, then relocating.
4. **Order lexicographically.** A lower factor decides only when the candidates share the same tier on every higher factor. A brand-name employer does not outrank better fit.
5. **Break remaining ties** with, in order: interest and availability (engaged, notice period, competing offers), level fit (not under or over the role), comp fit, evidence strength, then any tool match score.
6. **Name one risk per candidate:** over-level, comp ask vs band, work authorization to confirm, commute, flight-risk tenure pattern, thin vetting, padded-resume signals, competing offer. No reason and no risk, no rank.
7. **Check the slate as a set.** Give the client real choice; if two are near-duplicates, keep the stronger and note the other as a backup. Use calibration notes to check the slate against profiles the client advanced or rejected before.
8. **Order-bias check.** Rank a second time from a shuffled list. If the top 3 differ, settle them with head-to-head comparisons and say you did.
9. **Optional second ranker** for client-facing packs: an independent ranking from the same inputs, blind to the first. Send top-3 disagreements to the recruiter with both reasons.
10. **Write the output, run the pre-send checklist, freeze the snapshot.** Save it with the pack (a file or an ATS note) before it is shared. Never edit it afterward; add a dated note instead. Stop; a human decides what goes to the client.

## Per-candidate format

`rank N: <name>` (confidence: high / medium / low)
- **Confidence:** high = every ranking fact verified; medium = one or more inferred but fit verified; low = fit itself inferred.
- **Why:** one line on fit, then quality.
- **Vetted:** yes, partial or no, with the evidence (date, which role, how it went).
- **Location:** metro, and commute or relocation stance.
- **Risk:** the one that most threatens this placement; others after it.

## Pre-send checklist

- Every gate failure is listed with its gate.
- Each fact the client will see is checked against the resume or transcript.
- Comp asks and work authorization are confirmed, not assumed, for every slate member.
- Thin vetting is said plainly; low-confidence ranks are flagged.
- The comment the client will see carries the why, not only the name.

## Measuring

- Per pack, track: top-3 hit rate (share of your top 3 the client advanced); rank agreement with the furthest stage each candidate reached (for example, Kendall tau); interview-to-offer and offer-accept by rank.
- Map each client rejection reason to the factor or gate that should have caught it.
- Do not change this skill's order from one pack. Change it only after about 5 packs or 20 candidates point the same way. One-client lessons go in that client's calibration notes.
- Feed the snapshot and metrics into hiring-retrospective after the search closes.

## Worked synthetic example

**Role (synthetic):** Senior Enclosure Designer at Brightwater Robotics (fictional), on site in Austin, band $130-160K, preferred CAD tool a plus. Requirements v2, Nov 1. Six candidates.

**Gate report:** Lee Park works at Brightwater now (non-solicit). Sam Ortiz was submitted to Brightwater last month by another agency (conflict).

**rank 1: Priya Nair** (confidence: high)
- **Why:** 6 years of sheet-metal and molded enclosures at a top device maker; strong engineering school.
- **Vetted:** yes, screened for this role Oct 28, specific answers on tolerancing.
- **Location:** Austin. **Risk:** asked $165K, just above band.

**rank 2: Tom Reyes** (confidence: medium)
- **Why:** strong enclosure fit at two top-tier employers, uses the preferred tool.
- **Vetted:** partial, screened in June for a different role.
- **Location:** Dallas, willing to relocate. **Risk:** competing offer due next week.

**Not recommended:** Ana Cole, enclosure work ended 2015, now a program manager (stale, drift). Raj Iyer, strong brand but electrical, misses the mechanical must-have.

**Why Priya is above Tom:** both are strong on fit and quality, so vetting decides: a current screen beats a partial one. A shuffled rerun gave the same top 2.

## Failure modes / edge cases

- Ranking on public-profile claims, then repeating them to the client.
- Treating a client preference (citizenship, a tool) as a hard requirement, or ignoring a real one.
- Frozen snapshot missing or edited after send, so outcomes cannot be measured against it.

## Forever don'ts

- Never hire, reject, submit or contact anyone from this skill.
- Never present a current employee of the hiring company or a conflicted submission.
- Never invent experience, comp, authorization or interview results; mark them unknown.
- No numeric scores or weights; no production scoring internals.
- No real candidate or client names in shared examples.

## Provenance

Operator-vetted: a recruiting operator's ranking order (fit, quality, vetting, location) used on a live client pack, with lessons from that run (score as tiebreaker, partial vetting, comp and authorization risks, drift and staleness, duplicates, non-solicit) and reviewer additions (gates, same-tier ordering, order-bias check, measurement); QUALITY_BAR; not a bulk AI pack.
