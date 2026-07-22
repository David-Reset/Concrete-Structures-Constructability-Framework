# Evidence rating rubric

How to assign an entry's **evidence support** level — `established` / `directional` / `indicative` / `reasoned` — consistently, regardless of who is reviewing.

This is the rule maintainers follow when setting `evidenceSupport.level` and writing `evidenceSupport.summary` in the Data Manager. It is the maintainer-facing version of the explanation shown to readers on the site's Evidence support index — same logic, more detail.

---

## The core principle

> The rating measures **how much a reader can trust the specific numbers, or the specific recommendation, that the entry asks them to act on** — *not* whether the underlying effect or mechanism is real.

A strong, well-evidenced *mechanism* does not by itself earn a strong rating. The question is always: **does the evidence back the thing the reader actually acts on?**

> **The rating describes the evidence. It never issues an instruction.**
>
> No level tells an engineer what to do, and no level — including the top one — invites them to stop applying their own judgement. The reader is a professional carrying the design responsibility; the framework is not. What the rating tells them is **how much of this entry rests on evidence and how much rests on our judgement**, and therefore **where their own scrutiny has the most work to do.**
>
> Never write a level, a gloss or a summary that reads as *"use this as-is."* That is not what any of these levels mean, and it is not the framework's place to say it.

This distinction is the single most common source of inconsistent ratings, so it comes first — and it is why the scale has a level for *"the mechanism is proven, the number is ours."* That state is the most common one in this framework. It is not a deficiency. It has a name.

---

## Step 1 — Read the entry's kind off the quality rubric

Entries come in **four kinds**, defined in section 6 of the [entry quality rubric](entry-quality-rubric.md): **measured**, **chosen**, **judged**, **counted**. Each is tested differently, so establish the kind first — and **take it from the entry as framed. Do not re-derive it from the look of the bands.**

| Kind | What the reader acts on | What must be evidenced |
|---|---|---|
| **Measured** — a value read off the drawings that could land anywhere on a continuum | the **cut-offs** | the mechanism **and every cut-off** |
| **Chosen** — a selection from a menu of real options (*including numbers off a standard menu*) | the **call** | the recommended call **and the ordering of the options** |
| **Judged** — described states, assessed clearest to least clear | the **call** | the recommended call **and the ordering of the states** |
| **Counted** — how many named preconditions fail | the **conditions** and the **breakpoint** | every condition **and where the count starts to matter** |

> **The trap this table exists to prevent.** A parameter with millimetres in it is **not** automatically *measured*. Bar spacing (150 / 200 / 250 / 300), bar diameter (N12 / N16 / N20), pod depth (225 / 300 / 375) and fire-resistance levels come off a **standard menu** — the quality rubric calls these **chosen**, and so must this one. Asking for cut-off evidence at 260 mm demands a boundary no drawing ever lands on. **A menu value is a call, not a cut-off.**

---

## Step 2 — Grade every source on two axes

This is the heart of the rubric. A source has to clear **both** axes to evidence anything. Grading on one alone is what lets a strong-but-irrelevant source be smuggled into a slot it has not earned.

### Axis 1 — Source grade (how much weight the *type* of source can bear)

**Grade A — can fix a number.**
- Direct measurement or field data on the same element or parameter
- First-principles physical derivation from established component dimensions or mechanics
- Peer-reviewed research
- A **statutory duty** bearing on how the thing gets built — a WHS Regulation, the duty provisions of a Work Health and Safety Code of Practice, the Design and Building Practitioners Act

> **Design codes are deliberately not part of the evidence base — do not add them.**
>
> AS 3600, AS 4100 and their companions are **the engineer's own ground**. They already apply them, they are bound by them, and restating them tells a reader nothing they do not know. More to the point: **the framework exists for the constructability question the standard does not answer.** A design code tells you the section works. It does not tell you whether anyone can form it, reach it, bend it on site, or stand next to it safely — and that is the entire subject of this framework.
>
> An entry whose case rests on a design standard is either restating the code (and should be deleted), or has mistaken a compliance question for a constructability one (and should be reframed).
>
> Two narrow uses are legitimate, and neither is evidence: **vocabulary** (AS 2870 is cited for the site-classification terms suppliers label their pods by), and **boundary-marking** (naming the standard that governs a matter precisely in order to say the entry is *not* trespassing on it, and that it stays the engineer's responsibility). Both are context. Neither grades.
>
> **This excludes design codes — not materials and product standards.** AS/NZS 4671 is a *materials* standard: it records that the rebend test applies to deformed bars of 16 mm and smaller, with no equivalent above. That is a **physical and manufacturing fact about the steel**, not an instruction to a designer, and it is admissible as Grade B — it can fix a number precisely because the number is a physical fact. The test is simple: *does the document tell the engineer how to design, or does it record how the material or product actually behaves?* The first is theirs. The second is evidence.
>
> **Where a duty is cited as Grade A, it is a WHS or regulatory obligation about the act of construction — not a design code.** That distinction is the whole point.

**Grade B — can back a call, and can fix a number where the number is a physical or regulatory fact.**
- The **advisory content** of a regulator's Code of Practice or published guidance — the practical how-to, as distinct from the duty it implements
- Regulator research or a regulator's published findings (a VBA water-ingress report, a Building Commission defect study)
- Authoritative industry technical note or guidance (SRIA, CCAA, ACI, CIRIA, Engineering NZ) — a *technical note*, which is a different thing from a design code
- A **materials or product standard** recording a physical or manufacturing fact (AS/NZS 4671 on which bar sizes the rebend test covers) — again, not a design code
- Government or agency research synthesis (NCHRP, NBS)
- Doctoral thesis; established reference textbook
- Primary research conducted for the framework (e.g. a structured supplier-availability review)

**Grade C — can corroborate a claim. It can never evidence one.**
- Documented real project case (a `concern` / `recommended` example that actually occurred)
- Manufacturer or supplier product data
- Trade or contractor guidance; industry consultation
- Unaided practitioner judgement

> **Grade the provision, not the document.** A Code of Practice carries both kinds of content at once. The **duty** it imposes — *designers must eliminate the need to enter a confined space so far as is reasonably practicable* — is Grade&nbsp;A: it is an obligation, and it binds. The **practical advice** around that duty — recommended clearances, suggested methods — is Grade&nbsp;B. Cite which one you are leaning on, because they do not carry the same weight. The same discipline applies to a textbook, a technical note, or a journal paper: you grade the claim you are actually using, not the cover of the thing it came in.

### Axis 2 — Proximity (what the source is actually *about*)

- **On point** — it addresses the proposition the reader acts on.
- **Adjacent** — it addresses a *neighbouring* proposition. A source about a chamfer on a precast cladding joint is adjacent to a claim about a formed in-situ arris. A drafting manual that sets the standard chamfer size corroborates a **drawing convention**, not a **damage claim**.
- **Analogous** — the right phenomenon, studied in a different domain, applied by inference. Visual-clutter research on general displays, applied to reinforcement callouts. Pipefitting drawing studies, applied to RC structural sets.

### The rule that does all the work

> **A claim is *evidenced* only by a Grade A or Grade B source that is *on point*.**
>
> **Adjacent** or **analogous** caps the entry — however good the source is. A peer-reviewed paper about the wrong thing is still about the wrong thing.
>
> **Grade C never evidences a claim.** It corroborates one that Grade A or B has already established.

---

## Step 3 — Test independence, and test it on the same claim

`established` needs a second leg. Two rules govern what counts.

**Independence.** Two sources are independent only if they **could have disagreed** — different authors, different evidence base, different organisation.

The following are **one source, not two**:
- Two publications from the same body (SRIA Technical Note 4 and SRIA Issue 42/4)
- Parts I and II of the same review, by the same authors
- Two jurisdictions adopting the same model law (a SafeWork NSW and a SafeWork SA code implementing the model WHS Regulations)
- A thesis and the journal paper drawn from it
- A source and another source that merely cites it

**The corroborating source must be on point — on the same claim.** A second leg that supports a *neighbouring* proposition is not corroboration; it is a second entry's evidence, wearing this one's badge. If the claim is *"a chamfer prevents arris damage,"* a manual specifying that standard chamfers are 20 × 20 does not corroborate it. It corroborates that the convention exists.

> This is the rule most often broken, and it is broken in good faith — by a reviewer stacking up sources that all feel relevant. Before you count a leg, say out loud: *the claim is ___, and this source says ___.* If those are different sentences, it is not corroboration.

---

## Step 4 — Assign the level

Work down. The level is set by the **weakest** link, not the strongest source.

### `established` — *evidenced on point, and independently confirmed*
Everything the reader acts on rests on **on-point Grade A or B** evidence, and is **independently corroborated on the same claim** (by another on-point A or B source, or by an on-point Grade C documented real case).

For a *measured* entry that means **every cut-off**. For *chosen* or *judged*, the call **and its ordering**. For *counted*, **every condition and the breakpoint**.

This is the strongest evidence the framework carries. The residual uncertainty is about the precision of a single value, or how often the situation arises — not about whether the guidance sits in the right place.

It is **not** an instruction to adopt the numbers unexamined. An engineer's own checks, and their responsibility for the design, are undiminished at this level. What `established` says is narrow and factual: *we could not find the weak link.*

### `directional` — *the direction is proven; the number is ours*
**The mechanism and direction are evidenced on point by Grade A or B — but a link is missing.** One or both of:

- **Coverage.** The specific values the reader acts on are *reasoned*: a measured entry's cut-offs, a counted entry's breakpoint, or the gradation between a chosen/judged entry's states. The direction is proven; the number is the framework's.
- **Corroboration.** The call is fully and directly evidenced by an on-point A or B source, but nothing independent confirms it — a single authority, or a single documented case.

**What is evidenced here is the direction. The specific value is the framework's reasoned call** — and that is precisely the part an engineer should expect to weigh against their own job, because it is the part we cannot show them a source for.

> **This is the framework's home.** Most good constructability entries live here, and that is not a failing. A measured mechanism with a reasoned cut-off is an honest, useful, well-founded entry — and it is materially different from an entry that is mostly reasoning. Before this level existed, the two were both called "medium," and readers could not tell them apart.
>
> **The name is doing a job.** It tells a reader exactly how far to lean: *believe the direction, sanity-check the number.* Do not let a later reviewer rename it back to something that sounds like a grade — it is not a grade, it is an instruction.

### `indicative` — *plausible, but the evidence is about something else*
**The evidence base is not on point.** The claim rests on **adjacent** or **analogous** sources — however strong their grade — or the only on-point support is Grade C.

The direction here is *plausible* rather than proven — that is the line between this level and `directional`. The reasoning is sound, but nothing directly evidences the proposition the reader acts on, so the entry is carried by inference.

### `reasoned` — *practitioner judgement, published so the gap is visible*
Rests mainly on **Grade C**: practitioner judgement, trade guidance, or loosely analogous material, with nothing on point to confirm it. The call is essentially asserted.

> **A `reasoned` entry can still be published live, and should be.** Publishing it is what makes the gap visible and invites the measurement, source or field experience that would raise it. `reasoned` is an open invitation to supply evidence, not a failing grade and not a bar to release. A maintainer may publish at `reasoned`, or research further and publish higher.
>
> **`reasoned` does not mean nobody tried.** Distinguish the two cases in the summary, because they call for different action: *the research exists and this entry has not cited it* (go and cite it), versus *the study does not exist* (a real hole in the literature — say so plainly, and the entry becomes the record of that hole).

---

## Step 5 — Apply the matching test

**Measured — the per-cut-off test.** For **each** band boundary: is there an on-point Grade A or B source behind *this specific number* — a measurement, a physical derivation, a code provision, or a physical product standard? Every cut-off must clear it. One reasoned round number caps the entry at `directional`.

**Chosen and judged — the recommended-call test.** There are no cut-offs to defend, so ask instead: is the recommended choice — **and the ordering of the options or states** — backed by an on-point Grade A or B source? Do **not** cap a chosen or judged entry because it has no measured numbers. It has none to have. This holds for a menu of millimetres exactly as it holds for a menu of words.

**Counted — the conditions test.** Both halves need evidence:
1. **The condition list.** Is each named condition itself supported on point, and genuinely a precondition? This is the substance, and where the evidence usually is.
2. **The breakpoint.** Why does the rating change at *that* count — why is `2 or more` the concern and not `3`? This is almost always reasoned; nothing in the literature says two failed preconditions is where a waffle pod stops being right.

> **A counted entry caps at `directional` unless the breakpoint itself is sourced.** A fully-evidenced condition list with a judged breakpoint is a strong `directional`, not an `established`. Say so: *"each precondition is supported by X; where the count becomes material is a reasoned call."*

---

## Traps to avoid

* **Mechanism inflation.** A measured, peer-reviewed *effect* does not lift the *cut-offs* if the boundaries are judgement. That is `directional`, and the whole point of the level.
* **Grade laundering.** A Grade A source that is *adjacent* does not become on-point by being peer-reviewed. Proximity is not negotiable by quality.
* **Leg-stacking.** Counting a source that supports a neighbouring proposition as the corroborating leg. State the claim and the source's finding as two sentences and compare them.
* **False independence.** Two documents from one organisation, two parts of one review, two jurisdictions under one model law, a thesis and its paper. One source, published twice.
* **Menu-number mis-capping.** Demanding cut-off evidence for `150 / 200 / 250 / 300`. There is no boundary at 260 to evidence, because no drawing says 260. Judge the call.
* **Categorical mis-capping.** The same error in words: judging a chosen or judged entry as if it needed measured thresholds.
* **Counted-breakpoint inflation.** A beautifully-sourced condition list still caps at `directional` if nothing sources the breakpoint. Evidencing *what* you count is not evidencing *where the count matters*.
* **Single-scenario figures.** A number from one modelled or observed scenario, presented as a general cut-off, is not evidence for that cut-off — even from a peer-reviewed source.
* **Frequency vs magnitude.** If a cut-off encodes a *measured magnitude*, uncertainty about *how often* the situation arises affects scope, not the evidence grade. Don't demote on frequency alone. If the real doubt is *which jobs this should reach*, that is a **triage** question — raise it there.
* **Rating by comparison.** Never set a level "for consistency with" a neighbouring entry. Comparison-based rules are circular: both entries drift together and no test fires. Every entry is judged **on its own, against this standard.** If entries come out inconsistent, the standard is underspecified and *the standard* gets sharpened.

---

## Writing the `summary`

One or two plain sentences a reader can trust. State **what supports the entry**, then **its main limitation** — mirroring the two legs.

Pattern: *"[what the call / cut-offs / conditions rest on, strongest first]; [the reasoned value, the missing leg, the adjacent base, or the assumed frequency]."*

The summary must make the level **self-explaining**:

- an `established` summary names only precision or frequency doubts;
- a **`directional` summary must say which link is missing** — the reasoned cut-off, the judged breakpoint, or the absent second source. This is the level's whole job;
- an `indicative` summary names what the evidence is *about*, and why that is not the same as the claim;
- a `reasoned` summary says whether the research **exists and is uncited**, or **does not exist**.

Two mechanical rules:
* **Never announce the level in the summary.** It renders in a chip beside the text. *"A strong directional. Backed by…"* is redundant and goes stale the moment the level changes.
* **A summary that names no limitation at all** is a red flag on anything below `established`.

> **A note on vocabulary, and why `directional` is called that.** The level names are ordinary words the summaries themselves need — a summary will legitimately say a claim is *supported by* a standard, that a mechanism is *well established*, or that a cut-off is *reasoned*. That is fine. What is banned is using the word **as a verdict on the entry**. The one name deliberately kept out of that pool is **`directional`**, because "supported" is the single most common verb in an evidence summary, and a chip reading `SUPPORTED` beside a sentence beginning *"Strongly supported by four studies…"* leaves a reader unable to tell whether the prose is stating the rating or describing the sources. Where a summary needs to say a claim is well backed, prefer **backed by, rests on, evidenced by, confirmed by, fixed by**.

---

## When to re-rate

Set `dateReviewed` whenever you assign or change a level. Re-rate when:

* new evidence moves a value from reasoned to evidenced, or supplies a missing corroboration leg — or vice versa;
* the parameter or band boundaries change;
* **the entry's *kind* changes** — a reframing from *measured* to *chosen*, or a *counted* parameter named for the first time, changes which test applies and can change the level with no new source at all;
* an accepted edit suggestion alters the guidance or the supporting evidence.

A change in level always comes with an updated `summary`, so the two never contradict.

---

## Worked examples

**Measured → `directional` (coverage fails).** Peer-reviewed research measures edge-formwork labour rising with vertical face depth, and three project cases confirm the response — including a fold that actually failed on site. But the 600 mm boundary comes from contractor consultation (Grade C) and the 1000 mm from that single case (Grade C). The mechanism is Grade A and on point; **neither number the reader acts on is evidenced.** → `directional`, and the summary says: trust the direction, treat 600 as indicative.

**Chosen → `directional` (corroboration fails).** A bar-size hinge is directly and authoritatively backed by an industry technical note — on point, Grade B, full coverage of the call. But every citation is from the same body, and there is no project case. One source, published twice. → `directional`, missing the second leg. *One independent source, or one documented case, would make it `established`.*

**Chosen → `established` (both legs).** A supplier-availability review conducted for the framework (Grade B, on point) establishes which pod depths are actually stocked, and project drawings using those depths corroborate it on the same claim (Grade C, on point). → `established`.

**Counted → `directional` (breakpoint unsourced).** Each of three waffle-pod preconditions traces to on-point guidance and a documented case. But nothing says the system should be reconsidered at *two* failures rather than three. Strong list, judged breakpoint. → `directional`.

**Judged → `indicative` (proximity fails).** Peer-reviewed visual-clutter research shows targets get harder to find as a display grows cluttered, and a real project records extras being missed in a compressed callout. But the research is about **general displays**, not engineering drawings — no study tests how reinforcement callouts are read by steel fixers. Grade A, but **analogous**. → `indicative`. The grade does not rescue the proximity.

**Judged → `reasoned` (nothing on point).** The literature is borrowed by analogy from a sibling entry, and the two drawing examples illustrate the principle rather than documenting a failure that occurred. → `reasoned`, and the summary should say the on-point study does not exist rather than implying it was not looked for.
