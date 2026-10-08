---
name: role-assessment
description: >-
  Break a job down into a weighted requirements profile across seven axes
  (domain, skills, hands-on depth, employer and product background, education,
  eligibility, comp and level) before judging candidates. Use when opening a new
  search, when hiring-team feedback changes the bar, when scores or rankings
  disagree with the team's picks, or before running candidate-assessment. Not
  for writing the public job post or scoring a pipeline by itself.
---

# role-assessment

**When to use:** A recruiter has a job (description, intake notes, hiring-manager input) and needs to know what actually matters, and how much, before reading profiles.

**When not to use:** Writing the public posting; ranking candidates (use candidate-assessment with this profile as input).

## Purpose

Turn a role into a weighted requirements profile that phase 2 (candidate-assessment) can apply the same way to every candidate. The weights shift by role, domain and seniority, so set them per search rather than reusing a template. Assistive only: the profile is a draft for the recruiter and hiring team to confirm, not a screening decision.

## Inputs

- Job description and any intake or kickoff notes.
- Hiring-manager or team feedback (the newest input wins over the original description; note the conflict).
- Engagement facts: contract or FTE, client, site and on-site days, comp range or rate, duration.
- Optional: profiles the team already liked or rejected, with the reasons. These calibrate the weights better than the description.

## Outputs

- **Weighted requirements profile:** one row per axis with must-have, strong-plus and not-required items, a weight (summing to 100), and that axis's knockouts.
- **Knockout screen questions:** 3-5 questions a recruiter can ask in a first call that separate real hands-on experience from vocabulary.
- **Open questions** for the hiring team, where the inputs conflict or are silent.

## Procedure

1. Gather inputs. If on-site days, engagement type or comp range is missing, ask once and mark it open.
2. Work each axis. For every item, mark must-have, strong-plus or not-required, and say why.
   1. **Domain knowledge.** What the person must already understand about the product or physics, and whether a nearby domain transfers (for example, one sensor type to another).
   2. **Skills.** List them and rate each critical, important or nice. For each, say whether the exact skill is required or an adjacent or related one is enough (another scripting language, another instrument family).
   3. **Hands-on depth.** For each core skill, the level needed: owner (designed and ran the work, wrote the report), coordinator (directed others, compiled results) or exposure. Say which level is a must.
   4. **Employer, project and product background.** The company types, teams and products that produce this experience at the right pace and constraints, and how much it matters next to direct evidence.
   5. **Education.** The realistic bar, for example a PhD plus 0-2 years versus a Master's plus 3-5 years. Name what must accompany the degree to be useful (bench time, industry exposure). Decide whether strong education learns the gap quickly or the role is experience-heavy. For PhD-heavy roles, name the 3-5 standout labs or research groups that feed the field.
   6. **Eligibility.** Contract cooldown per the client's agreement (often about 6 months); the client's current employees are not candidates, because an employee will not or cannot take a contractor seat; former client contractors past the cooldown are eligible and often motivated to return; location and on-site days; work authorization and sponsorship.
   7. **Comp, scope and level.** Probable comp range and structure (base, bonus, equity, rate), the actual responsibilities, and the level they map to on a typical career ladder. This lets phase 2 judge whether a candidate sees the role as a step up or a step down.
3. Set weights. Start even, then move points toward the axes that best predict success in this search. Rules of thumb: senior or specialist roles weight hands-on depth and domain; early-career roles weight education and skills; contract roles weight eligibility and level fit higher, because they fail late and quietly. Eligibility items are knockouts, not points.
4. Write knockouts per axis: a short list of findings that end the evaluation (client employee, inside cooldown, no work authorization with no sponsorship, missing a true must-have).
5. Write 3-5 knockout screen questions. Each asks for a specific part, method or result, so a real answer is concrete.
6. List open questions and send the profile to the recruiter or hiring team to confirm before phase 2.

Per-axis sub-skills may split out later (for example, a dedicated education-bar or comp-level skill). Keep the axis names stable so they can.

## Worked synthetic example

**Role (synthetic):** Sensor characterization engineer, contract via a staffing partner, at Northwind Devices (fictional consumer wearables OEM), on site 3-4 days, rate equivalent to about $140-180K annualized, no equity. Team feedback: they need people who have handled MEMS parts on a bench, and they have rejected candidates who only knew the noise vocabulary.

| Axis | Must-have | Strong-plus | Not required | Weight |
|---|---|---|---|---|
| Domain | Hands-on MEMS with a moving mass (inertial or pressure); any proof-mass device transfers | Consumer-volume parts | Optical or thermal sensors as the main domain | 30 |
| Hands-on depth | Owner of characterization: test plan, data, report | Board bring-up, register-level setup | Coordinator-only history | 25 |
| Skills | Noise statistics (distributions, noise density, spectra); intermediate scripting for analysis | Instrument automation | Allan-variance vocabulary, rate-table expertise, FEA | 15 |
| Employer/product | Device maker or sensor supplier | Wearables, phones, headsets | Navigation-grade aerospace | 10 |
| Education | Master's in EE, ME or physics with bench work | PhD from one of 3-5 inertial-MEMS groups (named in the real profile; placeholders Lab A-D here) | PhD as a gate | 10 |
| Comp/level | Mid to senior IC; comfortable at the stated rate | Willing to relocate | Manager or principal-level scope | 10 |
| Eligibility | Not a current client employee; past cooldown; authorized to work | Local | (knockout only) | gate |

**Knockouts:** current Northwind employee; inside the cooldown; no work authorization (this seat does not sponsor); no hands-on moving-mass MEMS at all; manager-only scope with no bench work in years.

**Why the weights shifted:** domain transfer dominates because the team's past picks show it hires on proof-mass experience over vocabulary. Level fit gets more than usual because a contract seat with no equity loses senior people late. Allan-variance-style terms are not a knockout. A Master's is enough because the work is bench-heavy, not research.

**Knockout screen questions:** How do you measure and report a sensor's noise density? How do you bring up a digital MEMS part, and what do you set first? Have you personally run a rate table or thermal chamber, on what part, and what did you extract?

## Failure modes / edge cases

- Copying the job description's wish list into must-haves; nothing is weighted, so every candidate looks the same.
- Treating vocabulary as a knockout when the team cares about hands-on evidence.
- Forgetting eligibility until late, then losing an offer to a cooldown or a client-employee rule.
- Setting an education bar higher than the work needs and filtering out strong practitioners.
- Ignoring comp structure (bonus, equity) so phase 2 misreads level fit.

## Forever don'ts

- Never present the profile as a hire or reject decision; it is a draft for human confirmation.
- Never contact candidates or send outreach from this skill; it only produces the profile.
- Never treat a current client employee as a candidate.
- Never invent role facts, comp or team feedback; mark gaps as open.
- No real candidate or client names in shared examples; no production scoring internals.
- No assistant-specific channels, repos or IDs in the recipe.

## Provenance

Operator-vetted: a recruiting operator's own role-breakdown framework (seven axes, per-search weighting, eligibility rules for contract seats), used on live hardware engineering hiring loops and portability-scrubbed for this repo; QUALITY_BAR; not a bulk AI pack.
