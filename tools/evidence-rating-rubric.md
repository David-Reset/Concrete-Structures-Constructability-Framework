# Evidence rating rubric

How to assign the **evidence support** level (`high` / `medium` / `low`) to a framework entry, consistently, regardless of who is reviewing.

This is the rule maintainers follow when setting the `evidenceSupport.level` and writing the `evidenceSupport.summary` in the Data Manager.

\---

## The core principle

> The rating measures \*\*how well the cited evidence supports the entry's parameter and threshold bands\*\* — the specific values or choices a reader acts on — \*\*not\*\* whether the underlying effect or mechanism is real.

A strong, well-evidenced *mechanism* does not by itself earn a high rating. The question is always: **does the evidence support the actual numbers (or the recommended call) in the bands?**

This distinction is the single most common source of inconsistent ratings, so it comes first.

\---

## Step 1 — Classify the parameter

Every entry's parameter is one of two kinds. Decide which before you grade, because they are tested differently.

* **Numeric** — the bands are divided by values: millimetres, counts, volumes, percentages (e.g. fold depth `≤ 600 / 600–1000 / > 1000 mm`).
* **Categorical** — the bands are named choices or practices with no numeric boundary (e.g. *chamfered / not chamfered*; *socket into rock / cast from top / entry into shaft*).

## Step 2 — Apply the matching test

**Numeric parameter — the per-band-edge test:**
For **each** band boundary, ask: *can I point to the measurement, the physical/first-principles derivation, or the documented real case behind this specific number?*

* If **every** edge traces to one of those → the thresholds are evidenced.
* If **one or more** edges is a reasoned round number or a judgement call → the thresholds are partly unevidenced, regardless of how strong the effect is.

**Categorical parameter — the recommended-call test:**
There are no numeric edges to defend, so ask instead: *is the recommended choice (and the ordering of the options) backed by an authoritative, on-point source or duty* — a standard, code, regulator requirement, peer-reviewed study, or primary research conducted for the framework — *rather than by general/analogous literature or unaided judgement?*

> Do \*\*not\*\* cap a categorical entry at medium just because it has no measured numbers. It has no numbers to measure. Judge it on whether the call is backed.

## Step 3 — Assign the level

Use the evidence hierarchy below to weigh what the thresholds (or the call) actually rest on.

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

**`high`** — Every threshold edge (numeric), or the recommended call (categorical), rests on items **1–7**, directly on point. Corroborated by a real example or an authoritative source. Any residual uncertainty is about the *precision of a single value* or *how often the situation occurs* — not about whether the bands sit in the right place.

**`medium`** — The mechanism is well supported and at least one real example or relevant source backs the entry, **but** one or more threshold edges (or the specific ordering of a categorical call) is reasoned/judgement (items **8–9**) rather than measured or derived; **or** the evidence base is general/analogous rather than directly on point.

**`low`** — The recommendation rests mainly on items **9–10**: practitioner assertion or loosely analogous material, with no corroborating measurement, derivation, standard, duty, or documented case. Thresholds are essentially arbitrary.

> If no entry in your dataset is `low`, that is fine and expected — a `low` entry generally should not be published as live. Treat `low` as a signal that the entry needs more evidence before it goes out, not as a normal resting state.

\---

## Traps to avoid

These are the specific ways ratings drift if the rubric isn't applied deliberately.

* **Mechanism inflation.** A measured, peer-reviewed *effect* does not make the *bands* high if the band positions are judgement. (Worked example: a formwork-cycling saving can be measured while the floor-count bands that trigger "concern" vs "action" are a reasoned call — that is a medium.)
* **Categorical mis-capping.** A categorical parameter has no numeric edges; judging it as if it needed measured thresholds wrongly caps it at medium. Judge the call, not absent numbers.
* **Single-scenario figures.** A number taken from one modelled or observed scenario and presented as a general threshold is medium-grade *for that threshold*, even when the source is peer-reviewed.
* **Frequency vs magnitude.** If a threshold encodes a *measured magnitude* (e.g. a grade-down that equals a measured strength penalty), then uncertainty about *how often* the situation arises affects applicability/scope — not the threshold's evidence grade. Don't demote on frequency uncertainty alone.
* **One-source breadth.** A single authoritative, directly on-point source can support a `high` (especially for categorical calls). A single *general or analogous* source cannot — that's medium at best.

\---

## Writing the `summary`

One or two plain-language sentences that a reader can trust. State **what supports the entry** and **its main limitation**, in that order.

Pattern: *"\[What the thresholds/call rest on, strongest first]; \[the main thing that is reasoned, narrow, or assumed]."*

Good summaries name the limitation honestly (single scenario, reasoned bands, narrow base, assumed frequency) rather than implying the evidence is stronger than it is. The limitation clause is what lets a reader calibrate how hard to lean on the numbers.

\---

## When to re-rate

Set the entry's `dateReviewed` whenever you assign or change a level. Re-rate an entry when:

* new evidence is added (a study, a standard, a measured value, another real case) that moves a threshold edge from reasoned to evidenced — or vice versa;
* the parameter or band boundaries themselves are changed;
* an accepted edit suggestion alters the thresholds or the supporting evidence.

A change in level should always be accompanied by an updated `summary` so the two never contradict each other.

\---

## Worked examples

Two short applications of the rubric, to anchor the boundary.

**Numeric, demoted to medium.** An entry's effect is supported by measured field research, but its bands are floor counts (`1 / 2–3 / 4–5 / 6+`) and nothing in the evidence pins those boundaries — they mark where a compounding saving is judged to become material, and the underlying per-floor figure is from a single scenario. The mechanism is high-grade; the *thresholds* are reasoned → **medium**.

**Categorical, promoted to high.** An entry's parameter is a detailing choice (*detailed with cover kept / cover not coordinated / omitted*), and an authoritative industry technical note addresses that exact detail and recommends exactly that response, backed by real project examples. There are no numeric edges to defend, and the call is directly evidenced → **high**.

\---

