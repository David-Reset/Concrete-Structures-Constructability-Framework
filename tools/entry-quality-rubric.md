# Entry quality rubric

How to judge whether an entry is **well-framed** — consistently, regardless of who is reviewing.

This rubric is about the **shape** of an entry, not its content. It asks: does it have the parts it must have, is it under the right dimension, is the question one clear thing, is the parameter one thing you can act on, do the question and parameter answer the same thing, do the bands follow cleanly, and is everything as short as it can be? It does **not** judge whether the guidance is correct or well-supported (that is the [evidence rating rubric](evidence-rating-rubric.md)) or when the entry should surface on a job (that is the [triage rating rubric](triage-rating-rubric.md)).

---

## The core principle

> An entry asks **one concrete design question**, answered by **one design parameter you can act on**, split into **a few clearly-labelled threshold bands**. The question and parameter stay short; the depth goes into **Background** and **Evidence basis**.

Almost every framing problem is a version of putting the wrong thing in the wrong field — usually cramming detail into the question or the parameter that belongs in the bands, the background, or the evidence. Keep the top of the entry tight and let the lower fields carry the reasoning.

**Reframing moves text between fields. It does not re-author the guidance.** Don't move a threshold from 200 mm to 250 mm, don't change what a band means, don't invent evidence. Whether a number is *right* is the evidence rubric's job; this rubric only asks whether the entry is *shaped* so a reader can act on it. If a fix would change what the entry actually claims, that is a signal to send it back to the submitter — not to quietly rewrite it.

---

## What every entry must have

An entry is not complete — and the Data Manager will flag it as a draft that can't be published — unless it has all of these:

- **A dimension** to sit under (one of the five: Construction Methods, Detailing, Logistics, Safety in Design, Design Communication) — and it must be the **right** one (see section 1).
- **A name** — the entry title. Its stable **id** is generated from this. (Never change a live entry's id.)
- **A design question** — the one question it answers.
- **A design parameter** — the one thing the reader checks.
- **Threshold bands** — the design guidance, at least the bands themselves.
- **Applicability — where it applies** — the conditions under which the entry is relevant.

Everything else is **optional** and strengthens the entry rather than being required: Background, Evidence basis, Evidence support (Low / Medium / High), Location (the region the evidence came from), Recommended actions, supporting or example images, search keywords, element and lifecycle-stage tags, and related-entry links.

---

## 1. The dimension — the one that actually covers it

- Each dimension has a **description** stating what it covers. The entry belongs under the dimension whose description **actually covers the decision the entry is about** — not the one the submitter reached for first.
- Judge by the **question**, not the subject matter. An entry about reinforcement can sit under Detailing (how the bars are specified), Construction Methods (whether the cage can be built), Logistics (whether the bars can be sourced or bent on site), Safety in Design (whether someone has to cut them with a grinder) or Design Communication (whether the callouts can be read) — the dimension follows **what is being decided**, not what the element is.
- **The same design choice may legitimately appear under more than one dimension**, provided each entry asks a genuinely different question with its own parameter and its own consequence. That is by design, not duplication. It *is* duplication if two entries ask the same question and only the wording differs.

## 2. The design question — one concrete question, briefly

- **One question, not several.** If it joins two separate decisions with "and" or "or", it's usually two questions — split it, or cut the second half. Often the second half ("…and at what point should alternatives be considered?") is really the bands talking, and doesn't belong in the question at all.
  - **Not every "or" is a stacked question.** A question that offers two options of a *single* decision — "…should the soffit be folded to follow it, or should the top be stepped down to keep the soffit flat?" — is one question. The test is whether answering it requires **one** judgement or two.
- **Don't state the answer inside the question.** "Has slab reinforcement been detailed with 12 mm or 16 mm bars where structurally practical…?" can't be answered by someone who doesn't already know the guidance. Ask what is being checked; let the bands say what good looks like.
- **Concrete and answerable** from the drawings or the site, phrased as the actual question the entry answers.
- **Short — aim for a single sentence.** If it's running long, the extra context belongs in Background, not the question.

*Good:* "Can the pier or shaft base detail be completed from the surface, without a worker entering the excavation?" — one thing, one sentence.

## 3. Naming the default — cut it from the question, don't lose it

Many of the strongest entries are about an **omission**: the designer didn't weigh something, and doesn't know they didn't. Those entries are tempted into a long question with a rhetorical tail — *"…or has the structure defaulted to a single continuous pour because a break was never offered?"*

That tail is doing real work. It names the default so a designer recognises themselves in it. But it does **not** belong in the question field, where it makes the entry unscannable.

- **Cut it from the question. Move it to the first line of Background.** Relocate, don't delete.
- An entry that loses its named failure mode altogether is weaker, not tidier. A reviewer who deletes it has over-applied this rubric.

## 4. The design parameter — one thing you can act on, short

- Names the **single thing** the reader measures, counts, selects, or assesses from their drawings, the site, or a supplier.
- A **short noun phrase**, with units if it's a number. Not a sentence, not a list of options, not an instruction.
  - A trailing full stop is a reliable tell that the parameter has drifted into a sentence.
- It must be the thing the **bands are values or states of** (section 6).
- It does **not** have to be a number — see section 5.
- **One variable, not two joined by "and."** "The bushfire attack level, *and* whether any element in the attack path is combustible" is two parameters, and it forces the bands to become combinations. Usually one of the two is really a **driver** or a **condition of applicability**, not the parameter: name the thing the bands are states of, and move the other down.

*Good:* "Top setdown depth (mm)" · "Specified stirrup, ligature or tie bar size" · "Clarity of reinforcement bar callouts".
*Bad:* a parameter that describes the bands — e.g. a paragraph naming every class of drilling plant, or a sentence that runs "resolved in the design, drawn without coordination, or left to construction" (that is just the three bands restated). If your parameter is a paragraph, the bands have leaked into the wrong field: shorten the parameter to the thing being assessed and let the bands carry the detail.

## 5. Question and parameter must answer the same thing

**Read the question, then read the parameter. They must be about the same thing.** This check is easy to skip because an entry can pass every other section and still fail here.

The common failure is a question about a **process** paired with a parameter about a **magnitude**:

> *Question:* "Has the formwork-cycling advantage of post-tensioning been weighed in the slab system choice?"
> *Parameter:* "Number of repeated suspended floors."

A reader checks the parameter, lands in a band, and learns how *significant* the issue is — which is not what the question asked. It asked whether someone *weighed* it.

- When they diverge, **the parameter is usually the honest one** and the question needs rewriting to match it, not the other way round. The bands were built on the parameter; they are the evidence of what the entry really checks.
- A question the parameter can't answer is a question the entry can't answer.

## 6. What kind of condition is it?

The logic is always the same — **condition → band → response** — but the condition an entry checks can come from different places, and it is **not always a number**. Recognise which kind an entry is, and make sure the parameter and bands are framed for that kind rather than forced into fake numbers.

- **Measured** — you read a number off the documentation and find the **range** it falls in. The value could land anywhere on a continuum.
  *Parameter:* a quantity with units. *Bands:* numeric ranges.
  *Example:* "Top setdown depth (mm)" → `≤ 50 mm` (Best practice) · `> 50 – 100 mm` (Concern) · `> 100 mm` (Action required).
- **Chosen** — you compare a specified **choice** rather than a number.
  *Parameter:* the choice being made. *Bands:* the options, best to worst.
  *Example:* "Specified stirrup, ligature or tie bar size" → `R10 or N12` (Best practice) · `N16` (Consider) · `R6` (Concern).

  > **A parameter with units is not automatically *measured*.** If, in practice, the value comes off a **standard menu** — bar spacing (150 / 200 / 250 / 300), bar diameter (N12 / N16 / N20), pod depth (225 / 300 / 375) — then it is **chosen**, not measured, even though it is a number in millimetres. Nobody specifies 260 mm spacing.
  >
  > This matters, because the coverage rule in section 9 applies to *measured* bands only. Forcing a menu into invented ranges to close a "gap" that no real drawing will ever land in is worse framing, not better. Ask what a designer actually writes on the drawing, not what a ruler could theoretically read.
- **Judged** — there is no number at all; you assess something against described states, clearest to least clear.
  *Parameter:* what's being assessed. *Bands:* described states, best to worst.
  *Example:* "Clarity of reinforcement bar callouts…" → `Clean callouts` (Best practice) · `No laying order` (Consider) · `Count included` (Concern) · `Encoded notation` (Action required).
- **Counted** — several named preconditions or constraints either apply or they don't, and what matters is **how many**.
  *Parameter:* the count itself — "How many of the three preconditions fail". *Bands:* `0` · `1` · `2 or more`, best to worst.
  *Example:* "How many of the three waffle-pod preconditions fail on this site" → `0 fail` (Best practice) · `1 fail` (Consider) · `2 or more fail` (Concern).

  A counted parameter is **not** a composite parameter smuggled in — it is a legitimate single thing to read off the drawings, and it is often the honest framing for a system-selection entry where no single number decides it. Three conditions apply, and the first is non-negotiable:

  - **The conditions must be listed.** If the parameter says "how many of the four", then **Background must name the four**, plainly, each with its own heading or line, so a reader can count against them. An entry that asks you to count things it never names is unusable — you cannot answer its own parameter. Band guidance does not count as "listed": nobody reverse-engineers a checklist out of the Best-practice band.
  - **The count must appear consistently.** If Background names four and the question says "access, spoil or open-hole", the entry contradicts itself and a reader working from the question will under-count. Either the question drops the list, or it carries all of it.
  - **The count must be doing real work.** If one condition always decides it, that condition is the parameter and the count is a fiction.

  *The pattern to copy:* state the count in one sentence — "the entry counts how many of the waffle pod's three preconditions fail on this site" — then give each condition its own bolded heading and paragraph. A reader can then hold the list in their head and count.

The same shapes cover conditions **confirmed** from site conditions or **checked** with suppliers — they still resolve to a measured number, a chosen option, a judged state, or a count. Whichever kind it is, keep the parameter short and the band headings scannable.

## 7. Parameter and bands must agree

- Every band is a **value, range, state, or count** of the parameter — nothing else.
- Each band's guidance talks about **that** value of the parameter, not some other variable.
- If a band's guidance introduces a new measure the parameter never mentions, either the parameter is wrong, or that content belongs in Background.

Read the parameter, then read the band labels. They should obviously be the same thing.

## 8. Band headings — short and scannable (2–5 words)

- The heading is a **clean numeric range with units**, or a **2–5-word** categorical label.
- *Good:* "≥ 1000 mm" · "700 – 1000 mm" · "Socket into rock" · "R10 or N12" · "Clean callouts" · "2 or more fail".
- *Too long:* "Standard-auger limit / rock-auger attachment" · "Screw piles as a last resort, risk owned". Tighten the heading; the full detail goes in the band's **guidance text**, not its heading.
- No leading or trailing whitespace, and no stray punctuation.

## 9. As many bands as the reality has — no more

- Use the number of **natural breakpoints** the condition actually has. Two bands is perfectly fine; three and four are common. **Don't pad to four** for symmetry, and don't split one real threshold into two.
- Bands run **best → worst**, and each rating matches the severity of its guidance.

### The padding test — run it on every entry with four bands

"Don't pad" is useless without a way to *detect* padding, and padding is easy to miss: a fourth band always *reads* like it is saying something, because it is written in the worst-case voice. Run both tests:

1. **Are the two worst bands the same value of the parameter, split by a consequence?** Read them side by side and ask what actually separates them. If the answer is a variable the **parameter never names** — how tight the governing check is, how critical the space is, whether the other trades are already on site, whether the variation was avoidable — then they are **one band**, not two, and the split is a severity escalation on a second axis. This also fails section 7.
   > **The tell:** the last band opens with *"As above, and…"*, *"As above, but…"*, or restates the previous band and adds a worse consequence. If a band begins by referring to the one before it, it is not a distinct value of the parameter.
2. **Only if test 1 says yes:** if you deleted the last band, would any reader be told to do something different? If the response is the same action with more urgency attached, the urgency belongs *inside* the band above, not in a band of its own.

> **Test 2 never fires on its own.** Run it *only* on bands that already failed test 1. Many sound entries are **gradients** — the same action escalating with the parameter. "Justify the rock socket or remove it" is the right response at `> 150 – 300 mm` *and* at `> 300 mm`; what changes is how much drilling cost an unjustified socket is committing, and that is a real difference in the parameter. Applying test 2 alone would wrongly merge every gradient entry in the set. **A different value of the parameter always earns its own band, even when the action is the same.**

**Before you merge, check the parameter is named right.** A band pair that *looks* padded is often a symptom of a **mis-named parameter**, not a padded band. If two bands seem to be the same value, ask what the *first* band is a value of — if the parameter cannot describe the best band either, the parameter is the problem and the bands are fine. Rename the parameter to the scale the bands actually run along, and the padding disappears. Merge only once you are sure the parameter is right.

A band earns its place by being a **different state of the parameter**, not a worse outcome of the same state. Where two bands merge, **nothing is deleted**: the escalation content moves into the surviving band's guidance as a check to run ("check the margin in the governing check…", "the consequence scales with the space…").

### The missing-band test — the other half of the pair

Padding asks whether a band exists that shouldn't. This asks the opposite, and it is the easier one to miss, because a missing band leaves nothing behind to notice.

> **Walk the parameter's values from best to worst. At each step, ask whether the reader is told to do something different from the step before. Where the instruction stops changing, the bands stop. Where the instruction *would* change and no band marks it, a band is missing.**

The tell is a **parameter that reaches further than its bands do**. If the parameter says *"how many of the four constraints apply"* and the worst band is `2 or more`, then values 3 and 4 exist in the parameter but not in the bands. That is not automatically wrong — it is a **question to answer**:

- If a site with all four constraints gets **the same advice** as a site with two, then two is the last real breakpoint, `2 or more` is correct, and adding a band would be padding. **Leave it.**
- If it gets **different advice**, a band is missing and the entry's worst case is currently invisible.

Run this on any entry where the parameter can take values the bands do not name — a count that stops short of its own maximum, a menu with an option missing, a numeric scale whose worst band is closed at the top when the value could go higher.

**The two tests are a pair.** Padding without the missing-band test collapses entries toward too few bands; the missing-band test without padding inflates them. Run both, in that order, and only on the strength of what the parameter can actually take.

*What a genuine four looks like:* "Required plywood soffit-sheet width" → `≤ 1200 mm` · `> 1200 – 1800 mm` · `> 1800 – 2400 mm` · `> 2400 mm`. Four bands because plywood comes in those sizes. The reality has four breakpoints, so the entry has four bands.

### What the ratings actually grade

The four ratings grade **how much action the design decision demands**, not how good or bad the project is. This trips up reviewers, so it is worth stating plainly.

A band may legitimately describe a **fact about the project or the site** rather than a fault in the design — `0 preconditions fail`, `1 floor`, `no rating required`. **Best practice** there does not mean "well designed"; it means **nothing to do here — proceed**. **Action required** does not mean "the building is wrong"; it means **the designer must actively deal with this before the scheme locks**.

So do not "fix" an entry because a six-storey building comes out as *Action required*, or because a single-storey one comes out as *Best practice*. Ask instead: *at this band, how much is being asked of the designer?* If the answer escalates cleanly from "nothing" to "resolve this now", the ratings are right.
- The four ratings and their fixed colours are: **Best practice** (green), **Consider** (yellow), **Concern** (orange), **Action required** (red). These are the **only** four permitted strings, spelled and cased exactly as above — a variant like "Action Required" will not key correctly.
- A band set may skip a rating. Best practice → Consider → Action required is fine if that is what the reality has.

**Coverage — measured bands only:**

- Measured bands must cover the range **without gaps or overlaps**, because the value can land anywhere.
- **Endpoints must belong to exactly one band.** `≤ 600 mm` followed by `600 – 1000 mm` puts 600 in *both* — Best practice *and* Concern. This is not a pedantic edge case: 600 is a round number, and round numbers are exactly what designers write. The boundary value is the **most likely value on the drawing**, not the least.
  **House convention:** where a band claims a bound, the next band opens past it — `≤ 600 mm` · `> 600 – 1000 mm` · `> 1000 mm`. The `≤` already claimed 600, so this changes no guidance; it only says out loud what the band already meant.
- **The open ends must be closed.** The best band should run down to zero and the worst band up to infinity (`≤ 50 mm` … `> 100 mm`), so no real value falls off either end.
- **Chosen, judged and counted** bands cannot be exhaustive by nature and are not expected to be. They must be ordered and mutually exclusive; they need not enumerate every conceivable option. **Do not invent ranges to close a "gap" in a menu** — see the note in section 6.

## 10. Put the depth in Background and Evidence basis

- Keep the question and parameter tight by **moving explanation down**: *why it matters*, and *the default the designer may have fallen into* → **Background**; *how the guidance was established, the sources, the caveats* → **Evidence basis**. These are the fields that are allowed to be long.
- Test: a reader should grasp the entry from **question + parameter + band headings alone**, then read Background and Evidence only if they want the reasoning. If they can't, something that belongs lower has been pulled up top.

## 11. Framing hygiene (quick)

- **De-identified** — no project, company, person or site names anywhere. The framing must be anonymous. (Naming a *product class* or a *material system* is fine where no other term exists; naming the job it came from is not.)
- **Region belongs in Location** — if the guidance is region-specific, say so in the Location field rather than writing the region into the question.
- **Keywords add non-obvious terms** — trade slang and alternative names a searcher might use, not words already in the entry text.
- **Consistent voice** — plain, direct, present tense.

---

## Quick checklist

Run this yourself, or paste it to an AI along with the entry:

- [ ] **Complete** — has a dimension, name, question, parameter, threshold bands, and applicability
- [ ] **Dimension** — the one whose description covers the decision being made
- [ ] **Question** — one concrete question, ~one sentence, no stacked decisions, doesn't state its own answer
- [ ] **Default** — any named failure mode sits in Background, not in the question
- [ ] **Parameter** — one thing you can act on, short noun phrase, units if numeric, one variable not two, *not* a description of the bands
- [ ] **Coherence** — the parameter actually answers the question; where they diverge, the parameter is usually right
- [ ] **Kind** — measured / chosen / judged / counted is framed honestly. A number off a standard menu (spacing, diameter, pod depth) is *chosen*, not *measured*
- [ ] **Counted entries list what they count** — if the parameter says "how many of the four", Background names the four, and the question does not contradict the count
- [ ] **Match** — bands are values/ranges/states/counts of that parameter; each band's guidance stays on that parameter
- [ ] **Headings** — 2–5 words / clean numeric ranges, no stray whitespace
- [ ] **Count** — as many bands as real breakpoints (often 2–4); ordered best→worst; rating string is one of the exact four
- [ ] **Padding** — are the two worst bands the same value of the parameter, split by a consequence? Does the last band open with "As above…"? If so: first check the parameter is named right (a padded-looking pair is often a mis-named parameter), and only then merge, carrying the escalation into the surviving guidance
- [ ] **Not a gradient** — a different *value* of the parameter earns its own band even when the action is the same. Don't merge an escalating gradient
- [ ] **No missing band** — can the parameter take a value no band names (a count that stops short of its own maximum, a menu option, a value past the worst band)? If so, does the reader get different advice there? If yes, a band is missing
- [ ] **Ratings** — they grade how much action the designer owes, not whether the project is good. A band describing a project fact (`0 fail`, `1 floor`) is not a defect
- [ ] **Coverage** — *measured* bands have no gaps, no overlaps, no point values; endpoints belong to one band only (`≤ 600` · `> 600 – 1000`); the best and worst bands are open-ended
- [ ] **Depth** — background and reasoning live in Background / Evidence basis, not the question or parameter
- [ ] **Hygiene** — de-identified; region in Location; keywords add non-obvious terms

---

## What this rubric is *not*

- It does **not** judge whether the guidance is correct or how well it's supported — that is the **evidence rating rubric**.
- It does **not** decide when an entry surfaces on a job — that is the **triage rating rubric**.
- It is purely about how the entry is **framed and shaped**: complete, under the right dimension, one clear question, one parameter you can act on that answers it, clean bands, depth pushed down into background and evidence.
