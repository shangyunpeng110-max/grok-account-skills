# Worked reconstructions

These are patterns, not templates to paste. Steal the *move*, not the
nouns.

---

## 1. "Clone Twitter"

**Requested form:** a Twitter clone.

**Function:** people write short public notes; other people they chose
can see those notes in time order.

**Assumption bag:**

| Claim | Sort |
| --- | --- |
| Need tweets, retweets, likes, DMs, Spaces, Grok, ads, explore | hypothesis (platform residue) |
| Need follow graph + timeline | maybe — only if "other people they chose" is real |
| Need accounts | constraint if notes persist per person; else not |
| Must look like Twitter | hypothesis unless the user said "look like Twitter" |
| Preview must actually run | fact (platform) |

**Axioms:** one composer, a readable list, identity if persistence
matters, mobile-usable tap targets.

**Deleted:** Spaces, ads, explore, trending, moments, bookmarks
folders, the second sidebar.

**Reconstructed:** a tight feed + compose + follow (or even a single
shared board if "follow" is not the job). Looks like *this* product,
not a blue-bird skin.

**Tell you copied:** you built a right-rail "What's happening" panel
with fake trends.

---

## 2. "Build a dashboard"

**Requested form:** dashboard.

**Function (must be named):** e.g. "I can see which invoices are late
and poke the late ones."

**Analogical build:** sidebar, 4 KPI cards, a big area chart, a table
nobody acts on, a date range that does nothing.

**Axioms:** there are invoices; lateness is `due_at < now && unpaid`;
the action is remind / mark paid.

**Reconstructed:** a list of late invoices, the amount, one primary
action per row. Totals are a byproduct of that list, not the product.
A chart earns its place only if it changes a decision the list cannot.

**Tell you copied:** four cards that restate the same table.

---

## 3. "Add settings"

**Requested form:** a settings page.

**Function:** change the 1–2 things a person actually needs to change
(theme? name? default view?).

**Axioms:** those 1–2 values, persisted, reversible.

**Deleted:** the settings route, the nav item, the 12-row form.

**Reconstructed:** a control where the decision happens (a theme toggle
in the header; a rename on the profile). Add a settings page only when
the knobs are many and rarely used.

**Tell you copied:** a gear icon that opens three tabs of unused
switches.

---

## 4. Bug: "the page is blank"

**Analogical debug:** restyle the hero, add a spinner, rewrite the
router "to be cleaner."

**Function:** the page must show the content that is supposed to be there.

**Axioms:** data exists or does not; a component is throwing or not;
a route matches or does not.

**Reconstructed path:** load it, read console + DOM, fix the first
broken axiom. Do not "improve" around an unknown blank.

**Tell you copied:** you shipped a new color token on a white screen.

---

## 5. Game: "make an FPS"

**Requested form:** FPS.

**Function (typical one-liner):** move, look, shoot, something shoots
back, you can tell if you are winning.

**Assumption bag:** sprint, ADS, recoil graphs, loot, 3 weapons,
minimap, voice, multiplayer.

**Axioms here:** single-player only on this target; WASD + pointer
lock; A/D must not be inverted (`controls` skill); one enemy type is
enough to prove the loop.

**Deleted:** multiplayer, loadout screen, crafting.

**Reconstructed:** one arena, one gun, one enemy, a score, a start
overlay that states the controls. Then juice.

**Tell you copied:** a pause menu with graphics quality presets and no
working shoot.

---

## 6. "Use the popular stack / add Redux / add a CMS"

**Requested form:** a named tool.

**Function:** some state must survive some lifetime (one session? one
user? many authors?).

**Axioms:** what already sits in the workspace (React, Zustand, the
DB helpers) plus the actual lifetime.

**Reconstructed:** use the thing already here if it covers the
lifetime. Add a dependency only when an axiom (multi-user persistence,
offline, …) is not met.

**Tell you copied:** a new state library next to a working store, "for
scale."

---

## 7. Design: "make it look premium"

**Requested form:** premium / modern / clean.

**Function:** a stranger understands the hierarchy in one glance and
trusts the primary action.

**Axioms (`design-ui`):** few colors, two fonts, tokens not ad-hoc hex,
contrast, ~390px, no decorative blobs.

**Deleted:** gradient mesh, glassmorphism everywhere, extra accent
hues, three competing CTAs.

**Reconstructed:** one surface language, one accent, type and spacing
do the luxury. Premium is restraint plus material honesty, not more
effects.

**Tell you copied:** purple gradient, inter, rounded cards, fake
testimonials.

---

## How to write your own

For any new request, fill this once (silently unless §2 of `SKILL.md`
says to show it):

```text
form:     <what they named>
function: <what must be true>
axioms:   <sure facts + real constraints>
hypotheses we are dropping: <…>
smallest reconstruction: <next build>
```

If the reconstruction equals the analogical default, say so to
yourself and move. First principles that always invent a clever twist
are just a new habit.
