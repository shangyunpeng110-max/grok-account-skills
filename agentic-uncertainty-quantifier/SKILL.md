---
name: agentic-uncertainty-quantifier
description: >
  Scores task uncertainty (epistemic + procedural) to calibrate how deep to
  think, how much context to retrieve, and whether to iterate. ALWAYS consider
  this skill on high-stakes decisions, sparse facts, ambiguous goals, trading
  or financial choices, irreversible actions, or when confidence feels
  overstated. Use even if the user never says "uncertainty" or "how sure".
  Skip only trivial or pure-factual lookups.
version: 1.2.0
author: Stijnman + adapted
license: MIT
metadata:
  grok:
    tags: [quantify uncertainty, fast slow think, uncertainty score, how sure, decision, risk]
    related_skills: [self-refine-loop, first-principles, research-assistant]
compatibility: Grok agent; optional MCP and shell access
---

# Agentic Uncertainty Quantifier

## When to Use

- High-stakes or irreversible decisions (trading, money, health-adjacent, deploy)
- Facts are sparse, conflicting, or rapidly changing
- Goal is ambiguous or acceptance criteria unclear
- User asks about confidence / risk / "how sure"
- Any time first-principles reconstruction produces a non-obvious plan

## Workflow

1. Score epistemic uncertainty 0-10 (how much is unknown).
2. Score procedural uncertainty 0-10 (how clear are the steps).
3. High epistemic (>6): retrieve more context, run self-refine-loop.
4. Low procedural (<4): ask clarifying questions before acting.
5. Report scores and recommended depth to user.

## Integrations

- `self-refine-loop`
- `semantic-memory-manager`
- `deep-search-enabler`

## Error Handling

| Failure | Response |
|---------|----------|
| False confidence | Bias toward caution on destructive tasks. |

## Gotchas

- Uncertainty > 7 on financial/deploy actions triggers hitl-approver.

## Example

**Input:** User request matching triggers above.
**Output:** Structured result per workflow with integrations invoked as needed.
