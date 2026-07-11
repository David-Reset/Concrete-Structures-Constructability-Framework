# Entry quality rubric

How to judge whether an entry is **well-framed** — consistently, regardless of who is reviewing.

This rubric is about the **shape** of an entry, not its content. It asks: does it have the parts it must have, is it under the right dimension, is the question one clear thing, is the parameter one thing you can act on, do the bands follow cleanly from it, and is everything as short as it can be? It does **not** judge whether the guidance is correct or well-supported (that is the [evidence rating rubric](evidence-rating-rubric.md)) or when the entry should surface on a job (that is the [triage rating rubric](triage-rating-rubric.md)).

---

## The core principle

> An entry asks **one concrete design question**, answered by **one design parameter you can act on**, split into **a few clearly-labelled threshold bands**. The question and parameter stay short; the depth goes into **Background** and **Evidence basis**.

Almost every framing problem is a version of putting the wrong thing in the wrong field — usually cramming detail into the question or the parameter that belongs in the bands, the background, or the evidence. Keep the top of the entry tight and let the lower fields carry the reasoning.

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
- Judge by the **question**, not the subject matter. An entry about reinforcement can sit under Detailing (how the bars are specified), Construction Methods (whether the cage can be built), Safety in Design (whether someone has to enter the excavation) or Design Communication (whether the callouts can be read) — the dimension follows **what is being decided**, not what the element is.
- If an entry seems to fit two dimensions, it is often **two questions**. Split it, or pick the dimension of the question you actually kept.
- Getting this wrong is a real defect, not a filing quibble: it is how a reader finds the entry at all.

## 2. The design question — one concrete question, briefly

- **One question, not several.** If it joins two separate decisions with "and" or "or", it's usually two questions — split it, or cut the second half. Often the second half ("…and at what point should alternatives be considered?") is really the bands talking, and doesn't belong in the question at all.
- **Concrete and answerable** from the drawings or the site, phrased as the actual question the entry answers.
- **Short — aim for a single sentence.** If it's running long, the extra context belongs in Background, not the question.

*Good:* "Can the pier or shaft base detail be completed from the surface, without a worker entering the excavation?" — one thing, one sentence.

## 3. The design parameter — one thing you can act on, short

- Names the **single thing** the reader measures, counts, selects, or assesses from their drawings, the site, or a supplier.
- A **short noun phrase**, with units if it's a number. Not a sentence, not a list of options.
- It must be the thing the **bands are values or states of**.
- It does **not** have to be a number — see the next section.

*Good:* "Top setdown depth (mm)" · "Specified stirrup, ligature or tie bar size" · "Clarity of reinforcement bar callouts".
*Bad:* a parameter that describes the bands — e.g. a paragraph naming every class of drilling plant. If your parameter is a paragraph, the bands have leaked into the wrong field: shorten the parameter to the thing being assessed and let the bands carry the detail.

## 4. The condition isn't always a number

The logic is always the same — **condition → band → response** — but the condition an entry checks can come from different places, and it is **not always a number**. Recognise which kind an entry is, and make sure the parameter and bands are framed for that kind rather than forced into fake numbers.

- **Measured** — you read a number from the documentation and find the range it falls in.
  *Parameter:* a quantity with units. *Bands:* numeric ranges.
  *Example:* "Top reinforcement bar spacing (mm)" → `≤ 200 mm` (Best practice) · `250 mm` (Concern) · `300 mm` (Action required).
- **Chosen** — you compare a specified choice rather than a number.
  *Parameter:* the choice being made. *Bands:* the options, best to worst.
  *Example:* "Specified stirrup, ligature or tie bar size" → `R10 or N12` (Best practice) · `N16` (Consider) · `R6` (Concern).
- **Judged** — there is no number at all; you assess something against described states, clearest to least clear.
  *Parameter:* what's being assessed. *Bands:* described states, best to worst.
  *Example:* "Clarity of reinforcement bar callouts…" → `Clean callouts` (Best practice) · `No laying order` (Consider) · `Count included` (Concern) · `Encoded notation` (Action required).

The same shapes cover conditions **confirmed** from site conditions or **checked** with suppliers — they still resolve to a measured number, a chosen option, or a judged state. Whichever kind it is, keep the parameter short and the band headings scannable (next sections).

## 5. Parameter and bands must agree

- Every band is a **value, range, or state** of the parameter — nothing else.
- Each band's guidance talks about **that** value of the parameter, not some other variable.
- If a band's guidance introduces a new measure the parameter never mentions, either the parameter is wrong, or that content belongs in Background.

This is the most important check: read the parameter, then read the band labels. They should obviously be the same thing.

## 6. Band headings — short and scannable (2–5 words)

- The heading is a **clean numeric range with units**, or a **2–5-word** categorical label.
- *Good:* "≥ 1000 mm" · "700–1000 mm" · "Socket into rock" · "R10 or N12" · "Clean callouts".
- *Too long:* "Standard-auger limit / rock-auger attachment". Tighten the heading; the full detail goes in the band's **guidance text**, not its heading.

## 7. As many bands as the reality has — no more

- Use the number of **natural breakpoints** the condition actually has. Two bands is perfectly fine; three and four are common. **Don't pad to four** for symmetry, and don't split one real threshold into two.
- Bands run **best → worst**, cover the range **without gaps or overlaps**, and each rating matches the severity of its guidance. The four ratings and their fixed colours are: **Best practice** (green), **Consider** (yellow), **Concern** (orange), **Action required** (red).

## 8. Put the depth in Background and Evidence basis

- Keep the question and parameter tight by **moving explanation down**: *why it matters* → **Background**; *how the guidance was established, the sources, the caveats* → **Evidence basis**. These are the fields that are allowed to be long.
- Test: a reader should grasp the entry from **question + parameter + band headings alone**, then read Background and Evidence only if they want the reasoning. If they can't, something that belongs lower has been pulled up top.

## 9. Framing hygiene (quick)

- **De-identified** — no project, company, person or site names anywhere. The framing must be anonymous.
- **Keywords add non-obvious terms** — trade slang and alternative names a searcher might use, not words already in the entry text.
- **Consistent voice** — plain, direct, present tense.

---

## Quick checklist

Run this yourself, or paste it to an AI along with the entry:

- [ ] **Complete** — has a dimension, name, question, parameter, threshold bands, and applicability
- [ ] **Dimension** — the one whose description actually covers the decision being made, judged by the question rather than the element
- [ ] **Question** — one concrete question, ~one sentence, no stacked decisions
- [ ] **Parameter** — one thing you can act on, short noun phrase, units if numeric, *not* a description of the bands
- [ ] **Kind** — measured / chosen / judged is framed honestly (no fake numbers on a chosen or judged entry)
- [ ] **Match** — bands are values/ranges/states of that parameter; each band's guidance stays on that parameter
- [ ] **Headings** — 2–5 words / clean numeric ranges
- [ ] **Count** — as many bands as real breakpoints (often 2–4), not padded; ordered best→worst; no gaps or overlaps; rating matches severity
- [ ] **Depth** — background and reasoning live in Background / Evidence basis, not the question or parameter
- [ ] **Hygiene** — de-identified; keywords add non-obvious terms

---

## The line this rubric does not cross

A quality review may **reframe** an entry — reword the question, tighten the parameter, rename a band, drop a padded band, move it to the right dimension, add search keywords. It must **not re-author the guidance**: don't move a threshold from 200 mm to 250 mm, don't change what a band means, don't invent evidence. Whether a number is *right* is the evidence rubric's job; this rubric only asks whether the entry is *shaped* so that a reader can act on it.

If reframing an entry would require changing what it actually claims, that is a signal to send it back to the submitter — not to quietly rewrite it.

---

## What this rubric is *not*

- It does **not** judge whether the guidance is correct or how well it's supported — that is the **evidence rating rubric**.
- It does **not** decide when an entry surfaces on a job — that is the **triage rating rubric**.
- It is purely about how the entry is **framed and shaped**: complete, in the right dimension, one clear question, one parameter you can act on, clean bands, depth pushed down into background and evidence.
