# SKILL_NAMING

How skills written in this repo, or anywhere in the org, are named. The same rule ships as the `skill-naming` agent skill, which agents use when they create a skill.

## Scope

Applies to skills we write or adapt and now own. Downloaded or third-party skills (plugin and marketplace skills, vendor packs, skills copied from a public repo) keep their upstream names, because renaming them breaks updates and comparison with the source.

## Rule

Order words from least specific to most specific, so a sorted list groups related skills together:

```
<subject>-<narrower subject...>-<task>-<org>
```

- **Subject first:** what the skill works on, or the tool it wraps (`candidate`, `role`, `github`, `db-migration`).
- **Narrowing words next,** only as many as needed to tell siblings apart.
- **Task last, as a noun:** `assessment`, `outreach`, `audit`, `fix`. Leave it out when the subject already says it (`release-notes`).
- **Org qualifier at the end,** only for an org-specific overlay on a general subject (`webflow-pairwise`). The overlay then sorts next to the general skills for that tool.
- **Field knowledge packs** that other skills load use `domain-<field>-<area>` (`domain-engineering-hardware`). Keep two levels until one grows too large.

## Format

- Lowercase letters, digits and single hyphens; at most 64 characters; aim for 2-4 words.
- The folder name and the `name:` field match exactly.
- No reserved words (`anthropic`, `claude`), no version or phase numbers.

## Word choice

- Use the word people search for. Full words beat abbreviations, except a tool's own name (`gh`, `az`).
- One word for one thing across a group (not `pr` in one skill and `pull-request` in the next).
- Steps in a sequence get distinct task words (`role-requirements`, then `candidate-assessment`).
- Choose names to last. Renaming a skill breaks everything that points at it.

## Examples

| Draft | Better | Why |
|---|---|---|
| `fix-db-migration` | `db-migration-fix` | Subject first |
| `pairwise-daily-outreach` | `outreach-daily-pairwise` | Org goes last |
| `outreach` | `candidate-outreach` | Joins its group |
| `role-assessment` | `role-requirements` | Distinct from `candidate-assessment` |

## Test

Sort the neighboring skill names with the new one. It should land next to its relatives, and a reader should be able to guess what it does from the name alone.
