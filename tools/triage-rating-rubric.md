# Triage trigger rubric

How to set an entry's **triage trigger** (the `triage` array, any `triageExclude`, and the choice of gate / question / opt-in behind it) so the entry surfaces on the right jobs — consistently, regardless of who is authoring it.

This is the rule maintainers follow when building an entry's trigger in the **Triage** tab (the "Surfaces when…" line), and the standard every existing entry is held to when it is reviewed.

---

## The core principle

> The trigger measures **fit between the job and the entry** — it should fire when, and only when, a designer on this job should review this entry — **not** how important the entry is, and **not** which dimension it lives in.

Two corollaries fall straight out of this and cause most real triage defects:

* **Importance is not reach.** An important entry does not deserve a broad trigger; importance is already carried by the rating bands and the evidence support. A critical safety entry with a sloppy trigger that fires on every job trains readers to skim past the whole triage result.
* **Scope is not dimension.** An entry's trigger follows *what the entry is actually about*, never the dimension it happens to sit in. A drawing-clarity entry about large slab bars is triaged as a large-slab-bar entry, not as a "communication" entry. Triaging a whole dimension through one shared fact is the commonest structural mistake.

Everything below is machinery for applying this principle evenly.

---

## Step 1 — Name the entry's true scope

Before touching the trigger, write one sentence: *"This entry matters on a job when ___."* Fill the blank from the entry's own question and background, not from its dimension. That sentence is the target the trigger has to hit. Examples from the live set:

* *…when the job has piles.* (broad, element-level)
* *…when the job has a wall or column **and** the concrete is on show.* (element + condition)
* *…when suspended-slab reinforcement uses 20 mm-plus bars.* (a specific condition on an element)
* *…when the reader is still deciding whether steel could carry the floor.* (an open design intent)
* *…on essentially every reinforced-concrete job.* (genuinely universal)

The scope sentence decides everything in Step 3 — the shape *and* the mechanism.

## Step 2 — Classify the trigger you are building

Triggers are built from three fact types, two combinators, and a suppressor.

**Fact types (and the mechanism each represents):**

* **Presence gate** — an element is on the job: `pile`, `wall`, `slab-suspended`. Ticked at the start.
* **Condition gate** — a cross-cutting state ticked at the start. Two flavours: a *material/element* condition that pairs with a presence gate (`exposed-concrete`, `watertight`), and a *project-context* condition that can stand on its own because it isn't tied to any one element (`retained-or-staged` — retained, existing or part-built structure that must stay standing during construction).
* **Question fact** — a yes / no / not-sure answer to a conditional question, tagged by where the answer comes from (`drawings`, `geotech`, `site`, `intent`): e.g. `reactive-ground`, `considering-screw-piles`, `large-slab-bars`. A question only appears when one of its `when` gates is on.
* **Universal opt-in** — a default-off toggle the reader switches on to add a cross-cutting review: `universal-drawing-clarity`, `universal-buildability`, `universal-site-safety`.

**Combinators:**

* **OR within a slot** — `['wall','column']` = wall *or* column.
* **AND across slots** — `[['wall','column'],['exposed-concrete']]` = (wall or column) *and* exposed.

**Suppressor:**

* **`triageExclude`** — facts that *silence* the entry even when its positive trigger is met.

## Step 3 — Choose the shape and the mechanism

Start at the simplest shape that hits the scope sentence, and add structure only to fix a *failed test* (Step 4). Two questions drive it.

**A. Is the scope preventive or a consequence?**
This decides whether the trigger fires on *presence* or on a *condition*, and it is the distinction most often got wrong.

* **Preventive** — advice you want in front of the designer *before* they have made the choice ("keep slab bars to 12–16 mm where you can"). It must fire on **presence**, because the whole point is to reach the designer while the decision is still open. Gating it on the condition it is trying to prevent would show it only to the people already past the point of acting on it.
* **Consequence** — advice that only bites *once a condition is true* ("since 20 mm-plus bars are being used, watch on-site bending, grinder cutting and callout clarity"). It must fire on the **condition**, not on bare presence, or it over-fires on every job where the condition is absent.

A single topic often has both kinds. Split them: the preventive nudge stays on presence; the consequence entries take the condition. (This is exactly how the large-slab-bar family is wired — see the worked examples.)

**B. Which mechanism carries the scope?**
Match the scope sentence to the lightest mechanism that expresses it:

| Scope sentence looks like… | Use |
|---|---|
| "…whenever element X is present" (applies to every instance of X) | **presence gate** only |
| "…element X **and** state Y (exposed / watertight)" | presence gate **AND** **condition gate** |
| "…element X, but only when sub-condition Z holds" (Z often absent, and cheaply answerable from drawings / geotech / site / intent) | presence gate implied, gated on a **question** for Z |
| "…on essentially every RC job, and it's worth flagging every time" | **presence gate(s)** covering the element union — it will always surface, which is correct for genuinely universal *and* important advice |
| "…on essentially every job, but it's an optional QA-style pass the reader may not want" | **universal opt-in** (default off) |
| "…the same decision as another entry, but a more specific entry should win here" | keep the positive trigger; add **`triageExclude`** on the specific fact |

The two rows that get confused are the universal ones. **Genuinely-universal-and-important → presence union (always on)**, because an opt-in would hide advice that every reader should see. **Genuinely-universal-but-optional → opt-in.** If you cannot honestly call it optional, it does not belong behind an opt-in.

**C. Does a new question earn its place — and is it aimed correctly?**
A new question is friction — one click for every reader whose `when` gate is on. It earns that friction only if **both**: it materially sharpens precision (the entry is genuinely irrelevant when the answer is "no"), *and* the answer is cheap to give (tagged to a real source). A question that gates a single entry is fine when it prevents a real false positive; it is waste when the entry would apply whenever the element is present anyway. Prefer reusing an existing gate, condition or question before inventing one — and a question that gates a *family* of entries is worth far more than one that gates a single entry.

Then check *who answers it, and with what*. The failure to avoid is a question whose answer is **biased toward silencing the entry** — most often because it asks the author to judge the quality of their own work. "Is this structure hard to read in 2D?" fails: the designer holds the whole model in their head and will honestly answer "no," killing the entry meant to protect the builder who has no such model. The fix is **not** to fake objectivity — some genuine triage questions are judgment calls and forcing them into a checklist of observable features narrows them wrongly (a plain stacked frame can still be confusing; a fiddly detail on a simple building can too). The fix is to **remove the bias by framing the judgment as additive, not as a confession**: ask "could the design, or a detail within it, be easier to build with an isometric view?" — a low-bar "would this help?" the author can say yes to without conceding their set is poor — rather than "are your drawings unclear?" Keep the question a judgment where the honest question is a judgment; just don't point it at the one person who can't see the problem.

**D. Keep a family on one path.**
When several entries share a scope (the same condition, across dimensions), they must share one trigger fact so they surface together. Related entries reaching the reader through different paths — some on presence, one buried under an opt-in — is a defect even when each trigger is individually defensible.

## Step 4 — The two tests

Every finished trigger is graded on two independent questions that pull in opposite directions.

**The recall test — does it fire on every job where the entry matters?**
Walk the jobs your scope sentence names. Would each trip the trigger? A missed review is *silent*; a spurious one is merely ignored — so recall failures are the more dangerous kind. Every AND slot, every question, and every `triageExclude` is a chance to *lose* a relevant job; audit each against this test.

**The precision test — of the jobs that fire it, how many genuinely need it?**
Walk the jobs that trip the trigger. If a large share of readers would reasonably think "not relevant to me," tighten it — an AND slot, a condition, or a refining question.

> The two trade off. Widen for recall and you lose precision; tighten for precision and you risk recall. The rubric's job is to place each trigger **deliberately** on that line.

## Targeting quality — the self-check

There is no stored rating for a trigger the way there is for evidence support. Hold each finished trigger against this scale; anything below *well-targeted* needs a reason.

* **Well-targeted** — passes both tests, using the simplest shape and lightest mechanism that hits the scope sentence. No AND slot, question, opt-in or exclude that isn't pulling its weight; any family it belongs to shares its path.
* **Acceptable** — full recall, loose precision, *by deliberate choice* — the entry is cheap to dismiss and broadening avoids a fragile question (a presence-only gate on a common element, where the alternative would be an awkward question).
* **Mis-targeted** — fails a test, or uses the wrong mechanism for its scope (an opt-in for something element-specific; presence for a consequence; a dimension-shared fact instead of a scope fact). Re-shape before publishing.

> A **dark** entry — no valid trigger, so it never surfaces — is an automatic fail. The Triage tab flags these; treat one as unfinished.

---

## Traps to avoid

* **Dimension-lumping.** Triaging every entry in a dimension through one shared fact (e.g. all communication entries behind one "drawing-clarity" opt-in). Triage each entry by *its own* scope; entries in the same dimension will often use quite different mechanisms.
* **Importance inflation.** Broadening a trigger because the entry *feels* critical. Importance lives in the bands, not the reach.
* **Preventive/consequence mix-up.** Firing a "since the condition is true, watch out" entry on bare presence (over-fires), or firing a "keep it simple before you decide" entry on the condition it's trying to prevent (reaches nobody in time).
* **Opt-in misuse.** Hiding genuinely-universal, worth-acting-on advice behind a default-off opt-in (it never surfaces), or parking an element-specific entry under a universal opt-in (wrong mechanism for the scope).
* **The single-entry question that doesn't earn it.** A question gating one entry is fine *only* if the entry is truly irrelevant when the answer is "no." Ask: on a job where the gate is on but the answer is "no," was the entry ever relevant? If no, the question is doing nothing.
* **Silent recall loss.** Precision failures are visible to the reader; recall failures are invisible. Audit every AND slot, question and exclude against the recall test specifically.
* **OR / AND confusion.** `[['a','b']]` is *a or b* (one slot). `[['a'],['b']]` is *a and b* (two slots). Writing an intended "and" as one slot fires far too often.
* **Exclude as a patch.** Reserve `triageExclude` for routing between genuinely competing entries; never to silence an entry a sloppy positive trigger over-fires.
* **The self-silencing question.** A question whose answer is biased toward hiding the entry — usually because it asks the author to grade their own work ("are my drawings clear enough?", "is this detailed well?"). The problem is the bias, not that it's a judgment; the fix is to reframe as an additive "would X help?" the author can answer honestly, not to pretend a real judgment call is an observable fact.
* **Vocabulary drift.** A trigger referencing a fact not defined in `triageConfig` never fires (flagged as an unknown fact). Add the gate or question first, then build on it.

---

## Writing the "Surfaces when…" summary

The Triage tab renders each trigger in plain English. Read it back as a sentence and check it against the scope sentence from Step 1: if the two don't say the same thing, the trigger is wrong however the logic reads. A good trigger is **legible** — a maintainer who has never seen the entry should read the "Surfaces when…" line and agree it targets the right jobs.

---

## When to revisit a trigger

Re-check an entry's trigger when:

* a **new gate, condition or question** is added that could carry this entry's scope more precisely than its current mechanism;
* a **new entry** shares this one's scope — decide whether they should share a fact (family consistency) or whether one should `triageExclude` the other (routing);
* the entry's **scope changes** (its bands or applicability narrow or widen), which usually moves the recall boundary;
* the Triage tab's **validation** flags the entry as dark or referencing an unknown fact;
* readers report it surfacing where it doesn't belong (precision), or *not* surfacing on a job where it clearly applied (recall — take this one seriously).

Because triggers share a fact vocabulary, editing a gate or question can shift several entries at once — **re-run the simulator after any change to `triageConfig`.**

---

## Worked examples

Five applications from the live set, chosen to anchor each decision.

**Presence-only, correct (whole-of-element scope).** `bored-concrete-piles-vs-screw-piles` triggers on `[['pile']]`. Every piled job should weigh the pile-type choice, so recall must be total and precision is already high — any refining question would only drop relevant jobs. Simplest shape is the right one → **well-targeted**.

**Presence AND condition, correct (element + state).** `chamfered-exposed-external-corners` triggers on `[['wall','column'],['exposed-concrete']]`. On `wall` alone it would fire on the majority of walls that are never on show; the condition gate confines it to the jobs where a sharp exposed corner is actually visible → **well-targeted**.

**A family split preventive vs consequence, on one shared question (the model case).** Four sibling entries concern 20 mm-plus slab bars, across four dimensions. The *preventive* one, `hand-bendable-bar-sizes-for-slab-reinforcement` ("keep bars to 12–16 mm where practical"), stays on `[['slab-suspended']]` so it reaches every suspended-slab designer *before* bar sizes are locked. The three *consequence* entries — on-site bending plant (Logistics), grinder cutting (Safety) and callout clarity (Communication) — all trigger on `[['large-slab-bars']]`, a single drawings question gated under `slab-suspended`. One cheap question sharpens three entries at once, unifies a family that previously reached the reader by three different paths (one of them buried under a default-off opt-in), and keeps the preventive/consequence split honest → all four **well-targeted**.

**Universal by scope, so it rides presence — not an opt-in.** `reinforcement-callout-clarity` applies to any reinforced element, and clear callouts are worth flagging on every job, so it triggers on the union of the element gates and surfaces on essentially every run. That is correct: it is genuinely universal *and* worth acting on, so it must not hide behind an opt-in. What stays under the `universal-drawing-clarity` opt-in is only what is genuinely general *and* genuinely optional — a QA-style pass a reader could reasonably skip on a focused run. `isometric-overview-views` was moved *out* of that opt-in once its scope was seen clearly: it isn't universal, it's conditional on whether an isometric would actually help, so it now hangs off the `benefit-from-isometric` question instead (see below) — the mechanism follows the scope.

**A judgment question, aimed correctly.** `isometric-overview-views` is gated on `benefit-from-isometric`, asked plainly: *"Could the overall design, or a detail within it, be easier to build if the set included an isometric or 3D view?"* An earlier attempt objectified this into "does the structure step, slope or transfer?" — but that quietly narrowed the real question, since a simple frame can still be confusing and a fiddly detail on a plain building can too. The honest question here *is* a judgment; the only thing to engineer out is the bias, done by asking "would this help?" (additive) rather than "are your drawings unclear?" (a confession the author will refuse). Left as a judgment, aimed away from the blind spot → **well-targeted**.

**Wrong mechanism fixed — opt-in to condition.** `temporary-stability-of-retained-or-part-built-structure` once sat behind the default-off `universal-site-safety` opt-in. But its scope is not universal (it applies only when there's retained, existing or part-built structure that must stay standing mid-build) and not optional (it's a safety review a reader shouldn't have to opt into). Both facts point away from an opt-in. It now triggers on `[['retained-or-staged']]`, a standalone project-context condition gate, and the opt-in — which held nothing else — was deleted. Scope that is conditional-and-not-optional belongs on a condition, never an opt-in → **well-targeted**.

**Exclude for routing.** `raft-slab-vs-waffle-pod` triggers on `[['slab-on-ground']]` but carries `triageExclude: ['reactive-ground']`. Waffle-vs-raft is the right question on ordinary ground, but on reactive ground a more specific entry supersedes it, so the exclude hands the reader to that entry instead of showing both. Exclude used correctly — de-duplicating competing suggestions, not compensating for a broad trigger → **well-targeted**.

---
