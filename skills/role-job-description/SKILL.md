---
name: role-job-description
description: >-
  Write a public job description from a confirmed role-requirements profile:
  mission and outcomes in plain language, required vs preferred clearly
  separated, and no extra gates the profile did not confirm. Use when a
  recruiter needs a posting draft, a rewrite of a bloated or inaccurate JD,
  or a check that the live post still matches the current profile. Works for
  any role and employment model. Not for building the requirements profile
  itself (use role-requirements).
---

# role-job-description

**When to use:** A recruiter has a confirmed or draft role-requirements profile and needs a public job description, or the live posting no longer matches the profile.

**When not to use:** Building or revising the requirements profile (use role-requirements, or role-requirements-tuning when feedback changed the bar); reading a candidate.

## Purpose

Turn the internal profile into a posting a good candidate can recognize themselves in, without inventing must-haves or narrowing the role to one example tool, product or title. Assistive only: the draft is for a human to edit and post, never published from this skill.

## Inputs

Use whatever exists. Mark unpublished or unconfirmed facts as open rather than guessing.

- **Requirements profile** from role-requirements, with its version or date. This is the source of truth.
- Any existing posting or intake blurbs.
- **Employment model** and which logistics may be published: location and on-site days, comp range or structure, duration for contracts, work-authorization language the hiring team has approved.
- Optional: tone or length constraints from the hiring team; a matching `domain-<field>-*` skill for how the field talks about the work (not for adding new gates).

## Outputs

- **Draft job description:** title, a short about-the-role section, what the person will do (tied to first-year outcomes), required qualifications, preferred qualifications, and logistics that were approved to publish.
- **Trace notes:** each required line mapped to a profile must-have; any existing-post line that was dropped or rephrased, and why.
- **Open questions:** facts the hiring team must confirm before the post goes live (comp, sponsorship, on-site days, title).

## Procedure

1. **Start from the profile, not the old posting.** If only a posting exists, say the draft is unconfirmed and list the profile questions still open. Do not treat a wish-list JD as already confirmed.
2. **Lead with the work.** Open with why the role exists and the first-year outcomes, in plain language. Task lists come after, and only as examples of that work.
3. **Required vs preferred.** Required lines come only from confirmed Critical or High must-haves. Preferred tools, titles, employers, degrees and "nice to have" years stay preferred unless the profile makes them knockouts. A preferred item never silently becomes required.
4. **Do not invent or over-narrow.** If the profile names an adjacent domain that transfers, the posting should not read as if only one product, tool or title counts. Leave out must-haves the profile marked open or not-required.
5. **Publish only confirmed logistics.** Location, on-site expectations, comp, authorization and contract length appear only in the form the hiring team approved. If a fact is still open, omit it or use the agreed placeholder, and list it under Open questions.
6. **Check the draft against the profile.** Every required line traces to a must-have. No required line is stricter than the profile. Where the old posting disagreed with the profile (see role-requirements "JD disagreements"), the new draft follows the profile.
7. Stop. A human edits and posts. If later feedback changes the bar, run role-requirements-tuning first, then come back to this skill.

## Worked synthetic example

**Role (synthetic):** the Fernvale mid-market Account Executive profile from role-requirements (fictional). Agency direct-hire through Ridgeway Talent (fictional). Hybrid, 2 days a week in Denver. OTE about $150K, 50/50. Requirements v2. The old posting asked for "5+ years enterprise sales" and named one CRM as required. The hiring team has approved publishing Denver hybrid, 2 days on-site, and "competitive OTE"; it has not approved a number.

**Title:** Mid-Market Account Executive

**About the role:** Grow mid-market revenue for Fernvale in the Mountain region. In the first year you will close early deals in the territory, build a qualified pipeline and reach full quota.

**What you will do:** run full-cycle sales to finance and HR buyers; build and forecast your own pipeline; work in a small team with a hands-on manager, in Denver two days a week.

**Required:** experience closing software deals as the named seller; 2+ years carrying a quota; comfort selling to finance or HR buyers; able to work in Denver two days a week; authorization to work in the US (no sponsorship stated).

**Preferred:** payroll or HR tech; mid-market experience; any CRM.

**Logistics:** Hybrid, Denver, two days on-site. Competitive OTE (50/50 plan discussed in process).

**Trace notes:** "5+ years enterprise" and the named CRM were dropped because they contradict the profile. "Closed deals as the named seller" stays; years of quota follow the profile (2+), not the old post.

**Open questions:** may a number for OTE be published later?

## Failure modes / edge cases

- Copying a bloated posting and only polishing the prose, so invented must-haves stay in.
- Turning a preferred tool, title or degree into a required line.
- Narrowing the role to one example product or tool, then wondering why the applicant pool is tiny.
- Publishing comp, sponsorship or on-site rules the hiring team did not approve.
- Writing the JD before the profile exists, then treating the JD as the bar.

## Forever don'ts

- Never post, syndicate or auto-publish a job description from this skill.
- Never invent requirements, comp, location or authorization language.
- Never make a preference look like a knockout.
- No numeric candidate scores or production scoring internals.
- No real candidate or client names in shared examples.

## Provenance

Operator-vetted: a recruiting operator's method for writing and correcting postings from a confirmed requirements profile (required vs preferred, no invented gates, no over-narrowing, publish only approved logistics), used on live searches and generalized to any role; outcome-first framing draws on `docs/SOURCES.md`; QUALITY_BAR; not a bulk AI pack.
