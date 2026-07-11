# Evidence rating rubric

How to assign the **evidence support** level (`high` / `medium` / `low`) to a framework entry, consistently, regardless of who is reviewing.

This is the rule maintainers follow when setting `evidenceSupport.level` and writing `evidenceSupport.summary` in the Data Manager. It is the maintainer-facing version of the explanation shown to readers on the site's Evidence support index — same logic, more detail.

---

## The core principle

> The rating measures **how much a reader can trust the specific numbers, or the specific recommendation, that the entry asks them to act on** — *not* whether the underlying effect or mechanism is real.

Most entries hand the reader **cut-off numbers** (e.g. fold depth `≤ 600 / 600–1000 / > 1000 mm`). Some instead hand them a **choice** (e.g. *chamfered / not chamfered*). The rating is about how well the cited evidence backs those cut-offs or that choice.

A strong, well-evidenced *mechanism* does not by itself earn a high rating. The question is always: **does the evidence support the actual numbers (or the recommended call)?** This distinction is the single most common source of inconsistent ratings, so it comes first.

---

## How a rating is decided — three questions

Every level below is just a combination of the answers to three questions. Keep all three in mind; a rating is never decided by any one of them alone.

1. **Strength** — what *kind* of evidence sits behind the entry? Measured on site, derived from real component dimensions, set by a code or standard, taken from a study, or based on experience? The hierarchy in Step 3 ranks these.
2. **Coverage** — does that evidence back **every** cut-off (or the whole recommended choice), or only part of it? One backed cut-off out of three is partial coverage.
3. **Corroboration** — does **more than one independent source** point the same way (a second source, or a documented real case)? A single source on its own is never enough for `high`.

`high` = strong evidence **and** full coverage **and** corroboration. `medium` = good support but a cut-off (or the exact call) is a reasoned judgement, or only one leg, or an analogous base. `low` = mostly judgement or loose analogy with nothing to confirm it.

---

## Step 1 — Classify the parameter

Every entry's parameter is one of two kinds. Decide which before you grade, because they are tested differently.

* **Numeric** — the bands are divided by values: millimetres, counts, volumes, percentages (e.g. fold depth `≤ 600 / 600–1000 / > 1000 mm`).
* **Categorical** — the bands are named choices or practices with no numeric boundary (e.g. *chamfered / not chamfered*; *socket into rock / cast from top / entry into shaft*).

## Step 2 — Apply the matching test

This is the **coverage** question (question 2) made concrete.

**Numeric parameter — the per-cut-off test:**
For **each** cut-off (each band boundary), ask: *can I point to a measurement, a physical/first-principles derivation, or a code/standard provision behind this specific number?*

* If **every** cut-off traces to one of those → the numbers are evidenced.
* If **one or more** cut-offs is a reasoned round number or a judgement call → the numbers are only partly evidenced, regardless of how strong the effect is. That caps the entry at `medium`.

**Categorical parameter — the recommended-call test:**
There are no numeric cut-offs to defend, so ask instead: *is the recommended choice (and the ordering of the options) backed by an authoritative, on-point source or duty* — a standard, code, regulator requirement, peer-reviewed study, or primary research conducted for the framework — *rather than by general/analogous literature or unaided judgement?*

> Do **not** cap a categorical entry at medium just because it has no measured numbers. It has no numbers to measure. Judge it on whether the call is backed.

## Step 3 — Weigh the evidence (the hierarchy)

This is the **strength** question (question 1). Use it to weigh what the cut-offs (or the call) actually rest on.

**Evidence hierarchy — strongest to weakest:**

1. Direct measurement / field data on the same element or parameter.
2. First-principles physical derivation from established component dimensions or mechanics.
3. Regulatory duty or mandatory code provision (especially for safety and communication entries).
4. Peer-reviewed research directly on point.
5. Authoritative industry standard or guidance directly on point (e.g. SRIA, CCAA, RTA technical notes).
6. Primary research conducted for the framework (e.g. a structured supplier-availability review).
7. Documented real project case (a concern/recommended example that actually occurred).
8. Industry or contractor consultation.
9. General or analogous literature — the right phenomenon studied in a different domain, applied by inference.
10. Unaided practitioner judgement.

**Which items can do which job.** Items **1–6** are *cut-off-grade*: they can set where a numeric boundary sits, or directly back a categorical call. Item **7** (a documented real case) is *corroboration-grade* — it rarely sets a general numeric cut-off on its own (one project is one scenario), but it is exactly what confirms a cut-off or a call that strong evidence has already established. Items **8–10** are *supporting or suggestive only*. This split is why a lone real-project example, however vivid, is not a `high` by itself: it is the corroboration leg, not the evidence that fixes the numbers.

## Step 4 — Assign the level

**`high`** — Two legs, both present:

1. **Strength + coverage** — every numeric cut-off (or the recommended call) rests on items **1–6**, directly on point; and
2. **Corroboration** — at least one independent source *or* a documented real case (item 7 or another item 1–6) points the same way.

Use the numbers broadly as written. Any residual uncertainty is about the *precision of a single value* or *how often the situation occurs* — not about whether the cut-offs sit in the right place. **One source alone is never `high`**, no matter how authoritative.

**`medium`** — The issue is well established and genuinely supported (a real example or relevant source backs it), **but** at least one of the following holds:

* one or more cut-offs (or the exact ordering of a categorical call) is a reasoned judgement (items **8–9**) rather than measured, derived or set by a standard; **or**
* the evidence base is general/analogous rather than directly on point; **or**
* there is real support but only one leg — strength without independent corroboration, or a single case without strong cut-off evidence behind it.

Treat the numbers as a well-founded starting point; the reader should apply their own judgement to their project.

**`low`** — Rests mainly on items **9–10**: practitioner assertion or loosely analogous material, with no corroborating measurement, derivation, standard, duty, or documented case. The cut-offs are essentially arbitrary.

> A `low` entry can still be published live. Publishing it is what makes the gap visible and invites the measurement, source or field experience that would raise it — so `low` is a signal that an entry needs more evidence, and an open invitation to supply it, not a bar to release. A maintainer who receives a submission that only reaches `low` may publish it as `low`, or research it further and publish it at `medium` or `high`. It is fine and expected for a dataset to contain no `low` entries — as here, where each was researched to at least `medium` before release — but that reflects the effort put in, not a rule against publishing `low`.

---

## Traps to avoid

These are the specific ways ratings drift if the rubric isn't applied deliberately.

* **Mechanism inflation.** A measured, peer-reviewed *effect* does not make the *cut-offs* high if the boundary positions are judgement. (Worked example: a formwork-cycling saving can be measured while the floor-count bands that trigger "concern" vs "action" are a reasoned call — that is a `medium`.)
* **Single-leg high.** Strength *or* a real case is not enough on its own — `high` needs both the cut-offs/call evidenced **and** an independent confirmation. A single on-point standard with no example, or a single example with no underlying evidence, is `medium`.
* **Categorical mis-capping.** A categorical parameter has no numeric cut-offs; judging it as if it needed measured thresholds wrongly caps it at medium. Judge the call, not absent numbers. A real case + an on-point authoritative standard is a legitimate two-leg `high`.
* **Single-scenario figures.** A number taken from one modelled or observed scenario and presented as a general cut-off is medium-grade *for that cut-off*, even when the source is peer-reviewed.
* **Frequency vs magnitude.** If a cut-off encodes a *measured magnitude* (e.g. a grade-down that equals a measured strength penalty), then uncertainty about *how often* the situation arises affects applicability/scope — not the cut-off's evidence grade. Don't demote on frequency uncertainty alone.
* **One-source breadth.** A single authoritative, directly on-point source can anchor the strength leg of a `high` (especially for categorical calls), but still needs corroboration. A single *general or analogous* source cannot anchor it at all — that's `medium` at best.

---

## Writing the `summary`

One or two plain-language sentences a reader can trust. State **what supports the entry** and **its main limitation**, in that order — this mirrors the two legs above.

Pattern: *"[What the cut-offs / call rest on, strongest first]; [the main thing that is reasoned, narrow, single-source, or assumed]."*

Good summaries name the limitation honestly (single scenario, reasoned cut-offs, narrow base, one leg, assumed frequency) rather than implying the evidence is stronger than it is. The limitation clause is what lets a reader calibrate how hard to lean on the numbers — and it should make the level self-explaining: a `high` summary names only precision/frequency doubts, a `medium` summary names the reasoned cut-off or the missing leg.

---

## When to re-rate

Set the entry's `dateReviewed` whenever you assign or change a level. Re-rate an entry when:

* new evidence is added (a study, a standard, a measured value, another real case) that moves a cut-off from reasoned to evidenced — or supplies the missing corroboration leg — or vice versa;
* the parameter or band boundaries themselves are changed;
* an accepted edit suggestion alters the cut-offs or the supporting evidence.

A change in level should always be accompanied by an updated `summary` so the two never contradict each other.

---

## Worked examples

Two short applications of the rubric, to anchor the boundary.

**Numeric, capped at medium (coverage fails).** An entry's effect is supported by measured field research, but its bands are floor counts (`1 / 2–3 / 4–5 / 6+`) and nothing in the evidence pins those boundaries — they mark where a compounding saving is judged to become material, and the underlying per-floor figure is from a single scenario. The mechanism is high-grade; the *cut-offs* are reasoned → **medium**.

**Categorical, promoted to high (two legs present).** An entry's parameter is a detailing choice (*detailed with cover kept / cover not coordinated / omitted*), and an authoritative industry technical note addresses that exact detail and recommends exactly that response (strength leg), backed by real project examples (corroboration leg). There are no numeric cut-offs to defend, the call is directly evidenced, and a second source confirms it → **high**.

**Numeric, lone case (the one to watch).** An entry has a single documented project where a concern arose and an action was taken, and the cut-offs are drawn from that one project. That is item 7 only — one leg, one scenario, no independent confirmation and no cut-off-grade evidence behind the numbers → **medium** at best, and `low` if the numbers are essentially asserted. A lone example is never `high`.

---
