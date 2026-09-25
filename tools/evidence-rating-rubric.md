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

## Rating basis — what you rate, where, and when

- **Rate the entry as it stands, on the evidence it cites.** You may open a cited source and rerun a derivation from information in the entry. If you know of an uncited source that would change the level, that is a reason to **edit the entry** (cite it, then re-rate) — not to rate the entry as if it were already there.
- **Jurisdiction and date.** The framework is written for **New South Wales, Australia**. Some sources — WHS codes of practice above all — carry different weight in different places and can change weight when the law changes (Step 2). Grade them by their legal force **in NSW at the rating date**, and set `dateReviewed` so the date is on record.

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

> **Recognising the awkward one — *judged*.** *Measured* has a number, *chosen* has a menu, *counted* has a tally; *judged* has none of these, which is why it slips. A judged entry's bands are **described states of the design, ordered best to worst**, and the reader decides which description the design matches. Reinforcement-callout clarity is the type case — clean callouts, through a callout missing its laying order, to fully encoded notation — no measurement, no parts to pick. It is **not measured** (nothing sits on a continuum; the quality has no units) and **not chosen** (the bands describe the condition the design is *already in*, not interchangeable options you select between). What gets tested is the **ordering of the states and the call** (Step 5), never a cut-off.

---

## Step 2 — Grade every source on two axes

This is the heart of the rubric. A source has to clear **both** axes to evidence anything. Grading on one alone is what lets a strong-but-irrelevant source be smuggled into a slot it has not earned.

### Axis 1 — Source grade (how much weight the *type* of source can bear)

**Grade A — can fix a number.**
- Direct measurement or field data on the same element or parameter
- First-principles physical derivation from established component dimensions or mechanics
- Peer-reviewed research
- A **doctoral thesis** for which the doctorate has been **awarded** — whatever the institution, country or examination format. Doctoral examination is treated as equivalent to peer review. (A submitted but unawarded thesis is not Grade A.)
- A **book confirmed to have been formally peer-reviewed** — the publisher states a peer-review process, or it belongs to a recognised peer-reviewed monograph series. A book whose review status you cannot confirm is **Grade B**, not Grade A
- A **statutory duty** bearing on how the thing gets built — the provision of the **WHS Act or WHS Regulation** that says what must be done (cited by section), the Design and Building Practitioners Act — and, **in NSW from 1 July 2026**, the requirements and recommended controls of an **approved code of practice** (see *WHS law, codes and guidance* below)

> **What every Grade A source has in common — and why it can stand alone.** Each has already cleared *verifiable independent scrutiny* before it reached you: peer review, doctoral examination, a reproducible first-principles derivation anyone can rerun, or a duty that simply binds. That is the entire reason a single on-point Grade A source reaches `established` on its own (Step 4), where a Grade B source — authoritative, but never put through that gauntlet — still needs a second independent leg. When you promote a book to Grade A you are asserting that scrutiny happened *and can be pointed to*. If you cannot point to it, it is Grade B.

**Grade B — can back a call, and can fix a number where the number is a physical or regulatory fact.**
- **Practical guidance in an approved code of practice** where compliance with the code is not itself a statutory duty (outside NSW, or before 1 July 2026), and **regulator guides, safety alerts and other published guidance**
- Regulator research or a regulator's published findings (a VBA water-ingress report, a Building Commission defect study)
- Authoritative industry technical note or guidance (SRIA, CCAA, ACI, CIRIA, Engineering NZ) — a *technical note*, which is a different thing from a design code
- A **materials or product standard** recording a physical or manufacturing fact (AS/NZS 4671 on which bar sizes the rebend test covers) — again, not a design code
- Government or agency research synthesis (NCHRP, NBS)
- Established reference textbook, or a book whose formal peer-review status **cannot be confirmed** (a confirmed peer-reviewed book is Grade A)
- **Technical learning resources** published by a recognised public university, TAFE or equivalent body, where the **institution takes editorial responsibility** — published under the institution's name on its official site or in its official learner materials, not attributed to an individual lecturer — and the resource teaches established technical practice (the RMIT Learning Lab pages; an official TAFE NSW learner resource). Informal lecture notes, student material, commercial training content and privately published course material stay **Grade C**
- Primary research conducted for the framework (e.g. a structured supplier-availability review) — admissible, but it can never be the leg that lifts an entry (Step 3)

**Grade C — can corroborate a claim. It can never evidence one.**
- Documented real project case (a `concern` / `recommended` example that actually occurred)
- Manufacturer or supplier product data — **including a manufacturer's published limit**
- Trade or contractor guidance; industry consultation
- Unaided practitioner judgement

> **Grade C and `established`.** Only **one** kind of Grade C source can be the independent leg that corroborates a Grade B call: a **documented real project case that is independent of the framework, has traceable provenance, and addresses the same actionable claim**. Manufacturer data (published limits included), contractor guidance, consultation and practitioner judgement **cannot** be that leg. And **Grade C does not add up**: two manufacturer manuals agreeing on a 600 mm limit are still two pieces of Grade C — any number of them, however consistent, cannot establish a claim or stand in for an on-point A or B source.

> **Design codes are deliberately not part of the evidence base — do not add them.**
>
> AS 3600, AS 4100 and their companions are **the engineer's own ground**. They already apply them, they are bound by them, and restating them tells a reader nothing they do not know. More to the point: **the framework exists for the constructability question the standard does not answer.** A design code tells you the section works. It does not tell you whether anyone can form it, reach it, bend it on site, or stand next to it safely — and that is the entire subject of this framework.
>
> An entry whose case rests on a design standard is either restating the code (and should be deleted), or has mistaken a compliance question for a constructability one (and should be reframed).
>
> Two narrow uses are legitimate, and neither is evidence: **vocabulary** (AS 2870 is cited for the site-classification terms suppliers label their pods by), and **boundary-marking** (naming the standard that governs a matter precisely in order to say the entry is *not* trespassing on it, and that it stays the engineer's responsibility). Both are context. Neither grades.
>
> **This excludes design codes — not materials and product standards.** AS/NZS 4671 is a *materials* standard: it records that the rebend test applies to deformed bars of 16 mm and smaller, with no equivalent above. That is a **physical and manufacturing fact about the steel**, not an instruction to a designer, and it is admissible as Grade B — it can fix a number precisely because the number is a physical fact. The test is simple: *does the document tell the engineer how to design, or does it record how the material or product actually behaves?* The first is theirs. The second is evidence.
>
> **Nor does it exclude construction-basis clauses that happen to sit in a design manual or specification.** The exclusion bites only where a code is cited *because it governs the completed design*. A clause whose stated basis is **construction** is graded on its own terms: ACI 301's default of chamfering permanently exposed corners (a reference *construction* specification, not ACI 318), or a state authority's design-manual rule that rock removal be avoided and footings not keyed into rock without a design requirement. Ask what the clause is *for* — if it is there to control how the thing is built, it is construction guidance.
>
> **Where a duty is cited as Grade A, it is a WHS or regulatory obligation about the act of construction — not a design code.** That distinction is the whole point.

### WHS law, codes and guidance — three layers, graded by where you are

WHS sources come in three layers, and the middle one changes grade with the jurisdiction. **Grade the specific provision you rely on, by its legal force in NSW at the rating date, and cite it.**

| Layer | What it is | Grade |
|---|---|---|
| **WHS Act and WHS Regulation** | The law. Says what must happen; no opting out. *E.g. the designer's duty to design so far as reasonably practicable without risk to those who construct the structure (WHS Act s 22); the duty to eliminate the need to enter a confined space (WHS Regulation, confined spaces).* | **A** — cite the section |
| **Approved code of practice** | Explains how to meet the law. Approved by the Minister; a court may use it as evidence of what was reasonably practicable. **In NSW from 1 July 2026 (WHS Act s 26A)** a PCBU must comply with an applicable approved code or achieve an equivalent or higher standard — so its requirements and recommended controls are the enforceable minimum. | **A in NSW** (cite the code clause **and** s 26A); optional "may" content and explanatory text stay **B**. Where no such provision applies, **B** |
| **Regulator guides, safety alerts, published findings** | Guidance a step below codes. Authoritative, not binding. | **B** |

- **Where a code or guide restates a duty,** the Grade A source is the Act or Regulation provision it restates — cite that provision, not the code's paraphrase.
- **s 26A reaches designers.** It is a PCBU duty, and a design practice is a PCBU when it designs; the codes themselves say they guide PCBUs including those who design structures.
- **The grade follows the law.** A change in the law can move an entry's level with no new evidence — re-rate when it happens (see *When to re-rate*).

> **Grade the provision, not the document.** A code of practice carries several kinds of content at once. The **duty** it restates — *designers must eliminate the need to enter a confined space so far as is reasonably practicable* — is Grade A through the Regulation it restates. Its **recommended controls** are Grade A in NSW under s 26A, Grade B elsewhere. Its **optional and explanatory content** is Grade B everywhere. Cite which one you are leaning on, because they do not carry the same weight. The same discipline applies to a textbook, a technical note, or a journal paper: you grade the claim you are actually using, not the cover of the thing it came in.

### Axis 2 — Proximity (what the source is actually *about*)

- **On point** — it addresses the proposition the reader acts on.
- **Adjacent** — it addresses a *neighbouring* proposition. A source about a chamfer on a precast cladding joint is adjacent to a claim about a formed in-situ arris. A drafting manual that sets the standard chamfer size corroborates a **drawing convention**, not a **damage claim**.
- **Transferred** — the right phenomenon, but studied in a different field and carried across by inference. Visual-clutter research on general displays, applied to reinforcement callouts. Pipefitting drawing studies, applied to RC structural sets.

**There is no fourth value.** No "near-on-point", no "Grade B-ish". A source is on point, adjacent or transferred, and you must pick one.

**Different element, same mechanism.** Evidence from a different element or application is **on point only where the source states, measures or otherwise demonstrates the same mechanism** relevant to the actionable proposition — and then the difference is a **scope note**, not a lower proximity. A recommendation or convention stated **without** that mechanism in another setting stays **adjacent**.
- *On point, scope note:* BRANZ's thickened-edge and beam-box forming figures applied to a slab fold — the vertical face is formed the same way. Jarkas's perimeter edge-formwork productivity applied to an internal fold.
- *Adjacent:* CCAA TN63's "12 mm chamfer to minimise damage" on a precast cladding joint, applied to an in-situ arris — it states no mechanism, so there is nothing to show the mechanism carries.
- **Scale and sector are treated the same way.** Bridge or highway guidance applied to building work (CIRIA's *Bridge Detailing Guide*, state DOT manuals, NCHRP) is on point with a scope note where the same mechanism applies — not a lower proximity.

### The rule that does all the work

> **A claim is *evidenced* only by a Grade A or Grade B source that is *on point*.**
>
> **Adjacent** or **transferred** caps the entry — however good the source is. A peer-reviewed paper about the wrong thing is still about the wrong thing.
>
> **Grade C never evidences a claim.** It corroborates one that Grade A or B has already established — and only an independent, documented real case can do even that.

---

## Step 3 — Test independence, and test it on the same claim

**A Grade B call needs a second, independent leg to reach `established`. A single on-point Grade A call does not** — it stands on the scrutiny it already carries (Step 4). What follows therefore governs **Grade B corroboration**, and the lifting of any `directional` entry to `established`. Two rules govern what counts as a second leg.

**Independence.** Two sources are independent only if they **could have disagreed** — different authors, different evidence base, different organisation. **Test it on derivation, not wording:** different phrasing and different figures do not prove two sources are independent; the question is whether one takes the proposition from the other, or both take it from the same place.

The following are **one source, not two**:
- Two publications from the same body (SRIA Technical Note 4 and SRIA Issue 42/4; an agency's geotechnical manual and its bridge manual)
- Parts I and II of the same review, by the same authors
- Two jurisdictions adopting the same model law (a SafeWork NSW and a SafeWork SA code implementing the model WHS Regulations)
- A thesis and the journal paper drawn from it
- A source and another source that merely cites it
- **Two sources that both restate the same upstream source** — the same standard, model code or manual (a regulator's guide and the state code built from it; two training resources both paraphrasing the same industry guide or AS 2870; a state DOT rule taken from another state's manual). Count the lineage once.
- **A supplier, tool or market review — or a consultation — the framework ran itself, offered as its own second leg.** It shares the framework's author and motive and *could not have disagreed* with the entry it supports, so it is not independent of it. It may also be non-exhaustive: a scan that stops at four listings can miss the fifth that breaks the claim.

**A self-conducted review cannot be the leg that lifts an entry to `established`.** Evidence the framework gathered itself — a supplier/tool/market review, a price scan, an author-run contractor consultation — can *inform* an entry and be cited, but it is not independent of it, so it can never be the corroboration that raises a Grade B call from `directional` to `established`. The elevating leg must be **externally verifiable and independent of the framework**: a published standard, a second body's guidance, peer-reviewed work, or a genuinely independent documented project case (not the framework's own recommended detail shown in use). **Manufacturer or supplier data — a published limit included — is Grade C and cannot be the elevating leg.** A self-conducted review with no such second leg leaves the entry `directional`.

**The corroborating source must be on point — on the same claim.** A second leg that supports a *neighbouring* proposition is not corroboration; it is a second entry's evidence, wearing this one's badge. If the claim is *"a chamfer prevents arris damage,"* a manual specifying that standard chamfers are 20 × 20 does not corroborate it. It corroborates that the convention exists.

> This is the rule most often broken, and it is broken in good faith — by a reviewer stacking up sources that all feel relevant. Before you count a leg, say out loud: *the claim is ___, and this source says ___.* If those are different sentences, it is not corroboration.

**Corroborate the call, not every reason.** The second leg must support the **actionable call** — the proposition the bands sort by — not every strand of the explanation behind it. The mechanism can rest on one source while the call is corroborated by another:
- ACI 301's chamfer-by-default rule corroborates the **call** (*chamfer permanently exposed external corners unless deliberately excepted*); CIRIA carries the call **and** the damage mechanism. Two legs on the call → enough.
- A documented project case corroborates PN28's **construction-process** claim (plant spread, spoil) — it is not evidence that screw piles suit buildings.

So write the rated proposition as one sentence first, then test each leg against *that sentence*. And where a corroborating source comes from a different setting, add a **boundary sentence** in the evidence text saying what it is **not** being used to show — it stops a reader (or a reviewer) reading more into the leg than it carries.

---

## Step 4 — Assign the level

Work down. The level is set by the **weakest** link, not the strongest source.

**Two gates decide the level, in order — and the second one is about your guidance bands.**

**Gate 1 — proximity: is the effect on point?** Is there an on-point Grade A or B source for the effect the entry turns on — the thing the bands sort the design by? *On point* means it addresses the proposition the reader acts on, not a neighbour or an analogy (Step 2, Axis 2). Only adjacent or transferred support → `indicative`, however strong the source; **no on-point, adjacent or transferred support at all → `reasoned`**. If the effect **is** on point, the entry can reach `established` or `directional` — go to Gate 2.

**Gate 2 — coverage: are the guidance bands themselves evidenced?** Proximity buys a supported *effect*. Coverage asks whether the **bands the reader actually applies** — the boundaries between Best practice / Consider / Concern / Action required — are each backed by that on-point evidence. Band by band: a *measured* entry's numeric cut-offs; a *chosen* entry's recommended option and its ordering; a *judged* entry's ordering of the described states; a *counted* entry's conditions and the count at which the band changes. **Every** boundary evidenced on point (and independently corroborated where the on-point leg is Grade B) → `established`. The effect evidenced on point but **one or more boundaries is the framework's own reasoning** → `directional`.

So a missing band boundary can only drop you from `established` to `directional` — it is a Gate 2 (coverage) matter. It can never take you to `indicative`, which is a Gate 1 (proximity) failure. The two gates fail in different places; judge them in order.

> **Walking both gates — off-form upturn clearance (entry 1, as currently written).** *Gate 1:* the effect is "you need room behind the form to build it", and the formwork mechanics address exactly that — on point, Grade A/B. Gate 1 passes, so the entry is at least `directional` and `indicative` is off the table. *Gate 2:* the bands are ≥ 1000 / 700 / 350 mm. The formwork-component half of each boundary is first-principles (Grade A) — but the human working-clearance built into every boundary is practitioner judgement (Grade C), and the entry cites nothing on point for it. The bands the reader applies are therefore **not fully evidenced** → one leg reasoned → **`directional`**, capped by coverage, not proximity.
>
> *What lifts it:* on-point evidence for the working clearance **exists** — Safe Work Australia's *Guide to Formwork* (≥ 450 mm two-plank platform) and Pallett & Filip's 600 mm typical platform. Citing them and re-banding (≥ ~830 / ~680–830 / < ~680 mm) covers every boundary with two independent legs → `established`. Until that edit is made, the entry is rated as it stands.

### `established` — *evidenced on point; the scrutiny is independent*
Everything the reader acts on rests on **on-point** evidence, and reaches this level in **either** of two ways:

- **a single on-point Grade A source** — peer-reviewed research, an awarded doctoral thesis, a confirmed peer-reviewed book, a reproducible first-principles derivation, or a binding statutory duty (including, in NSW, an approved code's requirements). Grade A carries its independent scrutiny in itself, so it **stands alone**; or
- **an on-point Grade B source, independently corroborated on the same claim** — by another on-point A or B source, or by an **independent, on-point Grade C documented real case with traceable provenance**.

For a *measured* entry that means **every cut-off**; for *chosen* or *judged*, the call **and its ordering**; for *counted*, **every condition and the breakpoint**. (Coverage is tested in full at Step 5 either way — that is where a single scenario dressed up as a general cut-off fails, on coverage, not here on corroboration.)

This is the strongest evidence the framework carries. The residual uncertainty is about the precision of a single value, or how often the situation arises — not about whether the guidance sits in the right place.

It is **not** an instruction to adopt the numbers unexamined. An engineer's own checks, and their responsibility for the design, are undiminished at this level. What `established` says is narrow and factual: *the guidance sits on evidence that has itself been independently scrutinised.*

### `directional` — *the direction is proven; the number is ours*
**The mechanism and direction are evidenced on point by Grade A or B — but a link is missing.** One or both of:

- **Coverage.** The specific values the reader acts on are *reasoned*: a measured entry's cut-offs, a counted entry's breakpoint, or the gradation between a chosen/judged entry's states. The direction is proven; the number is the framework's.
- **Corroboration (Grade B only).** The call is fully and directly evidenced by a single on-point **Grade B** source, but nothing independent confirms it — a single authority, or a single documented case. **A single on-point Grade A source does not land here** — it reaches `established` on its own (see Step 4). Adding one independent leg lifts a Grade B `directional` to `established`.

**What is evidenced here is the direction. The specific value is the framework's reasoned call** — and that is precisely the part an engineer should expect to weigh against their own job, because it is the part we cannot show them a source for.

> **This is the framework's home.** Most good constructability entries live here, and that is not a failing. A measured mechanism with a reasoned cut-off is an honest, useful, well-founded entry — and it is materially different from an entry that is mostly reasoning. Before this level existed, the two were both called "medium," and readers could not tell them apart.
>
> **The name is doing a job.** It tells a reader exactly how far to lean: *believe the direction, sanity-check the number.* Do not let a later reviewer rename it back to something that sounds like a grade — it is not a grade, it is an instruction.
>
> **`directional` can be the right end state.** Some entries are *missing-evidence* `directional` — the second leg exists, go and find it. Others are *judgement-terminal* — the remaining gap **is** the professional judgement the entry exists to provide, and forcing `established` would mean falsifying a derivation or stripping the rule the reader needs. Say which kind it is. Never narrow or reword an entry into something less useful just to reach a higher level; reframe only where it corrects an error or improves the guidance.

### `indicative` — *plausible, but the evidence is about something else*
**The evidence base is not on point.** The claim rests on **adjacent** or **transferred** sources — however strong their grade — or the only on-point support is Grade C.

The direction here is *plausible* rather than proven — that is the line between this level and `directional`. The reasoning is sound, but nothing directly evidences the proposition the reader acts on, so the entry is carried by inference.

### `reasoned` — *practitioner judgement, published so the gap is visible*
The call rests on practice-based judgement, and **no on-point, adjacent or transferred evidence** has been identified for it. The call is essentially asserted.

> **Where the line with `indicative` falls.** Evidence borrowed from a neighbouring proposition (adjacent) or another field (transferred) — however loose — makes the entry `indicative`, not `reasoned`. So does on-point support that is **only** Grade C. `reasoned` is reserved for the case where there is genuinely nothing to point to beyond the framework's own judgement.

> **A `reasoned` entry can still be published live, and should be.** Publishing it is what makes the gap visible and invites the measurement, source or field experience that would raise it. `reasoned` is an open invitation to supply evidence, not a failing grade and not a bar to release. A maintainer may publish at `reasoned`, or research further and publish higher.
>
> **`reasoned` does not mean nobody tried.** Distinguish the two cases in the summary, because they call for different action: *the research exists and this entry has not cited it* (go and cite it), versus *the study does not exist* (a real hole in the literature — say so plainly, and the entry becomes the record of that hole).

---

## Step 5 — Apply the matching test

**Measured — the per-cut-off test.** For **each** band boundary: is there an on-point Grade A or B source behind *this specific number* — a measurement, a physical derivation, a regulatory fact, or physical product information? Every cut-off must clear it. One reasoned round number caps the entry at `directional`.
- **A band must not over-claim against its own source.** If a cited source shows that part of an "Action required" range is acceptable (e.g. a regulator's minimum is met inside it), the boundary is wrong, not just unevidenced. The fix is a confirm band between the two evidenced lines — not a binary split that contradicts the source.

**Chosen and judged — the recommended-call test.** There are no cut-offs to defend, so ask instead: is the recommended choice — **and the ordering of the options or states** — backed by an on-point Grade A or B source? Do **not** cap a chosen or judged entry because it has no measured numbers. It has none to have. This holds for a menu of millimetres exactly as it holds for a menu of words.
- **Middle "compare / confirm" states need no evidence of their own.** A state that only tells the designer to compare the evidenced end states, or confirm which applies, makes no claim to evidence. A middle state that makes **its own** claim — a ranking of methods, say — must be evidenced like any other.
- **Two right answers are not a ranking.** If the entry ranks two states that the evidence treats as equally acceptable outcomes (a socket with an identified function; no socket where rock bearing suffices), that ranking is unevidenced and caps the entry at `directional`. The fix is authorial — put both states in one band (see the padding test in section 9 of the entry quality rubric).

**Counted — the conditions test.** Both halves need evidence:
1. **The condition list.** Is each named condition itself supported on point, and genuinely a precondition? This is the substance, and where the evidence usually is.
2. **The breakpoint.** Why does the rating change at *that* count — why is `2 or more` the concern and not `3`? This is almost always reasoned; nothing in the literature says two failed preconditions is where a waffle pod stops being right.

> **A counted entry caps at `directional` unless the breakpoint itself is sourced.** A fully-evidenced condition list with a judged breakpoint is a strong `directional`, not an `established`. Say so: *"each precondition is supported by X; where the count becomes material is a reasoned call."* And check whether the count is real at all — if the entry's own bands show that the *type* of condition does the work rather than the number, the entry is really *judged*, and that is a reframing question for the quality rubric.

---

## Traps to avoid

* **Mechanism inflation.** A measured, peer-reviewed *effect* does not lift the *cut-offs* if the boundaries are judgement. That is `directional`, and the whole point of the level.
* **Grade laundering.** A Grade A source that is *adjacent* does not become on-point by being peer-reviewed. Proximity is not negotiable by quality.
* **Proximity fudging.** "Near-on-point" is not a category. If you cannot show the source carries the same mechanism, it is adjacent — say so.
* **Leg-stacking.** Counting a source that supports a neighbouring proposition as the corroborating leg. State the claim and the source's finding as two sentences and compare them.
* **Leg-stretching.** Using a legitimate corroborating source to prove more than it says — a bridge-project case used as proof about building foundations. Write the boundary sentence.
* **False independence.** Two documents from one organisation, two parts of one review, two jurisdictions under one model law, a thesis and its paper, two sources restating the same upstream standard. One source, published twice.
* **Grade C arithmetic.** Two manufacturer limits, three contractor opinions, four supplier pages. Still Grade C; still cannot establish anything.
* **Miscitation in our favour.** Check that the source actually says what the entry claims — not just that the citation is real. A correctly cited paper pointed at the wrong claim (an economy-of-scale finding cited as a depth-labour penalty) is the most dangerous error, because it looks like evidence.
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

Two content rules:
* **Say what the sources actually say.** Don't upgrade a "should" to a "requires", or a code's scope statement to a duty that "binds" — the summary is the first place an overclaim is visible.
* **Name the jurisdiction where the level depends on it.** If an entry is `established` because an approved code is Grade A in NSW, say so — the same entry may read lower elsewhere.

Two mechanical rules:
* **Never announce the level in the summary.** It renders in a chip beside the text. *"A strong directional. Backed by…"* is redundant and goes stale the moment the level changes.
* **A summary that names no limitation at all** is a red flag on anything below `established`.

> **A note on vocabulary, and why `directional` is called that.** The level names are ordinary words the summaries themselves need — a summary will legitimately say a claim is *supported by* a standard, that a mechanism is *well established*, or that a cut-off is *reasoned*. That is fine. What is banned is using the word **as a verdict on the entry**. The one name deliberately kept out of that pool is **`directional`**, because "supported" is the single most common verb in an evidence summary, and a chip reading `SUPPORTED` beside a sentence beginning *"Strongly supported by four studies…"* leaves a reader unable to tell whether the prose is stating the rating or describing the sources. Where a summary needs to say a claim is well backed, prefer **backed by, rests on, evidenced by, confirmed by, fixed by**.

---

## When to re-rate

Set `dateReviewed` whenever you assign or change a level. Re-rate when:

* new evidence moves a value from reasoned to evidenced, or supplies a missing corroboration leg — or vice versa;
* **a source's grade is reassessed** — recognising an awarded doctoral thesis or a confirmed peer-reviewed book as Grade A, or an institutionally published learning resource as Grade B, can move an entry with **no new source**;
* **the law changes** — a new statutory provision (such as NSW WHS Act s 26A from 1 July 2026) can change the grade of a code of practice, and with it an entry's level, with no new evidence;
* **a citation turns out to be wrong** — a misattributed author, or a source that does not say what the entry claims; fix the citation first, then re-rate on what the source actually supports;
* the parameter or band boundaries change;
* **the entry's *kind* changes** — a reframing from *measured* to *chosen*, or a *counted* parameter named for the first time, changes which test applies and can change the level with no new source at all;
* an accepted edit suggestion alters the guidance or the supporting evidence.

A change in level always comes with an updated `summary`, so the two never contradict.

---

## Worked examples

**Measured → `directional` (coverage fails).** Suspended slab folds (entry 16, as live). A BRANZ technical publication (Grade B) shows standard slab-edge and beam-box forming capped at 600 mm, and the vertical face of a fold is formed the same way — on point, with a scope note. Manufacturer manuals show the forming arrangement stepping up around the same depth, but they are Grade C and cannot corroborate, and nothing on point supports the entry's response *above* 600 mm (prefer blockwork or separate pours) — that is the framework's reasoning, as is the 1000 mm boundary. → `directional`: trust that forming gets heavier around 600 mm; the recommended response is ours. *(The live entry also cites Jarkas for "labour rising with face depth" — a misread; Jarkas shows economy of scale. Fix the citation, then re-rate.)*

**Chosen → `directional` (corroboration fails, Grade B).** A bar-size hinge is directly and authoritatively backed by an industry technical note — on point, **Grade B**, full coverage of the call. But every citation is from the same body, and there is no project case. One source, published twice. → `directional`, missing the second leg. *One independent source, or one independent documented case, would make it `established`.* The grade is doing the work here: had that single on-point source been **Grade A**, the entry would be `established` on its own.

**Chosen → `established` (single Grade A leg).** A recommended call and its ordering are directly and on-point evidenced by a single peer-reviewed study (**Grade A**), covering the call in full. No second independent source exists. → `established`. Grade A carries its own independent scrutiny, so a second leg is not required — corroboration would still be welcome (it is what lifts the Grade B case above), but its absence does not cap a Grade A call.

**Judged → `established` (both legs, on the call).** Chamfered exposed external corners. CIRIA's *Bridge Detailing Guide* (Grade B, on point) says sharp formed corners can't be cast cleanly and should generally be chamfered — the call and the mechanism. ACI 301-20 §2.3.1.2 (Grade B, on point, independent) makes chamfering the construction default on permanently exposed corners, with exceptions stated by the specifier — the same call. Two independent legs on the call → `established`. The RTA manual and a stamped drawing set support only the *documentation* convention, and CCAA TN63 is adjacent; none of them is a leg.

**Chosen → `directional` (self-conducted review cannot lift it).** A framework-run supplier review (Grade B, on point) shows which pod depths are stocked, and the framework's own project drawings show those depths in use. The review cannot be the elevating leg, and the drawings are the framework's own detail in use (and show use, not stock status). → `directional` until an independent source — an industry supply survey, a supplier association's stock list — confirms the same claim.

**Counted → `directional` (breakpoint unsourced).** Each of three waffle-pod preconditions traces to on-point guidance and a documented case. But nothing says the system should be reconsidered at *two* failures rather than three. Strong list, judged breakpoint. → `directional`.

**Judged → `indicative` (proximity fails).** Peer-reviewed visual-clutter research shows targets get harder to find as a display grows cluttered, and a real project records extras being missed in a compressed callout. But the research is about **general displays**, not engineering drawings — no study tests how reinforcement callouts are read by steel fixers. Grade A, but **transferred**; the project record is on point but Grade C. → `indicative`. The grade does not rescue the proximity.

**Judged → `reasoned` (nothing to point to).** The recommended ordering rests on practitioner judgement, and the two drawing examples illustrate the principle rather than documenting a failure that occurred. No study or authoritative source addresses the proposition — on point, from a neighbouring proposition, or from another field. → `reasoned`, and the summary should say the on-point study does not exist rather than implying it was not looked for. *(If there **had** been research borrowed by analogy — from a sibling entry or another field — that would be transferred support, and the entry would be `indicative`, not `reasoned`.)*
