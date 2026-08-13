# Anti-patterns

Read this when you are writing a long justification, adding "what a
real product would have," or about to override a want the user already
chose.

## 1. Fake first principles

Symptoms:

- a numbered list that restates the analogical plan in solemn language
- "axiom: users expect a hamburger menu"
- "axiom: we should use a design system" (that is a method, not a truth)
- quoting Musk and then cloning the category leader

A real axiom survives the question **"how do we know?"** with a
measurement, a law, or a stated user constraint. If the answer is
"that's how these apps work," it is an analogy wearing a lab coat.

## 2. Physics LARPing

Going to atoms, Maxwell, or "what is information" when the next action
will not change.

One or two levels below the common description. Stop when further
digging does not change what you build this hour.

Related: padding a reply with the history of first principles so the
user can see you are being rigorous. They asked for the thing, not the
seminar.

## 3. Deleting the user's want

The method questions *requirements*, not *taste they already picked*.

If they said dark, Japanese, "exactly like this sketch," "must have a
feed," those are constraints. Reconstruct **inside** them.

Question the want only when:

- it contradicts a harder axiom (physics, safety, the preview cannot
  do it)
- they named a form that cannot deliver the function they also named
- they asked you to think, not just to obey

Then say so briefly and offer the reconstructed option. Do not silently
substitute.

## 4. Overthinking as politeness

Using the loop to delay a decision the axioms already settle. Shipping
a smaller correct thing teaches more than another pass of "what is a
task, really?"

If you have the function, 3 axioms, and a smallest reconstruction —
build it.

## 5. Optimizing the leftover ceremony

Musk's most common intelligent-person error: making a thing excellent
that should have been deleted.

Tells:

- a beautiful empty state for a screen that should not exist
- a clever cache around a fetch you do not need
- animating an onboarding step whose information belongs on the first
  screen
- abstracting one call site "for reuse"

Delete, then polish what remains.

## 6. Automating first

Writing a framework, a generator, a config layer, or a plugin system
before a single manual path works.

First make one instance correct and simple. Accelerate. Automate only
the boring remainder.

## 7. Requirements with no owner

"We'll need admin roles." "We'll need i18n." "We'll need analytics."
"We'll need a landing page *and* an app *and* a blog."

Who asked? What breaks if it is absent from v1? If you cannot name
either, it is not a v1 requirement.

## 8. Analogy to your last build

The previous app in context (or in training) had auth, a sidebar, and
four routes. This request is a timer. Copying the last skeleton is
analogy.

Rebuild from this function. Reuse platform wiring (auth helpers, Vite
port contract) because those are **real constraints of this
environment**, not because the last demo used them.

## 9. First principles versus known failure modes

Ignoring a domain skill's hard-won axiom because you "reasoned from
scratch":

- inverted A/D (`controls`)
- blank production build (asset MIME / nitro gated to `build`)
- ad-hoc hex and purple blobs (`design-ui`)
- code-drawn stick figures where real sprites were implied

Those are measured facts about this environment. Treating them as
optional is not independent thought.

## 10. Performing the worksheet

Pasting the function/axioms/deleted/plan block on every reply,
including "change the button to green."

Show the reconstruction only when `SKILL.md` §2 says so. Otherwise
let the work reveal the thinking.
