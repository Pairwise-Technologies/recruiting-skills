---
name: sourcing-plays
description: "Sourcing plays: near-miss pairs, empty-filter vs empty-pool, employer/problem framing, lab-to-grad."
---

# sourcing-plays

**When to use:** Keyword filters return the wrong people, an empty result set, or a noisy pile. You need deliberate plays: near-miss titles, employer/problem search, lab→grad paths, and a clear empty-filter vs empty-pool diagnosis.

## Purpose

Operator sourcing playbook for specialized eng where boolean search fails. Produce **shortlist drafts** and diagnosis notes for human keep/edit/drop. Augment recruiters; never source-and-hire or auto-message "for you." Guest packs remain web URLs in product; these plays are not MCP writes.

## Inputs

- Role modality / domain tags and known near-miss title pairs
- Current search/filter state (result count, empty vs noisy)
- Optional: imported LinkedIn or lab-affiliate lists (operator-provided; synthetic examples only in public copy)
- Optional: assistive score/rank drafts on imported profiles
- Ideal/anti persona cards when available

## Outputs

- Shortlist drafts labeled by play
- Near-miss pair map for the role
- Employer / problem search angles
- Empty-filter vs empty-pool diagnosis note
- Human-review notes (never auto-add or auto-message)

## Procedure

1. **Diagnose empty vs noisy.** If results are empty, run the empty-filter vs empty-pool check (step 5) before declaring no talent. If noisy, tighten with persona signals, not more random keywords.
2. **Near-miss role pairs.** List titles that boolean treats as identical but operators know differ (e.g. Test vs Characterization, Controls vs Motion Planning, Firmware vs Embedded Linux). Search both sides deliberately; tag each shortlist row with which side it came from.
3. **Employer / problem search.** List employers who ship the problem space and problem statements the seat actually owns. Search those angles, not only JD keywords.
4. **Lab→grads.** Map relevant labs/groups to recent grads or affiliates; draft a shortlist for human outreach decisions.
5. **Empty-filter vs empty-pool:**
   - Empty-filter: constraints too tight (title AND keyword AND location AND seniority). Loosen one axis at a time; log whether candidates reappeared.
   - Empty-pool: loosened filters still empty in this market slice. Escalate to employer/problem or lab plays; do not keep adding synonyms forever.
6. **Modality re-rank / underrated-score rescue.** After import, re-order by modality and persona fit. Flag mid/low assistive scores with strong fit for human dig-deeper (same hygiene as `domain-fit-over-score`). Do not game scores.
7. Hand all drafts to recruiters for keep/edit/drop. Never auto-send (hand off to `draft-for-human-send` if outreach text is needed).

## Worked synthetic example

**Role (synthetic):** Characterization Engineer, IMU / pressure sensors  
**Near-miss pairs:** Characterization ↔ Test; Sensor Design ↔ Sensor Applications; Metrology ↔ Validation  

**Empty result:** Title="Characterization Engineer" AND "IMU" AND "Bay Area" AND "7+ years" → 0 results.  
**Diagnosis:** Likely **empty-filter**. Loosen seniority to 4+ and allow Test Engineer at sensing companies.  
**Recovery (synthetic):** 12 profiles reappear; 4 match persona. Log: empty-filter recovery = yes.

**Employer/problem angles:** employers known for sensor modules and industrial IMUs; problem language "fixture-limited noise floor" / "temp co across lots."  

**Shortlist draft (synthetic, 3 rows):**

| Play | Fake name | Why keep for human review |
|------|-----------|---------------------------|
| Near-miss (Test@sensing) | Riley Chen | Test eng at sensing module shop; dig for char depth |
| Employer/problem | Morgan Patel | Applications eng at IMU vendor; problem-space overlap |
| Lab→grad | Casey Nguyen | Recent grad from a known sensors lab group |

Human keep/edit/drop on these three feeds Loop 4.

## Failure modes / edge cases

- **False empty-pool:** Declaring no talent while title+location+seniority are all maxed. Always test empty-filter first.
- **Synonym soup:** Adding 20 title OR-clauses without persona. Prefer near-miss pairs + employer/problem.
- **Auto-message:** Turning shortlists into sends inside the skill. Forbidden; use draft-for-human-send + human send.
- **Live LinkedIns in public copy:** Use fake names and placeholder links only.
- **Score gaming:** "Find underrated scores to exploit." Wrong frame; dig-deeper flags only.

## Forever don'ts

- Do not publish live LinkedIns or real pipeline candidate IDs.
- Do not teach gaming assistive scores or imply skills power Pairwise production scoring.
- Do not auto-send outreach or claim agents hire/screen for you.
- Guest packs remain web URLs; sourcing plays are not MCP writes.
- No real job UUIDs or ATS deep links in examples.

## Measure this loop

**Loop 4 - Sourcing play → shortlist draft** (see `docs/LOOPS_AND_METRICS.md`).

- Primary: draft accept / edit / reject rate (keep / edit / drop) per play.
- Also: empty-filter vs empty-pool recovery rate; near-miss / domain-fit flags that led to human advance.
- Sample floor: ~5 shortlist drafts per play type; ~10 empty-result incidents before changing the diagnosis checklist.
- Write-back: high keep-rate plays expand in this file; low keep-rate plays get tighter inputs or demoted order (human-approved).
