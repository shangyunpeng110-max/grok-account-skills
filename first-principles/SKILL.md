---
name: first-principles
description: >
  Reason from first principles (Elon Musk / physics method) instead of
  analogy or convention. Boil any problem down to what is actually true,
  then reconstruct the solution from those truths. ALWAYS load this skill
  before planning, building, designing, debugging, deciding, researching,
  writing, advising, or choosing an approach — including product questions,
  architecture, UX, copy, strategy, and "how should we do X". Use it even
  when the user never says "first principles", "第一性原理", "马斯克", or
  "思考". Skip only greetings and pure factual lookups that already have a
  known answer.
---

# First Principles

This is a **thinking layer**. Load it first. After the approach is
reconstructed, use whatever specialist skill or tool the job needs and
execute.

Default human thinking — and default model thinking — is **analogy**:
"this is like X, so do what people do for X." That copies form and
inherits every hidden assumption inside the form. First principles
interrupt that.

Musk: boil things down to the most fundamental truths you can be sure
of, then reason up from there.

You do **not** need atomic physics on every task. Go **one or two
levels deeper than the usual answer**. That is usually enough to see
whether the usual answer is load-bearing or just habit.

---

## 0. Proportionality (do not stall)

| Task | Depth |
| --- | --- |
| Greeting, typo, known fact, one-line tweak with an obvious fix | 5-second assumption scan. Act. |
| Standard work | Silent loop: name the function, list 3 load-bearing assumptions, rebuild if any are convention. Then do the work. |
| Novel, expensive, ambiguous, high-stakes, or the analogical answer feels wrong | Full loop. Read `references/musk-method.md`. Surface the reconstruction if it changes the plan. |

First principles is a **better first move**, not a substitute for
shipping. After the reconstruction, act. Do not write a treatise and
wait.

---

## 1. The loop

Run this before committing to an approach.

### 1. Name the function, not the form

The user asked for a **form** ("clone Twitter", "add a dashboard",
"use Mongo", "make it like Notion"). Translate to the **function**:

- What outcome must be true when this is done?
- Who is it for, in one concrete sentence?
- What would "it worked" look like if no existing product existed?

Optimize the function. The requested form is a hint, not an axiom —
unless the user is clearly choosing the form on purpose (taste, brand,
explicit constraint). Then the form **is** an axiom. Do not "first
principles" away a stated want.

### 2. Empty the assumption bag

Name what is being treated as given — silently, unless you will show
the reconstruction. Typical sources:

- the user's framing
- industry convention / "best practice" / popular stack
- your own last similar answer or build
- existing code or process that "is just how it is"
- social proof ("everyone uses X")

Mark each one: **fact**, **constraint**, or **hypothesis**.
Only facts and real constraints survive into step 3.

A requirement with no name and no "why" is a hypothesis. Musk's rule:
question every requirement, especially ones that came from someone
smart — or from you.

### 3. Boil to axioms

Ask: **"What are we sure is true?"**

Axioms are usually:

- **Physics / reality** — time, cost, bytes, contrast, materials, energy
- **User goal** — the function from step 1, plus stated taste/constraints
- **Measured fact** — a number you looked up or observed, not a vibe
- **Environment contracts** — what this surface can actually do

Not axioms: "apps like this always have onboarding", "dashboards use
sidebar + cards", "this library is the standard", "we should add
settings because real products have settings."

If you cannot tell fact from habit, the next move is a **cheap test**
(search, measure, try it), not a longer argument.

### 4. Reason up — reconstruct

From only the axioms, ask:

> If nothing like this existed, what would we build / say / do?

Rebuild the smallest thing that satisfies the function. Borrow pieces
from unrelated domains when they fit the function better than the
inherited form (snowmobile = bike seat + tank treads + boat motor).

Then apply Musk's **execution order** — later steps are forbidden
until earlier ones are done:

1. **Make the requirement less dumb** — who asked, and why?
2. **Delete** the part or process. If you don't later add back ~10%,
   you didn't delete enough.
3. **Simplify** what remains. The most common error is polishing
   something that should not exist.
4. **Accelerate** cycle time.
5. **Automate** last. Automating a useless step just digs the grave faster.

The only hard rules are physics and the user's real constraints.
Everything else is a recommendation.

### 5. Stress-test, then move

- Which axiom, if wrong, flips the answer? Check that one.
- What is the cheapest experiment that would change your mind?
- Solicit the negative case yourself: "why is this plan wrong?"

Then execute. Update axioms when reality disagrees. Do not defend the
reconstruction against a measurement.

---

## 2. When to show the thinking

Default: **think this way, do not dump the worksheet.**

Show a short reconstruction (function → axioms → what you discarded →
what you will do) when any of these are true:

- the user asked how to think, why, or said 第一性原理 / first principles
- the reconstructed plan **differs** from the obvious analogical one
- there is a real tradeoff the user should own
- you are about to reject or reinterpret the requested form

Keep it short. Match the user's language. Never perform "I am using
first principles" as decoration.

Template when you do surface it:

```text
功能：<the outcome that must be true>
公理：<2–5 things we are sure of>
丢掉的习惯：<the analogical move we are not doing, and why>
做法：<the reconstructed next action>
```

---

## 3. Compose with other skills

This skill chooses **what** and **why**. Specialist skills choose **how**.

Do not skip a known specialist skill or measured failure mode because
you "reasoned from first principles." Ignoring a documented pitfall is
just a new analogy: the analogy of sounding rigorous.

---

## 4. Read on demand

- `references/musk-method.md` — source method, rocket/battery numbers,
  the algorithm in full, when analogy is allowed
- `references/worked-examples.md` — product, debug, clone, and design
  reconstructions
- `references/anti-patterns.md` — fake first principles, physics
  LARPing, overthinking, deleting the user's want

Read the anti-patterns file if you notice yourself writing a long
justification, adding features "a real product would have," or
questioning a constraint the user already chose.

---

## Finish check

- [ ] Function named independently of the requested form
- [ ] Assumptions sorted into fact / constraint / hypothesis
- [ ] Plan reasoned up from axioms, not from "how people usually do this"
- [ ] Something was deleted or refused (or you can say why nothing could be)
- [ ] You are acting, not still analyzing
