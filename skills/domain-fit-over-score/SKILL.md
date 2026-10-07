---
name: domain-fit-over-score
description: "Flag mid/low assistive scores when title+company scream domain fit on specialized eng roles; human dig-deeper only."
---

# domain-fit-over-score

**When to use:** A specialized eng role (sensors, characterization, controls, embedded) where title+company scream domain fit but the assistive score/rank draft sits mid or low, and keyword screens are likely missing hands-on people.

## Purpose

Flag candidates for **human dig-deeper** when domain signals from title and company outweigh a mid/low assistive score. Keyword filters fail on specialized eng; this playbook registers a human-review pass. It is not a scoring override, not a Pairwise production change, and not an agent that hires for you.

Score/rank language here means **assistive drafts for human review** only.

## Inputs

- Candidate summary cards: title, company, location, assistive score/rank draft (from board or MCP funnel-read)
- Role domain tags (e.g. sensors, characterization, controls, fixture design)
- Optional: ideal/anti persona cards from `ideal-anti-persona` (synthetic exemplars in public copy)
- Explicit note of what the keyword screen already filtered on

## Outputs

- Flag list: mid/low-score cards with strong title+company domain signals
- Per-flag human-review note (2-4 sentences: why dig deeper, what to verify in UI/PDF)
- Assistive re-order sketch for the recruiter board (draft only)
- Reason tags for the loop log (e.g. `title-company-fit`, `keyword-miss`, `persona-match`)

## Procedure

1. Load the role's domain tags and, if available, the current ideal persona signals.
2. Scan the stage (or imported shortlist) for titles/companies that match domain tags **despite** mid/low assistive score. Do not invent resume bullets from titles alone.
3. Spot generic keyword misses: e.g. "Test Engineer" at a sensor/char lab when the JD says "Characterization"; "Controls" at a robotics OEM when the JD says "Motion Planning" only.
4. For each candidate worth flagging, write a short dig-deeper note:
   - Evidence allowed: title, company, location, fields already on the application card
   - Evidence forbidden here: invented metrics, invented ship claims, guessed PDF contents
5. Tag the flag with a reason code. Hand the list to a human reviewer. Do not auto-promote, auto-reject, or rewrite Pairwise scores.
6. Log the human outcome: advanced to review/share, passed with reason, or discarded as false positive. Feed Loop 1.

## Worked synthetic example

**Role tags:** sensor characterization, fixture design, mixed-signal  
**Assistive board (synthetic):**

| Name (fake) | Title | Company | Assistive draft | Flag? |
|-------------|-------|---------|-----------------|-------|
| Alex Rivera | Test Engineer | Northlake Sensing Labs | Mid | Yes - test eng at sensing lab often means char work; dig into fixture/excitation in UI |
| Jordan Lee | Characterization Engineer | Generic SaaS Co | Mid | No - title matches keywords but company is off-domain |
| Sam Okonkwo | Hardware Engineer | Coastal Robotics | Low | Maybe - only if persona likes HW generalists who touched sensors; else skip |

**Human-review note (Alex):** "Title+company suggest hands-on sensor test at a char-oriented lab. Assistive score mid; likely keyword miss on 'characterization'. Open PDF in Pairwise UI; ask last fixture + metrics if advanced. Do not invent char experience from the title."

**Outcome log (synthetic):** Human advanced Alex to review (`title-company-fit`). Jordan not flagged. Sam discarded (`weak-company-signal`). One advance from two flags → log for Loop 1.

## Failure modes / edge cases

- **Title cosplay:** Fancy titles at off-domain companies. Require company-type signal, not title alone.
- **Invented resume:** Writing "characterized IMUs for two years" when the card only says Test Engineer. Stop; open UI/PDF.
- **Flag spam:** Flagging everyone mid-score. Cap to strong domain tags; quality over volume.
- **Score-override language:** "Raise the score" or "Pairwise got it wrong" in client-facing notes. Use dig-deeper / human review wording only.
- **Empty evidence:** No title and no company on the card. Do not flag; ask for a fuller application read via `mcp-funnel-read` + UI.

## Forever don'ts

- Do not teach or imply gaming Pairwise assistive scores.
- Do not claim these skills power Pairwise production scoring.
- Do not invent resume, metrics, or ship claims from titles alone.
- Do not auto-hire, auto-screen-out, or speak as agents that hire for you.
- No real UUIDs, PII, or named-client exemplars in public copy.

## Measure this loop

**Loop 1 - Domain-fit rescue** (see `docs/LOOPS_AND_METRICS.md`).

- Primary: near-miss / domain-fit flags that led to human advance (count + reason tags).
- Also: draft accept / edit / reject rate on the flag notes.
- Sample floor before skill patch: ~20 flagged cards on one role family.
- Write-back: recurring false-positive reason tags → update domain-signal examples in this file (human-approved).
