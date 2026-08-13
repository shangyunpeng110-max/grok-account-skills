# Musk / physics first-principles method

Load this when the task is novel, expensive, or the analogical answer
feels sticky. The `SKILL.md` loop is enough for ordinary work.

## What a first principle is

Aristotle: "the first basis from which a thing is known" — a premise
that cannot usefully be deduced from something more basic **in this
problem**.

You are not doing particle physics. You are refusing to treat
*inherited form* as *necessary truth*.

Musk (TED / interviews):

> I tend to approach things from a physics framework. Physics teaches
> you to reason from first principles rather than by analogy. … boil
> things down to the most fundamental truths and say, "What are we
> sure is true?" … and then reason up from there.

> The normal way we conduct our lives is we reason by analogy. We are
> doing this because it is like something else that was done, or it is
> like what other people are doing.

> Though most of our life we get through it by reasoning through
> analogy … otherwise mentally you wouldn't be able to get through the
> day. But when you want to do something new you have to apply the
> physics approach. Physics has really figured out how to discover new
> things that are counter-intuitive, like quantum mechanics.

> The only rules are the ones dictated by the laws of physics.
> Everything else is a recommendation.

Two more habits he pairs with the method:

- **Solicit negative feedback**, especially from people who will
  actually tell you that you are wrong. Generate the counter-argument
  yourself if nobody else is in the room.
- **Use analogy for the routine day.** First principles is for the
  part that needs to be new, cheaper, simpler, or true.

## Worked source examples (keep the numbers)

### Rockets — SpaceX

Analogical frame: "orbital rockets cost $50–65M; that is what rockets
cost."

First-principles questions:

1. What is a rocket *made of*? Aerospace aluminum alloys, titanium,
   copper, carbon fiber.
2. What do those materials cost on the commodity market?
3. Answer Musk cited: materials ≈ **2% of the typical rocket price**.

So the axiom is not "rockets are expensive." The axiom is "these
materials, arranged to survive this physics, currently carry a huge
manufacturing and non-reuse markup." The reconstructed moves:
manufacture in-house, delete parts, reuse the expensive ones.

The analogical industry optimized the *form* (expendable government
rockets). First principles optimized the *function* (mass to orbit).

### Batteries

Analogical frame: "batteries cost X per kWh because that is the
industry price."

First-principles: what materials, in what proportions, at commodity
prices? Then: what process steps add the rest of the cost? Delete or
vertical-integrate the expensive steps.

## The Algorithm (execution order — do not invert)

1. **Make the requirement less dumb** — Who asked, and why? Question
   every requirement, especially ones from smart people (including
   yourself).
2. **Delete** the part or process. If you don't later add back ~10%,
   you didn't delete enough.
3. **Simplify** what remains. The most common error is polishing
   something that should not exist.
4. **Accelerate** cycle time.
5. **Automate** last. Automating a useless step just digs the grave
   faster.

The only hard rules are physics and the user's real constraints.
Everything else is a recommendation.

## When analogy is the right tool

Analogy is not a sin. It is compression.

Use it when:

- the problem is routine and the inherited form is cheap and known-good
- you are matching an existing system on purpose (this app's tokens,
  this engine's conventions, this user's stated taste)
- you need a 5-second answer and being 10% wasteful is fine

Refuse it when:

- the form is expensive, ugly, or "everyone does it this way"
- you are about to add a layer / entity / settings screen / engine
  "because real apps have one"
- the user asked for a clone but the function is smaller than the clone
- a number (cost, latency, steps, fields) feels inherited rather than
  measured

A practical split: **analogy to start moving, first principles on
anything you are about to keep.**

## How far to dig

James Clear's operational rule: you do not have to reach atoms. Go
one or two levels below the common description.

| Common description | One level down | Two levels down |
| --- | --- | --- |
| "We need a dashboard" | "Someone must see these 4 numbers and act" | "The action is: reply to the overdue invoice" |
| "Clone Twitter" | "People post short public notes and follow others" | "This user wants to jot thoughts and see friends' thoughts" |
| "Add authentication" | "This data must belong to one person" | "Only the owner may read or write these rows" |
| "The game needs a tutorial" | "The player must learn A = left before the first crash" | "The first 10 seconds are the tutorial" |

Stop when further decomposition does not change the next action.

## Negative feedback as a step

Before you lock a non-trivial plan, spend one pass on:

- "This plan is wrong because ___."
- "The axiom I am least sure of is ___."
- "If I am just copying a familiar app, the tell is ___."

If you cannot fill those blanks, you have not looked. If you can,
either check the weak axiom or proceed with eyes open.
