---
name: self-refine-loop
description: >
  Runs a generator-critique-reviser loop to iteratively improve outputs.
  Use when quality matters: complex reasoning, code/strategy drafts, research
  synthesis, high-uncertainty tasks, or when the first answer feels incomplete.
  Prefer this over one-shot answers for non-trivial work. Also trigger on
  explicit "refine / critique / improve / self-refine". Stop at 5 iterations
  or confidence ≥ 8/10.
version: 1.2.0
author: Stijnman + adapted
license: MIT
compatibility: Grok agent; optional MCP and shell access
metadata:
  grok:
    tags: [self refine, reflexion loop, critique and revise, improve output, iterate]
    related_skills: [goal-verifier, agentic-uncertainty-quantifier, first-principles]
---

# Self Refine Loop

## When to Use

- Complex or high-stakes outputs (strategy code, research conclusions, decisions)
- First draft is incomplete, inconsistent, or low-confidence
- User asks to refine, critique, improve, or iterate
- After uncertainty-quantifier flags high epistemic uncertainty

## Workflow

1. Capture the current output and the user's quality criteria.
2. Generate a critique listing specific weaknesses (max 5 bullets).
3. Revise the output addressing every critique point.
4. Score confidence 0-10 on whether criteria are met.
5. Repeat until confidence >= 8 or 5 iterations; return best version with changelog.

## Integrations

- `goal-verifier`
- `agentic-uncertainty-quantifier`
- `dspy-prompt-optimizer`

## Error Handling

| Failure | Response |
|---------|----------|
| No criteria given | Ask user for 1-3 success criteria before looping. |
| Confidence stuck below 5 | Stop early; report blocker and ask for guidance. |
| Output grows unbounded | Cap revisions to prior length + 20%. |

## Gotchas

- Do not loop on trivial typos; one-pass fix is enough.

## Example

**Input:** User request matching triggers above.
**Output:** Structured result per workflow with integrations invoked as needed.
