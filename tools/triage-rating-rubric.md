# Triage trigger rubric

How to set an entry's **triage trigger** — the `triage` array, any `triageExclude`, the `standing` flag, and the gates and questions behind them — so the entry surfaces on the right jobs, consistently, regardless of who is authoring it.

This is the rule maintainers follow when building an entry's trigger in the **Triage** tab (the "Surfaces when…" line), and the standard every existing entry is held to when it is reviewed.

---

## The core principle

> A trigger measures **fit between the job and the entry**. It fires when, and only when, a designer on this job should review this entry. It is not a measure of how important the entry is, not a measure of which dimension it lives in, and **not a measure of what the reader feels like reading.**

Three corollaries fall out, and they cause most real triage defects:

* **Importance is not reach.** An important entry does not deserve a broad trigger. Importance is already carried by the rating bands and the evidence support. A critical safety entry with a sloppy trigger that fires on every job trains readers to skim past the whole triage result.
* **Scope is not dimension.** A trigger follows *what the entry is actually about*, never the dimension it happens to sit in. A drawing-clarity entry about large slab bars is triaged as a large-slab-bar entry, not as a "communication" entry. Triaging a whole dimension through one shared fact is the commonest structural mistake.
* **Reader appetite is not a job fact.** "I have read this before and considered it" is true of the reader, not of the job. It must never enter a trigger. If experienced readers should be able to mute standing advice, that is a **display preference**, handled in the results view — not a question in the triage flow. This is why the old default-off universal opt-ins were deleted: they let reader appetite decide whether a Safety in Design entry ever surfaced.

Everything below is machinery for applying this principle evenly.

---

## The reconstruction test — the whole method in one line

> **Name the jobs the entry bites on. Then find the smallest set of facts that reproduces exactly that set of jobs.**

Every rule in this rubric is a consequence of that test, not an axiom above it. If a rule below ever conflicts with the test, the test wins and the rule is wrong.

Three things can go wrong, and only three:

1. **The trigger fires on jobs the entry doesn't bite on** → a precision failure.
2. **The trigger misses jobs the entry does bite on** → a recall failure, and it is *silent*.
3. **No combination of existing facts reproduces the job set** → the **vocabulary** is wrong, not the trigger. Fix the vocabulary. Do not approximate.

Case 3 is the one reviewers skip, and it is where the real defects hide. Two symptoms:

* **A gate standing in for something broader than it says.** A slab entry wired to `slab-suspended` when its own scope names raft slabs too. The gate isn't wrong; the trigger is using it as shorthand for "slab", and every ground-slab job silently loses the entry.
* **One fact doing two jobs.** A `watertight` fact that means both *"this structure must hold water out"* and *"this deck carries a membrane"* will be ticked for one meaning and silently withhold the entries that needed the other. Split it.

---

## Step 1 — Name the entry's true scope

Write one sentence: *"This entry matters on a job when ___."*

The entry's `applicability.appliesWhere` is the **starting draft** of that sentence, not the finished article. It was written by the same person who wrote the trigger, so it will tend to agree with the trigger by construction — which makes the recall test in Step 4 tautological if you accept it uncritically. **Attack it first:**

* Read the **bands**, not the prose. Where does the guidance actually change what the reader does? That is the real boundary.
* Then ask the counter-question: **name a job where this entry would have been worth reading, that my scope sentence excludes.** If you can name one, the sentence is too narrow — and so is the trigger built on it.

Good scope sentences from the live set:

* *…when the job has piles.* (broad, element-level)
* *…when the job has a wall or column **and** the concrete is on show.* (element + condition)
* *…when any slab — suspended or ground-bearing — uses 20 mm-plus bars.* (a condition on a family of elements)
* *…when the reader is still deciding whether steel could carry the floor.* (an open design intent)
* *…on every reinforced-concrete job.* (genuinely universal → a **standing** entry)

The scope sentence decides everything in Step 3.

## Step 2 — The fact vocabulary

Triggers are built from **three** fact types, two combinators, and a suppressor. There is no fourth type; in particular **there is no opt-in.**

**Fact types:**

* **Presence gate** — an element is on the job: `slab-suspended`, `beam-suspended`, `slab-on-ground`, `footing`, `wall`, `column`, `pile`. Ticked at the start.
* **Condition gate** — a cross-cutting state ticked at the start. Two flavours: a *material/element* condition that pairs with a presence gate (`exposed-concrete`, `water-retaining`, `wet-or-drained-slab`), and a *project-context* condition that stands on its own because it isn't tied to any one element (`retained-or-staged`).
* **Question fact** — a yes / no / not-sure answer to a conditional question, tagged by where the answer comes from (`drawings`, `geotech`, `site`, `intent`): `large-bars`, `reactive-ground`, `considering-screw-piles`. A question is only asked when one of its `when` gates is on.

**Combinators:**

* **OR within a slot** — `[['wall','column']]` = wall *or* column.
* **AND across slots** — `[['wall','column'],['exposed-concrete']]` = (wall or column) *and* exposed.

**Suppressor:**

* **`triageExclude`** — facts that *silence* the entry even when its positive trigger is met.

**"Not sure" counts as yes.** A question answered *not sure* establishes its fact, and the entry surfaces flagged as *"you weren't sure."* This is deliberate: a recall failure is silent, a spurious suggestion is one line to skim. Never design a question that relies on *not sure* behaving as *no*.

## Step 3 — Choose the shape

Start at the simplest shape that hits the scope sentence. Add structure only to fix a *failed test* (Step 4).

**A. Is the scope universal? Then it is a standing entry.**
If the honest scope sentence is *"on every reinforced-concrete job"* — formwork exists on every RC job; every drawing set carries reinforcement callouts, details and schedules — the entry does not need a trigger at all. Mark it **`standing: true`**. It surfaces on every triage run, in its own group, above the job-specific results.

Do not fake a trigger for a standing entry by OR-ing together every element gate. That is the same statement dressed as logic, and it hides the fact that the entry is unconditional.

Do not hide a standing entry behind anything the reader has to switch on. If the advice is worth giving on every job, the reader who never switches it on is precisely the reader who needed it.

**B. Is the scope preventive or a consequence?**
This decides whether the trigger fires on *presence* or on a *condition*, and it is the distinction most often got wrong.

* **Preventive** — advice you want in front of the designer *before* they make the choice ("keep slab bars to 12–16 mm where you can"). It fires on **presence**, because the point is to reach the designer while the decision is still open. Gating it on the condition it is trying to prevent shows it only to people already past the point of acting on it.
* **Consequence** — advice that only bites *once a condition is true* ("since 20 mm-plus bars are being used, watch on-site bending, grinder cutting and callout clarity"). It fires on the **condition**, not on bare presence, or it over-fires on every job where the condition is absent.

A single topic often has both kinds. Split them: the preventive nudge stays on presence; the consequence entries take the condition. This is exactly how the large-bar family is wired — see the worked examples.

**C. Which mechanism carries the scope?**

| Scope sentence looks like… | Use |
|---|---|
| "…on every RC job" | **`standing: true`** — no trigger |
| "…whenever element X is present" | **presence gate** only |
| "…element X **and** state Y (exposed / water-retaining / membrane)" | presence gate **AND** condition gate |
| "…element X, but only when sub-condition Z holds" (Z often absent, cheaply answerable from drawings / geotech / site / intent) | **question** for Z, `when`-gated on the elements that make Z askable |
| "…the same decision as another entry, but a more specific entry should win here" | keep the positive trigger; add **`triageExclude`** on the specific fact |

**D. Does a new question earn its place — and is it aimed correctly?**
A question is friction: one click for every reader whose `when` gate is on. It earns that friction only if **both**: it materially sharpens precision (the entry is genuinely irrelevant when the answer is "no"), *and* the answer is cheap to give (tagged to a real source). Prefer reusing an existing gate, condition or question before inventing one — and a question that gates a *family* of entries is worth far more than one gating a single entry.

Then check *who answers it, and with what*. The failure to avoid is a question whose answer is **biased toward silencing the entry** — most often because it asks the author to judge the quality of their own work. "Is this structure hard to read in 2D?" fails: the designer holds the whole model in their head and will honestly answer "no," killing the entry meant to protect the builder who has no such model. The fix is **not** to fake objectivity — some genuine triage questions are judgment calls, and forcing them into a checklist of observable features narrows them wrongly (a plain stacked frame can still be confusing; a fiddly detail on a plain building can too). The fix is to **remove the bias by framing the judgment as additive, not as a confession**: ask "could the design, or a detail within it, be easier to build with an isometric view?" — a low-bar "would this help?" the author can say yes to without conceding their set is poor — rather than "are your drawings unclear?" Keep the question a judgment where the honest question *is* a judgment; just don't point it at the one person who can't see the problem.

**E. Check the question's `when`, not just the trigger.**
A question can only be asked on jobs where one of its `when` gates is ticked. **A trigger built on a question inherits that question's `when` as a hidden AND-slot.** This is the easiest way to lose an entry silently: the trigger reads correctly, the fact exists, the validator is happy, and the entry is nonetheless dark on a whole class of jobs because the question is never put.

Audit it explicitly: *on the jobs my scope sentence names, is this question actually asked?* If a slab entry's question is `when`-gated on `slab-suspended` alone, every ground-slab job loses the entry — no matter how good the trigger looks.

**F. Keep a family on one path.**
When several entries share a scope (the same condition, across dimensions), they must share one trigger fact so they surface together. Related entries reaching the reader by different paths — some on presence, one behind a separate switch — is a defect even when each trigger is individually defensible.

## Step 4 — The two tests

Every finished trigger is graded on two questions that pull in opposite directions.

**The recall test — does it fire on every job where the entry matters?**
Walk the jobs your scope sentence names — the *attacked* sentence from Step 1, not the one you first wrote. Would each trip the trigger? Every AND slot, every question (**and every question's `when`**), and every `triageExclude` is a chance to *lose* a relevant job. Audit each against this test.

**The precision test — of the jobs that fire it, how many genuinely need it?**
Walk the jobs that trip the trigger. If a large share of readers would reasonably think "not relevant to me," tighten it.

**How the two trade off — and why they are not symmetric.**

A false positive costs one line the reader skims and doesn't tick. A false negative costs the entry entirely, and *the reader never learns it happened*. So:

> **Precision is a property of the result set, not of an entry.** Do not tighten an individual trigger for its own precision unless a real job's result list has become too long to read. Recall is judged entry by entry; precision is judged list by list.

This reconciles two things that look contradictory: a spurious suggestion is individually cheap, *and* an entry that fires on every job regardless of fit still degrades the whole result. The first is about one row; the second is about the list.

The practical consequence: **run the simulator on real jobs, not just on entries.** Before signing off a pass, walk three or four representative jobs — a single-storey house on a waffle raft; a two-storey house with a suspended slab and piles; a small commercial frame with a basement; a renovation with retained structure — and read each result list as a reader would. If it is unusable, the problem is systemic and no individual trigger will reveal it.

## Targeting quality — the self-check

Hold each finished trigger against this scale. **Record the call and the reason in the entry's triage rationale** — a deliberately loose trigger and a careless one look identical to the next reviewer, and the point of a written rating is to make the gap visible.

* **Well-targeted** — passes both tests, using the simplest shape and lightest mechanism that hits the scope sentence. No AND slot, question, exclude or standing flag that isn't pulling its weight; any family it belongs to shares its path.
* **Acceptable** — a *deliberate* trade, stated as such. Two legitimate kinds: **full recall / loose precision by choice** (a presence-only gate on a common element, where the alternative would be an awkward question and the entry is cheap to dismiss); and **vocabulary-limited** (no existing fact expresses the scope exactly, and a new one would not earn its friction). Both need the reason written down.
* **Mis-targeted** — fails a test, or uses the wrong mechanism for its scope: a standing flag on something conditional; presence for a consequence; a condition for a preventive; a dimension-shared fact instead of a scope fact; a question whose `when` doesn't reach the scope. Re-shape before publishing.

> A **dark** entry — no valid trigger and not standing, so it never surfaces — is an automatic fail. The Triage tab flags these; treat one as unfinished. But the validator only catches *structurally* dark entries. An entry made dark by a question's `when` (Step 3E), or by an exclude with no receiving entry, is invisible to it. That is what Step 4 is for.

---

## Traps to avoid

* **Reader appetite in the trigger.** Any mechanism that lets the reader decide *in advance* whether an entry is relevant to them, rather than describing the job. The deleted universal opt-ins were exactly this. Muting belongs in the results display, never in the logic.
* **A gate used as shorthand.** `slab-suspended` standing in for "any slab", `footing` for "anything in the ground". The entry's own scope will contradict the trigger; read them side by side.
* **A conflated fact.** One fact carrying two meanings, so ticking it for one silently withholds the entries that needed the other.
* **The hidden `when`.** A trigger on a question whose `when` gates don't cover the entry's scope. Structurally valid, silently dark. (Step 3E.)
* **Dimension-lumping.** Triaging every entry in a dimension through one shared fact. Triage each entry by *its own* scope; entries in the same dimension will often use quite different mechanisms.
* **Importance inflation.** Broadening a trigger — or marking an entry standing — because it *feels* critical. Importance lives in the bands, not the reach. `standing` means *universal in scope*, not *important*.
* **Preventive/consequence mix-up.** Firing a "since the condition is true, watch out" entry on bare presence (over-fires), or firing a "keep it simple before you decide" entry on the condition it is trying to prevent (reaches nobody in time).
* **The single-entry question that doesn't earn it.** A question gating one entry is fine *only* if the entry is truly irrelevant when the answer is "no." Ask: on a job where the gate is on but the answer is "no," was the entry ever relevant? If no, the question is doing nothing.
* **Silent recall loss.** Precision failures are visible to the reader; recall failures are invisible. Audit every AND slot, question, `when` and exclude against the recall test specifically.
* **OR / AND confusion.** `[['a','b']]` is *a or b* (one slot). `[['a'],['b']]` is *a and b* (two slots). Writing an intended "and" as one slot fires far too often.
* **Exclude as a patch.** Reserve `triageExclude` for routing between genuinely competing entries; never to silence an entry a sloppy positive trigger over-fires. **And every exclude owes a receiving entry**: name the entry that picks the reader up on the excluded fact, and check its trigger actually fires there. An exclude with nothing behind it is a silent recall hole — the most dangerous defect in the system, and the validator cannot see it. Beware copying an exclude from a sibling: one that correctly routes a *system-choice* entry away will silently kill a *supply* or *detailing* entry that nothing supersedes.
* **The self-silencing question.** A question whose answer is biased toward hiding the entry — usually because it asks the author to grade their own work. The problem is the bias, not that it's a judgment; the fix is to reframe as an additive "would X help?", not to pretend a real judgment call is an observable fact.
* **Vocabulary drift.** A trigger referencing a fact not defined in `triageConfig` never fires (flagged as an unknown fact). Add the gate or question first, then build on it.

---

## Standing entries

A standing entry has `standing: true` and no trigger. It surfaces on every triage run, grouped separately from the job-specific results.

The bar is **scope, not importance**: the honest scope sentence must be *"on every reinforced-concrete job."* Three entries meet it — every RC job has formwork to build, load and strip; every drawing set carries reinforcement callouts; every drawing set carries details and schedules.

An entry is *not* standing because it is important, or because it is hard to trigger, or because it belongs to a dimension that feels general. If you can name a real RC job on which it doesn't apply, it isn't standing — find the fact that names that job.

Standing entries are why triage does not need an opt-in. Advice is either universal (→ standing, always shown) or conditional (→ a question). An opt-in is a third thing nothing actually needs, and it fails in the worst direction: default-off means the reader who has never considered the advice is the one who never sees it.

**Reader fatigue is handled downstream.** A reader who has internalised the standing entries can collapse or hide the group in the results view — a remembered display preference, not a question in the flow. The test for whether something is a triage fact at all: *does the answer change from job to job?* "Have I read this before" doesn't. It isn't a triage fact.

---

## Writing the "Surfaces when…" summary

The Triage tab renders each trigger in plain English. Read it back and check it against the scope sentence from Step 1: if the two don't say the same thing, the trigger is wrong however the logic reads. A good trigger is **legible** — a maintainer who has never seen the entry should read the "Surfaces when…" line and agree it targets the right jobs.

---

## When to revisit a trigger

Re-check an entry's trigger when:

* a **new gate, condition or question** is added that could carry this entry's scope more precisely;
* a **question's `when` changes** — this silently changes the reach of every entry triggered on that question;
* a **new entry** shares this one's scope — decide whether they should share a fact (family consistency) or whether one should `triageExclude` the other (routing);
* an entry that **receives** an exclude changes its own trigger — the excluding entry may now be handing readers to nobody;
* the entry's **scope changes** (its bands or applicability narrow or widen), which usually moves the recall boundary;
* the Triage tab's **validation** flags the entry as dark or referencing an unknown fact;
* readers report it surfacing where it doesn't belong (precision), or *not* surfacing on a job where it clearly applied (recall — take this one seriously).

Because triggers share a fact vocabulary, editing a gate or question can shift several entries at once — **re-run the simulator after any change to `triageConfig`.**

---

## Worked examples

**Standing, correct (genuinely universal scope).** `formwork-and-falsework-complexity` applies wherever an RC design has to be formed, loaded and stripped — every RC job, without exception. It is also a *Safety in Design* entry. It once sat behind the default-off `universal-buildability` toggle, which meant the reader who had never thought about avoidable falsework complexity was exactly the reader who never saw it. Universal scope, not optional → **`standing: true`**. Same for `reinforcement-callout-clarity` and `details-and-schedule-references`.

**Presence-only, correct (whole-of-element scope).** `bored-concrete-piles-vs-screw-piles` triggers on `[['pile']]`. Every piled job should weigh the pile-type choice, so recall must be total and precision is already high — any refining question would only drop relevant jobs. The simplest shape is the right one → **well-targeted**.

**Presence AND condition, correct (element + state).** `chamfered-exposed-external-corners` triggers on `[['wall','column','beam-suspended'],['exposed-concrete']]`. On `wall` alone it would fire on the majority of walls never on show; the condition gate confines it to jobs where a sharp exposed arris is actually there. `beam-suspended` is in the slot because the entry's own scope names beam edges and parapets — the element slot is set by the scope sentence, not by the entry's title → **well-targeted**.

**A family split preventive vs consequence, on one shared question (the model case).** Four sibling entries concern 20 mm-plus slab bars, across four dimensions. The *preventive* one, `hand-bendable-bar-sizes-for-slab-reinforcement` ("keep bars to 12–16 mm where practical"), fires on presence — `[['slab-suspended','slab-on-ground']]` — so it reaches every slab designer *before* bar sizes are locked. The three *consequence* entries — on-site bending plant (Logistics), grinder cutting (Safety) and callout clarity (Communication) — all fire on `[['large-bars']]`, a single drawings question. One cheap question sharpens three entries at once and keeps the preventive/consequence split honest.

The shape was always right; the **reach** was not. `large-bars` was originally `when`-gated on `slab-suspended` alone, so on any job without a suspended slab — a house on a waffle raft with N20s in the ribs — the question was never asked and all three consequence entries were dark. Nothing in the triggers showed it, and the validator could not see it. Fixed by broadening the question's `when` to `slab-suspended` **or** `slab-on-ground` (Step 3E) → all four **well-targeted**.

**A judgment question, aimed correctly.** `isometric-overview-views-in-structural-drawing-sets` is gated on `benefit-from-isometric`: *"Could the overall design, or a detail within it, be easier to build if the set included an isometric or 3D view?"* An earlier attempt objectified this into "does the structure step, slope or transfer?" — which quietly narrowed the real question, since a simple frame can still be confusing and a fiddly detail on a plain building can too. The honest question here *is* a judgment; the only thing to engineer out is the bias, done by asking "would this help?" rather than "are your drawings unclear?" Its `when` now covers every element gate, because the entry's own scope names ground beams, pile caps and retaining walls — the jobs previously never asked → **well-targeted**.

**Wrong mechanism fixed — opt-in to condition.** `temporary-stability-of-retained-or-part-built-structure` once sat behind the default-off `universal-site-safety` opt-in. But its scope is not universal (it applies only where retained, existing or part-built structure must stay standing mid-build) and not optional (it is a safety review nobody should have to switch on). Both facts point away from an opt-in. It now triggers on `[['retained-or-staged']]`, a standalone project-context condition gate → **well-targeted**. Scope that is conditional-and-not-optional belongs on a condition. Scope that is universal-and-not-optional is **standing**. Neither is ever an opt-in — which is why the mechanism no longer exists.

**One fact doing two jobs — split.** `watertight` once meant both *"the structure must hold water out or in"* (basements, tanks, lift pits) and *"this deck carries a membrane"* (bathrooms, balconies, podiums, planters). Its label led with "Basement or watertight structure", so on a house with a bathroom and a balcony and no basement, nobody ticked it — and `waterproofing-buildability` silently vanished from exactly the jobs it was written for. Split into `water-retaining` (gating the two wall entries) and `wet-or-drained-slab` (gating the slab entry). A conflated fact is a **vocabulary** defect, not a trigger defect — no trigger could have fixed it.

**Exclude for routing, correct — and the copy that wasn't.** `raft-slab-vs-waffle-pod` triggers on `[['slab-on-ground']]` and carries `triageExclude: ['reactive-ground']`. Waffle-vs-raft is the right question on ordinary ground; on reactive ground a more specific system-selection entry supersedes it, and that entry demonstrably fires on `reactive-ground`. The exclude has a receiving entry → correct.

The same exclude had been copied onto `waffle-pod-depth-availability` — and there it was a silent recall hole. Pod-depth availability is a **supply** question: whether the specified depth is a stocked size. Nothing supersedes it on reactive ground, and a waffle raft on reactive clay is the single most common job the entry exists for. The exclude was silencing it on precisely its home ground. Removed. **Never copy an exclude from a sibling without naming the receiving entry.**
