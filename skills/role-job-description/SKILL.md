---
name: role-job-description
description: >-
  Write a public job description from a confirmed role-requirements profile:
  the work and its outcomes first, a short required list that traces to the
  profile, preferences kept as preferences, and only the sections the inputs
  can support. Use when a recruiter needs a posting draft, a rewrite of a
  bloated or inaccurate post, or a check that a live post still matches the
  profile. Works for any role and employment model. Not for building the
  profile itself (use role-requirements).
---

# role-job-description

**When to use:** A recruiter has a role-requirements profile and needs a public posting, or a live posting may no longer match the profile.

**When not to use:** Building or changing the profile (use role-requirements); reading a candidate.

## Purpose

Turn the profile into a posting a strong candidate can recognize themselves in, without inventing must-haves, narrowing the role to one tool or title, or filling sections with guesses. Assistive only: the draft is for a human to edit and post.

## Inputs

Use whatever exists. Mark anything missing as open rather than guessing.

- **Requirements profile** from role-requirements, with its version or date. It is the source of truth.
- Any existing posting or intake notes.
- **What the hiring team approved to publish:** location and on-site days, pay, benefits, how to apply and by when, an equal-opportunity or accommodation statement, a short company blurb.
- Optional: tone or length limits; a matching `domain-<field>-*` skill for how the field describes the work (never for adding gates).

## Outputs

- **Draft posting** with only the sections the inputs support.
- **Trace notes:** each required line mapped to a profile must-have; each old-post line dropped or reworded, and why.
- **Flags and open questions:** facts the hiring team must supply or confirm before the post goes live, and wording for a human to decide on.

## Procedure

1. **Start from the profile, not the old posting.** If only a posting exists, say the draft is unconfirmed and suggest role-requirements first. A wish-list post is not a confirmed bar.
2. **Pick sections from what you have.** The core is title, about the role, what you will do, required and preferred. Work arrangement, pay and benefits, how to apply, company blurb and an equal-opportunity statement appear only when the inputs supply them. Never fill a section from general knowledge; a missing fact becomes an open question.
3. **Title:** the plain title people search for. No internal levels, codes, slogans or gendered words.
4. **Lead with the work.** Open with why the role exists and the first-year outcomes. Then 4-7 lines of what the person will do, each tied to an outcome.
5. **Keep the required list short and honest.** Required lines come only from Critical or High must-haves and knockouts, and each must be checkable from a resume or a screen. Preferred tools, titles, employers and degrees stay preferred unless the profile makes them knockouts.
6. **Replace proxies with the work behind them.** A years or degree line becomes the outcome it stands for, unless the profile defends the number. Flag age- or background-coded wording ("digital native", "recent graduate", "young team", "culture fit") for a human. Swap hype words ("rockstar", "ninja", "crush") for plain ones; this is a light check, not a lever.
7. **Publish logistics only as approved.** Location, on-site days, pay, sponsorship and contract length appear only in the form the hiring team approved. If no pay range was given, do not invent one; add this flag: "No pay range given. Many places require one in a posting (for example Colorado, California, New York, Washington, the EU). Confirm before you post."
8. **Check the draft against the profile.** Every required line traces to a must-have, and none is stricter than the profile. Where the old post disagreed with the profile, the draft follows the profile. Read it as a strong candidate from an adjacent domain: would they see themselves in it?
9. **Audit a live posting** when asked or after the profile changes: does it match the current profile version, are dates and deadlines current, and does it come down once the role is filled?
10. Stop. A human edits and posts.

## Worked synthetic example

**Inputs (synthetic):** the Fernvale mid-market Account Executive profile v2 from role-requirements (fictional). The old post asked for "5+ years enterprise sales", named one CRM as required, and promised "a young, high-energy team". The hiring team approved: hybrid, 2 days a week in Denver; US work authorization, no sponsorship. No pay, benefits or application details were supplied.

**Title:** Mid-Market Account Executive

**About the role:** Grow Fernvale's mid-market revenue in the Mountain region. In your first year you will close your first deals, build a qualified pipeline and reach full quota.

**What you will do:** run full-cycle sales to finance and HR buyers, from first call to signature; build and forecast your own pipeline; work in a 6-person team with a hands-on manager.

**Required:** closed software deals as the named seller; 2+ years carrying a quota; sold to finance or HR buyers; authorization to work in the US (no sponsorship).

**Preferred:** payroll or HR tech; mid-market experience; any CRM.

**Work arrangement:** hybrid, in Denver two days a week.

**Trace notes:** "5+ years enterprise" dropped: it contradicts the profile, which wants mid-market closers. "2+ years carrying a quota" kept: the profile defends it under comp and level. The named CRM moved to preferred ("any CRM").

**Flags:** "young, high-energy team" removed as age-coded; describe the team by size and pace instead. No pay range given. Many places require one in a posting (for example Colorado, California, New York, Washington, the EU). Confirm before you post.

**Open questions:** pay range and plan structure; benefits; how to apply and by when; whether to add an equal-opportunity statement.

## Failure modes / edge cases

- Polishing a bloated old post, so its invented must-haves survive.
- A preferred tool, title or degree turned into a required line.
- Narrowing the role to one product or tool, then wondering why the pool is tiny.
- Filling pay, benefits or a company blurb with plausible guesses.
- Writing the post before the profile exists, then treating the post as the bar.

## Forever don'ts

- Never post, syndicate or auto-publish from this skill.
- Never invent requirements, pay, benefits, location or authorization language.
- Never make a preference look like a knockout.
- No numeric candidate scores or production scoring internals.
- No real candidate or client names in shared examples.

## Provenance

Operator-vetted: a recruiting operator's method for writing and correcting postings from a confirmed requirements profile (required vs preferred, no invented gates, no over-narrowing, publish only approved logistics), used on live searches and generalized to any role; outcome-first framing and the wording check draw on `docs/SOURCES.md`; QUALITY_BAR; not a bulk AI pack.
