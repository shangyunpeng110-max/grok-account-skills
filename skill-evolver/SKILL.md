---
name: skill-evolver
description: >
  Full skill rewrite and improvement with versioned backups. Use when a skill
  is insufficient for the current task, produces weak results, or the user
  asks to evolve / upgrade / improve a skill. Also consider after repeated
  similar failures or when first-principles analysis shows the skill's
  assumptions are outdated. Prefer proactive suggestion over waiting for
  exact trigger words.
version: 1.2.0
author: Stijnman + adapted
license: MIT
metadata:
  grok:
    tags: [evolve skill, upgrade SKILL.md, improve skill file, skill improvement]
    related_skills: [skill-creator, first-principles]
compatibility: Grok agent; optional MCP and shell access
---

# Skill Evolver

## When to Use

- User explicitly asks to evolve / upgrade / improve a skill
- A skill repeatedly under-performs on the user's typical tasks
- First-principles review reveals outdated assumptions in a skill
- After installing new skills that need local adaptation

## Workflow

1. Backup to versions/<timestamp>/SKILL.md.
2. Read references/evolution-guide.md for rubric.
3. Rewrite weak sections per 10-dimension review.
4. Validate; run hyper-skill-tester; save or rollback.

## References

Read `references/evolution-guide.md` when setup, backends, or rubric details are needed.

## Integrations

- `skill-evolution-engine`
- `hyper-skill-tester`
- `natural-language-to-skill`

## Error Handling

| Failure | Response |
|---------|----------|
| Broken frontmatter | Restore from versions/ immediately. |

## Gotchas

- Read references/evolution-guide.md before major rewrites.

## Example

**Input:** User request matching triggers above.
**Output:** Structured result per workflow with integrations invoked as needed.
