---
name: goal-verifier
description: >
  Verifies task completion against stated or inferred goals before declaring
  work done. ALWAYS run a lightweight check at the end of multi-step tasks,
  code changes, research deliverables, strategy updates, or when the user
  asks to confirm / verify / "is this done". Use even without explicit
  "verify" wording if the conversation has a clear original goal.
version: 1.2.0
author: Stijnman + adapted
license: MIT
compatibility: Grok agent; optional MCP and shell access
metadata:
  grok:
    tags: [verify goal, confirm success, did I achieve this, check if done, complete]
    related_skills: [self-refine-loop, first-principles]
---

# Goal Verifier

## When to Use

- End of any multi-step task that had an explicit or implied goal
- After code/strategy changes or research synthesis
- User asks to confirm, verify, or "is this finished / good enough"
- Before marking a deliverable complete

## Workflow

1. Restate the original goal in one sentence.
2. List acceptance criteria (explicit or inferred from conversation).
3. Check each criterion: pass / fail / partial with evidence.
4. If any fail, invoke self-refine-loop or report gaps.
5. Only mark complete when all critical criteria pass.

## Integrations

- `self-refine-loop`
- `auto-tester`

## Error Handling

| Failure | Response |
|---------|----------|
| Goal undefined | Ask user to confirm goal before verifying. |
| False positive risk | Require evidence (file path, command output, or test result). |

## Gotchas

- Verification is read-only; do not mutate artifacts during checks.

## Example

**Input:** User request matching triggers above.
**Output:** Structured result per workflow with integrations invoked as needed.
