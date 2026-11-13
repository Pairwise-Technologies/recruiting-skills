---
name: candidate-assessment
description: >-
  Read one candidate against a role-requirements profile, axis by axis, from
  whatever evidence exists (a full file, one resume, a screen transcript, or a
  single paragraph). Returns evidence-backed reads, a separate authenticity
  call, and a verdict with its confidence. Use when a recruiter asks "is this
  person worth it?", wants a read before outreach, or has screen notes to act
  on. Works for any role. Not for building the role profile itself.
---

# candidate-assessment

**When to use:** A recruiter has something about a candidate and a role, and wants a structured read of fit before spending outreach, screen or interview time.

**When not to use:** Building the role profile (use role-requirements); bulk ranking without per-candidate evidence; writing an interview guide.

## Purpose

Apply the role's profile to one candidate so the read is consistent, cites evidence, and separates what happened from what is only claimed. More sources make a stronger read, but a sparse input still gets a useful read with a stated confidence. Assistive only: the verdict is a recommendation for a human, never a hire, reject or contact action.

## Inputs

- **Role profile** from role-requirements. If none exists, build a quick one with that skill first and mark it draft.
- **Candidate evidence, any subset:** resume, LinkedIn profile, list of roles and companies, screen notes or transcript, work samples, a recruiter's paragraph. Nothing is required except some text about the person.
- For a screen or interview transcript, run interview-transcript-review first (coverage, evidence with its basis, interview checks), then use its debrief as evidence here. A quote it marks disputed is not evidence.
- Optional operator context: comp expectations, relocation stance, referral, prior conversations.
- Optional: a matching `domain-<field>-*` skill for field-specific inflation signals and ownership cues.

## Outputs

- **Evidence inventory:** the sources used.
- **Per-axis table:** evidence, its basis (verified, claimed or inferred) and source, and the read.
- **Authenticity call:** Owned, Mixed or Resume-deep, or "not assessable: one source." Kept separate from fit.
- **Verdict** with a one-line reason and a confidence (low, medium, high).
- **What would change this read:** the one extra source worth getting next.
- **Open items:** at most 3 things a screen or reference must settle, stated as what to find out, not as scripted questions.
- Optional **short summary** for a single candidate.

## Read scale

| Read | Meaning |
|---|---|
| Ideal | Matches a must-have, on **verified** evidence |
| Strong | Matches, or an accepted adjacent skill; claimed evidence caps here |
| Unverified | Plausible but claimed, implied by title, or ambiguous |
| Gap | Missing; say whether it is learnable in the time the role allows |
| Major risk | Likely to sink the hire even if everything else fits |

Verified means shown in a work product, a screen, or consistent detail across independent sources. A skills list, headline or summary is claimed.

## Procedure

1. **Inventory the evidence.** List each source. Note which axes it can and cannot speak to.
2. **Eligibility first.** Apply the profile's knockouts. A current employee of the hiring company, or anyone inside a client-agreement restriction, is do-not-contact. Stop on any hard knockout.
3. **Read each axis.** Cite evidence, mark its basis, assign a read. With no evidence for an axis, write "no evidence," not Gap.
4. **Compare sources.** Where two sources cover the same work, list contradictions (dates, titles, scope, tools, results). Make the authenticity call:
   - **Owned:** sources agree, with specific detail on what they did.
   - **Mixed:** some claims hold, some are inflated or contradicted.
   - **Resume-deep:** claims fall apart under a second source or a screen.
5. **Check inflation signals:** results with no baseline; plans or simulations presented as delivered results; team results stated as personal; titles that do not match the described work; skills lists that echo the job description.
6. **Ownership and trajectory.** Did they own the work or support it? Program, field, coordinator or "supported" titles default to Unverified. Read direction of travel, not only level: is their career moving toward this role's work or away from it, and why are they leaving now?
7. **Level, comp and environment fit.** Step up, sideways or step down? Flag relocation, and bonus or equity a new plan will not replace. Read team and environment fit only from real evidence.
8. **Judge transferability** for each Gap: learnable because of adjacent evidence (name it), or not in the time the role allows.
9. **Verdict.** Before a screen: **interview**, **screen first** (promising, key items unverified), **pass** (misses a true must-have), **do-not-contact** (eligibility). After a screen: **advance**, **hold as fallback**, **pass**, or **reference check first** when sources still disagree. A Major risk on a Critical or High axis caps the verdict at screen first or hold. Set confidence from evidence depth: one source is low.
10. Write what would change the read, and up to 3 open items.
11. Optional short summary, single candidate only: 3-5 lines of highlights, lowlights and the verdict. When the verdict is interview or screen first, hand off to candidate-outreach.

## Worked synthetic example

**Candidate (synthetic):** Dana Whitfield, Account Executive at Copperline Payroll (fictional). **Role:** the Fernvale mid-market AE profile from role-requirements. **Sources:** resume, LinkedIn.

Eligibility: not a Fernvale employee, never placed by Ridgeway, Denver-based. Clear.

| Axis (tier) | Evidence (basis, source) | Read |
|---|---|---|
| Ownership depth (Critical) | "142% of quota FY25" (claimed, resume); no quota size or deal count | Unverified: no baseline; team or personal? |
| Domain (High) | Sells payroll software to HR and finance leads (claimed, both agree) | Strong (claimed caps here) |
| Comp and level (High) | Resume: "Account Executive" to 2025. LinkedIn: "Senior AE, Mid-Market" since 2024 | Unverified: titles disagree |
| Skills (Medium) | "Forecasting, MEDDICC, discovery" in skills list, worded like the JD (claimed) | Unverified: echoes JD |
| Team and environment (Medium) | No evidence | No evidence |
| Background (Medium) | B2B SaaS, sales-led (both agree) | Strong |

**Transferability:** mid-market cycle length is a Gap; learnable, because they already sell to finance buyers on shorter cycles.

**Authenticity:** Mixed. Title dates conflict and the headline number has no baseline. Not a red flag alone.

**Verdict:** screen first, confidence low (two self-written sources). Trajectory points toward mid-market, which fits.

**What would change this read:** a screen on which deals they closed alone; a reference if titles still disagree.

**Open items:** quota size and how many deals were theirs alone; when the title changed and what scope came with it; how they run discovery with finance leads.

## Failure modes / edge cases

- Reading eligibility last and wasting a screen.
- Treating a skills list or title as verified, or giving Ideal to a claim.
- Reading each source alone, so contradictions between them go unseen.
- Refusing to read on sparse input instead of lowering confidence.
- Letting one Ideal axis carry a candidate who misses a heavier must-have.
- Turning open items into an interview script.

## Forever don'ts

- Never hire, reject or contact a candidate from this skill; verdicts are recommendations for a human.
- Never contact a current employee of the hiring company; never auto-send outreach.
- Never invent experience, comp or motivation; mark it no evidence or Unverified.
- No numeric scores; no production scoring internals.
- No real candidate PII or client names in shared examples.

## Provenance

Operator-vetted: a recruiting operator's own candidate-read method (eligibility first, evidence per axis, owner vs supporter, authenticity separate from fit, level and comp fit), used on live hiring loops and generalized to any role; draws on `docs/SOURCES.md`; QUALITY_BAR; not a bulk AI pack.
