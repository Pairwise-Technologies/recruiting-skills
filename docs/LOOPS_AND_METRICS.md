# LOOPS_AND_METRICS - self-refining experiment spine (v0)

Operator-experiment metrics only. Not Pairwise product analytics. Not production scoring KPIs.

**Frame:** human-in-the-loop self-refining loops. Skills propose; recruiters accept, edit, or reject; measure the loop, not "AI hire rates."

These loops turn skill runs into durable playbook improvements. A human always owns the decision and the write-back.

---

## What a loop is here

1. **Run skill** - operator (or assistive agent) produces a draft flag, shortlist, question, persona patch, outreach draft, or funnel read.
2. **Human decision** - accept as-is, edit, or reject. Record a short reason tag when rejecting or editing.
3. **Outcome logged** - operator notes what happened next (advanced to review, discarded, sent, not sent, filters loosened, etc.). Logged by the operator; this repo does not instrument Pairwise production systems.
4. **Skill / rubric update proposal** - if the outcome teaches something durable, propose a patch to the matching skill file. **Human-approved only** before any public or shared skill body changes.

Metrics below are **assistive / operator-logged**. Do not invent Pairwise production analytics. Do not claim these skills power Pairwise scoring.

---

## Metrics OK publicly (operator-experiment, not product SLAs)

| Metric | Definition (operator-logged) | Feeds |
|--------|------------------------------|-------|
| Draft accept / edit / reject rate | Per skill run: human sent-as-is, edited then used, or rejected | All playbooks + draft-for-human-send |
| Near-miss / domain-fit flags → human advance | Count of flags that led to dig-deeper or advance, plus reason tags | domain-fit-over-score, sourcing-plays |
| Hard-screen coverage | % of role must-haves that have at least one interviewable question | hard-screens-interviewable |
| Empty-filter vs empty-pool recovery | How often loosening filters recovered candidates after an empty result | sourcing-plays |
| Persona refresh cadence | How often ideal/anti cards are patched when client likes/shipped profiles shift | ideal-anti-persona |
| MCP funnel-complete without invent | % of kit sessions that finish summary → list → application without inventing resume/PDF claims or PII | funnel-read (+ session-whoami, job-discovery) |

Optional later (not required for v0): edit distance on accepted drafts; reply rate / screen-pass rate on sourcing shortlists (human-reported only).

---

## Loop 1 - Domain-fit rescue

**Tied skill:** `skills/domain-fit-over-score/SKILL.md`

**Hypothesis:** Mid/low assistive-score candidates with strong title+company domain signals are over-discarded by keyword-shaped boards. Flagging them for human dig-deeper raises useful advances without teaching score gaming.

**Procedure spine:** Domain-fit rescue → human dig-deeper → advance/pass with reason.

**Metric:** Near-miss / domain-fit flags that led to human advance (count + reason tags). Also draft accept / edit / reject rate on the flag notes themselves.

**Sample size guidance:** Log at least 20 flagged cards on one role family before proposing a skill-body patch. Prefer one modality (e.g. sensors/char) per batch so reason tags stay comparable.

**Failure modes:**
- Flags based on title alone with invented resume claims
- Treating flag volume as success (noise)
- Writing score-override language into the skill

**Write-back:** Accepted reason tags and recurring false-positive patterns → update domain-signal examples and failure modes in `domain-fit-over-score.md`. Human-approved only.

---

## Loop 2 - Hard-screen → interviewable Q

**Tied skill:** `skills/hard-screens-interviewable/SKILL.md`

**Hypothesis:** Must-haves that keyword search cannot prove become useful only when each maps to an interviewable question. Interviewer notes then refresh ideal/anti persona signals.

**Procedure spine:** Hard-screen → interviewable Q mapped → interviewer notes back into persona.

**Metric:** Hard-screen coverage (% must-haves with an interviewable Q). Secondary: draft accept / edit / reject rate on the question bank. Notes that change persona feed Loop 3.

**Sample size guidance:** One role's full must-have list per run. After 3+ interviews using the bank, harvest interviewer notes for persona refresh proposals.

**Failure modes:**
- Vague questions that get "yes but useless" answers
- Auto pass/fail from transcript keywords
- Publishing real transcripts as examples

**Write-back:** Questions that discriminated vs questions that flopped → revise question bank and probe depth notes in `hard-screens-interviewable.md`. Durable signals → propose persona patch via Loop 3.

---

## Loop 3 - Ideal / anti-persona refresh

**Tied skill:** `skills/ideal-anti-persona/SKILL.md`

**Hypothesis:** Personas built from client likes and shipped profiles (not JD alone) drift. Refreshing when likes shift keeps screens aligned with what the hiring team actually advances.

**Procedure spine:** Ideal/anti-persona refresh from likes/shipped (synthetic examples in public copy).

**Metric:** Persona refresh cadence (when client likes shift). Also draft accept / edit / reject rate on proposed persona patches.

**Sample size guidance:** Refresh when 3+ new like/pass exemplars contradict the current cards, or on a weekly check if the role is hot. Public examples stay synthetic.

**Failure modes:**
- JD-only personas that ignore client likes
- Real names / LinkedIns in public skill copy
- Treating personas as auto-reject rules

**Write-back:** Approved patch → update ideal and anti cards in `ideal-anti-persona.md`. Cross-link new signals into domain-fit and hard-screen examples when relevant.

---

## Loop 4 - Sourcing play → shortlist draft

**Tied skill:** `skills/sourcing-plays/SKILL.md`

**Hypothesis:** Near-miss pairs, employer/problem search, and empty-filter diagnosis recover candidates keyword filters miss. Measuring keep/edit/drop on shortlist drafts shows which plays earn human time.

**Procedure spine:** Sourcing play → shortlist draft → human keep / edit / drop.

**Metrics:** Draft accept / edit / reject rate (per play). Empty-filter vs empty-pool: how often loosening filters recovered candidates. Near-miss / domain-fit flags that led to human advance (when plays produce rescue flags).

**Sample size guidance:** 5 shortlist drafts per play type before ranking plays against each other. For empty-filter recovery, log 10 empty-result incidents before changing the diagnosis checklist.

**Failure modes:**
- Declaring "no talent" when filters were too tight
- Auto-add or auto-message from shortlists
- Live LinkedIns or real IDs in public examples

**Write-back:** High keep-rate plays and recovery patterns → expand play sections in `sourcing-plays.md`. Low keep-rate plays get tighter inputs or get demoted in the procedure order.

---

## Loop 5 - Draft-for-human-send

**Tied skill:** `skills/draft-for-human-send/SKILL.md`

**Hypothesis:** Short, claim-hygienic drafts raise human send-as-is rate and cut invented-experience edits. Send/no-send stays a human action forever.

**Procedure spine:** Draft-for-human-send → send / no-send (never auto-send).

**Metric:** Draft accept / edit / reject rate (sent as-is / edited / rejected). Optional later: edit distance.

**Sample size guidance:** 15 drafts on one channel (email or LinkedIn) before proposing tone or checklist changes.

**Failure modes:**
- Auto-send or enqueue
- Invented resume claims in the draft
- Real PII in public examples

**Write-back:** Recurring edit reasons → update review checklist and example draft shape in `draft-for-human-send.md`.

---

## Loop 6 - MCP read funnel complete

**Tied skills:** `mcp-session-whoami`, `mcp-job-discovery`, `mcp-funnel-read` (and `mcp-interviews-read` when transcripts are in scope)

**Hypothesis:** Operators who finish the read-only funnel recipe (summary → list → application) without inventing resume/PDF claims produce cleaner handoffs into playbooks.

**Procedure spine:** MCP read funnel complete (summary → list → app) without invented resume claims.

**Metric:** MCP kit: % sessions that finish funnel recipe without PII invent / PDF invent.

**Sample size guidance:** 10 kit sessions per operator cohort before changing funnel-read failure modes. Count a session "complete" only if Levels 1-3 ran and resume claims came from UI/PDF or existing application fields - never invented.

**Failure modes:**
- Skipping whoami / scope check
- Inventing PDF body text because MCP has no resume PDF
- Documenting write tools
- Real UUIDs in public examples

**Write-back:** Invent patterns and incomplete-funnel reasons → tighten steps and forever-don'ts in `skills/mcp-funnel-read/SKILL.md` and `docs/MCP_KIT.md`. Human-approved only.

---

## Never in metrics or skill bodies

- Pairwise production score deltas, fraud thresholds, gaming guidance
- Named-client experiments
- Real UUIDs, guest pack URLs, ATS deep links
- Claims that skills power Pairwise production scoring or that agents hire/screen "for you"
- Any write/mutate MCP surface

---

## How to run a starter experiment (operator checklist)

1. Pick one loop and one role family.
2. Run the tied skill as written; log accept / edit / reject (and the loop-specific metric).
3. After the sample-size floor, draft a one-paragraph skill patch proposal.
4. Human approves or rejects the patch before any shared skill body changes.

No invented Pairwise dashboards. Spreadsheet or notes file is enough for v0.
