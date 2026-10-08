---
name: candidate-assessment
description: >-
  Assess one candidate against a weighted role-assessment profile, axis by axis,
  with evidence-backed reads (Ideal, Strong, Unverified, Gap, Major risk) and a
  verdict: interview, knockout screen, pass, or do-not-contact. Use when a
  recruiter pastes a LinkedIn profile or resume and asks "is this person worth
  it?", or wants a profile read before outreach or an interview. Optional short
  summary for one candidate. Not for building the role profile itself.
---

# candidate-assessment

**When to use:** A recruiter has a candidate's profile or resume and a role, and wants a structured read of fit before spending outreach or interview time.

**When not to use:** No role profile yet and no time to build one (run role-assessment first); bulk ranking without per-candidate evidence.

## Purpose

Apply the role's weighted profile to one candidate so the read is consistent, cites evidence, and separates what is verified from what is only claimed. Assistive only: the verdict is a recommendation for a human, never a hire, reject or contact action.

## Inputs

- **Role profile** from role-assessment (axes, weights, must-haves, knockouts, screen questions). If none exists, build it first with that skill.
- **Candidate evidence:** LinkedIn profile, resume, publications, screen notes or transcripts. Note which source each fact comes from.
- Optional operator context: known comp expectations, relocation stance, referral, prior conversations.

## Outputs

- **Per-axis table:** axis, evidence (with source), read, and whether the evidence is verified or claimed.
- **Verdict:** interview, knockout screen, pass, or do-not-contact, with a one-line reason.
- **Verification questions:** one per Unverified item, phrased so the answer is concrete.
- Optional **summary** (phase 3) for a single candidate.
- When the verdict is interview or knockout screen, hand off to the `outreach` skill to draft contact copy for human review.

## Read scale

| Read | Meaning |
|---|---|
| Ideal | Directly matches a must-have, with specific evidence |
| Strong | Matches, or an adjacent skill the profile accepts |
| Unverified | Plausible but claimed, implied by title, or ambiguous |
| Gap | Missing; learnable or covered by another axis |
| Major risk | Likely to sink the hire even if everything else fits |

## Procedure

1. **Eligibility first.** Check the profile's knockouts before reading anything else: current client employee, inside a contract cooldown, work authorization, location and on-site days. A current client employee is do-not-contact. A former client contractor past cooldown is eligible and worth noting as motivated. Stop here on any hard knockout.
2. For each remaining axis, cite the evidence, then assign a read. Mark each fact verified (shown in work product, publications or a screen) or claimed (skills list, headline, summary).
3. **Owner vs coordinator.** For hands-on work, decide whether they designed and ran it or directed, supported or compiled it. Titles like field applications, program, technical lead or "supported customers" default to Unverified until a screen confirms ownership.
4. **Motivation and level fit.** Compare their current level, scope and comp structure (base, bonus, equity) with the role's. Would they see it as a step up, sideways or a step down? Can the seat compete with their career ladder? A manager or designer will rarely take a technician-level seat unless out of work. Flag relocation, and bonus-heavy or equity pay that a contract rate will not replace.
5. Weigh the reads with the profile's weights. A Major risk on a heavy axis outweighs several Strongs on light ones.
6. Pick a verdict: **interview** (must-haves verified, no Major risk); **knockout screen** (promising, but key items Unverified or one Major risk a call can settle); **pass** (missing a true must-have); **do-not-contact** (eligibility knockout).
7. Write one verification question per Unverified item, drawing on the profile's screen questions.
8. Optional phase 3, single candidate only, at the agent's discretion: 3-5 lines of key highlights and lowlights plus the verdict. Leave out the full table and any numbers. When comparing many candidates, stop at step 7.

## Worked synthetic example

**Candidate (synthetic):** Sam Okafor, Principal FAE at Brightmoor Sensors (fictional MEMS supplier), about 15 years of experience, based in another state. **Role:** the Northwind Devices sensor characterization contract from the role-assessment example.

Eligibility: not a Northwind employee, no prior engagement, authorized to work. Clear; continue. Rows follow the profile's axes, split where the evidence differs (hands-on depth becomes reporting, bring-up and characterization).

| Axis | Evidence | Read |
|---|---|---|
| Domain | Consumer IMUs and pressure sensors for the supplier's largest customers (claimed, profile) | Ideal |
| Reporting | Delivered characterization and qualification reports with product, reliability and packaging teams (claimed) | Strong; may have compiled reports rather than generated the data |
| Device bring-up | Schematic and layout reviews, board bring-up, field-return failure analysis (claimed) | Strong |
| Integration knowledge | Wrote internal customer design guides on board layout and part handling (verified, internal) | Strong and rare: board stress and assembly effects |
| Hands-on characterization | Field role: supports customers, coordinates product engineering (claimed, title) | Unverified: owner or coordinator? |
| Scripting (MATLAB/Python) | Not mentioned anywhere; hardware-design heavy (profile silent) | Gap |
| Level and comp fit | Principal, likely paid above the role's ceiling with a large bonus; relocation needed; the seat has no equity (inferred from level and location) | Major risk |

**Verdict:** knockout screen. Domain and integration knowledge are rare, but ownership is unverified and level fit is a major risk. Ask comp expectations early.

**Verification questions:** Which characterization did you personally run, on what part, and what did you extract? What did you use to analyze the data? What total comp and location would make a contract seat worth it?

**Phase 3 summary:** Ideal domain and rare integration depth; strong bring-up. Bench ownership unverified and no scripting shown. Likely a step down on comp and level, with relocation. Screen before interviewing.

## Failure modes / edge cases

- Reading eligibility last and wasting a screen on a client employee or someone inside cooldown.
- Treating a skills list as verified hands-on work, or a field or program title as ownership.
- Ignoring comp structure, so a strong candidate drops out at the offer stage.
- Letting one Ideal axis carry a candidate who misses a heavier must-have.
- Dumping the full table into a summary meant for a quick decision.

## Forever don'ts

- Never hire, reject or contact a candidate from this skill; verdicts are recommendations for a human.
- Never contact a current client employee; never auto-send outreach.
- Never invent experience, comp or motivation; mark it Unverified.
- No real candidate PII or client names in shared examples; no production scoring internals.
- No assistant-specific channels, repos or IDs in the recipe.

## Provenance

Operator-vetted: a recruiting operator's own candidate-read method (eligibility first, evidence per axis, owner vs coordinator, level and comp fit), used on live hardware engineering loops; the worked example is a synthetic example; QUALITY_BAR; not a bulk AI pack.
