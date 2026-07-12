# Constructability Framework for Reinforced Concrete Design

A practical, evidence-based framework that helps structural engineers evaluate and improve the constructability of reinforced concrete design decisions during early project stages.

## What is this?

Structural design standards like AS 3600 ensure that reinforced concrete structures are safe and serviceable once completed. But structurally compliant designs can still be difficult, costly, or unsafe to construct if design decisions don't adequately consider construction processes, site constraints, material availability, and communication.
This framework bridges that gap. It provides structured, dimension-based guidance that translates practical construction knowledge into actionable design-stage recommendations — so that constructability issues are identified and resolved when changes are least costly.

## How it works

The framework is organised around **five dimensions** of constructability:

| Dimension | What it covers |
|---|---|
| **Safety in Design** | Design decisions affecting the safety of construction workers and other stakeholders |
| **Detailing** | Reinforcement detailing, slab geometry, and formwork |
| **Logistics** | Material and equipment availability, site access, and supply chain considerations |
| **Construction Methods** | System selection, buildability, and construction feasibility |
| **Design Communication** | Drawing clarity, notation, and communication with contractors |

Each dimension contains:
- **General guidance** — key principles for that area of design
- **Specific entries** — individual constructability issues with design parameters, threshold-based guidance, recommended actions, evidence, and real-world examples

### Entry structure

Every entry in the framework follows the same general display format:

- **Design Question** — what specific design question is being answered
- **Location** — the country and/or state where the evidence was gathered, shown near the entry heading (see [Regional applicability](#regional-applicability))
- **Background** — why this matters for constructability *(optional)*
- **Design Parameter** — what the engineer can measure, count, or assess from their drawings
- **Design Guidance** — threshold bands rated as Best practice, Consider, Concern, or Action required
- **Applicability and Limitations** — defines where the entry applies, lists factors the designer should check before applying the guidance, and provides a closing note framing the rating as a review prompt rather than a prohibition *(optional)*
- **Recommended Actions** — what to do if you're in the concern or action required zone, given as a numbered list of practical options. Each action can be a short instruction or a structured option with a title and longer description *(optional)*
- **Evidence Basis** — how the guidance was established *(optional)*
- **Evidence Support** — an Established, Directional, Indicative, or Reasoned indicator showing how far the entry's cut-offs (or its recommended call) rest on evidence rather than on our judgement. This does not rate whether the constructability issue is important or whether the guidance is mandatory *(optional)*
- **Examples** — real design drawings tagged as Concern, Acceptable, or Recommended *(optional)*
- **Supporting Images** — images, excerpts, diagrams, or site photographs that support the evidence or show what the issue looks like in practice *(optional)*
- **Related Entries** — links to other entries worth considering alongside this one (e.g. a chamfer detail and a drip groove on the same formed edge). Each link can carry a short note explaining why the other entry is relevant *(optional)*
- **Comments** — short community notes, observations, questions, or regional feedback left by readers and shown beneath the entry. Comments are reviewed and de-identified before they appear, and are shown anonymously by default *(optional)*
- **Search keywords** — extra words a searcher might type that aren't already written in the entry (synonyms, trade jargon, abbreviations), used to help the entry surface in search *(optional)*

Entries are date-stamped and designed to be updated as construction technology and practice evolve.

### Evidence support

Entries carry an **Evidence Support** rating on four levels: **Established**, **Directional**, **Indicative**, **Reasoned**.

The rating measures one thing: **how far you can trust the specific numbers (the threshold cut-offs), or the specific recommendation, that the entry asks you to act on.** It does not judge whether the constructability issue is real or important, and it does not make the guidance mandatory. A well-evidenced *mechanism* does not by itself earn a strong rating — the question is always whether the evidence backs the thing the reader actually acts on.

The level follows from three questions, asked in order:

1. **Is the mechanism evidenced, on point?** Is there a source strong enough to fix a number — direct measurement, a first-principles derivation from real component dimensions, peer-reviewed research, a statutory duty, or a materials/product standard — speaking to *this* issue rather than a neighbouring one? (Design codes such as AS 3600 are deliberately **not** part of the evidence base: they are the engineer's own ground, and the framework exists for the constructability question the code does not answer.)
2. **Does that evidence cover the numbers?** Every cut-off, or the recommended choice and the ordering of the options — not just the direction of the effect.
3. **Does a second, independent source confirm the same claim?** Independent means it *could have disagreed*. Two papers from one body, or two states adopting one national law, are one source, not two.

| Level | What it means |
|---|---|
| **Established** | Evidenced on point, and independently confirmed. Everything the entry asks you to act on rests on strong, on-point evidence, and an independent source or a documented real project confirms the same claim. |
| **Directional** | The direction is proven; the number is ours. The mechanism is evidenced on point, but the specific value you act on is a reasoned call — or the recommendation is backed and nothing independent confirms it. |
| **Indicative** | Plausible, but the evidence is about something else. The supporting sources are adjacent or analogous, however strong they are, so the entry is carried by inference. |
| **Reasoned** | Practitioner judgement, published so the gap is visible. Nothing on point confirms it. This is not a failing grade: publishing the gap is what invites the measurement, source or field experience that would close it. |

**Directional is where most live entries sit, and that is by design.** A proven mechanism with a reasoned cut-off is an honest, useful entry — and it is materially different from an entry that is mostly reasoning. The scale separates the two so a reader knows how far to lean on each.

**No level tells you what to do.** The rating grades *the framework's evidence*, not *your decision*. It tells you how much of an entry rests on sources and how much rests on our judgement — and therefore where your own scrutiny is most needed. The design, and the responsibility for it, remain yours at every level, including the top one.

The full rule maintainers follow — the four entry kinds (measured / chosen / judged / counted), the source grades, the proximity test and worked examples — is in [`tools/evidence-rating-rubric.md`](tools/evidence-rating-rubric.md). The same logic is shown to readers on the site's **Evidence support index**, which also lets them filter every live entry by level.

On dimension pages, Evidence Support is shown only as a compact rating beneath the design parameter so users can quickly see which entries are more developed and which may benefit from strengthening. Inside an entry, the same rating is shown near the bottom of the page with a short summary naming what backs the entry and where its main limitation lies.

### Regional applicability

Constructability is influenced by local factors including material availability, labour practices, equipment access, supplier networks, and construction conventions. What is true in one region may not hold in another — even within the same country.

Every entry in the framework is tagged with the **location where its evidence was gathered** (e.g. "NSW, Australia"). This is not a claim that the guidance applies only to that location, but a transparent record of where the knowledge came from. Users can then judge for themselves whether the guidance is relevant to their own context.

The framework includes a **region filter** that allows users to view entries by country or by state/region within a country. Entries tagged at the country level (e.g. "Australia") appear when filtering by any state within that country. Entries tagged at the state level (e.g. "NSW, Australia") appear only when filtering by that specific state or by the country as a whole.

As the framework grows and receives contributions from different regions, users may find multiple entries addressing the same design question with different thresholds — for example, formwork clearance guidance based on NSW practices alongside separate guidance based on UK practices. This is expected and reflects the regional nature of construction knowledge.

## Using the framework

### Live site
The framework is hosted at: <a href="https://david-reset.github.io/Concrete-Structures-Constructability-Framework/" target="_blank"><strong>https://david-reset.github.io/Concrete-Structures-Constructability-Framework/</strong></a>

Browse by dimension, read the general guidance, then explore specific entries relevant to your design decisions. Use the region filter within each dimension to focus on entries relevant to your location.

### Guided triage
Search and browse assume you already know the design decision you want guidance on. **Guided triage** works the other way round — for when you know the *project* but not yet which entries apply.

It asks what the design includes (suspended slabs, ground slabs, footings, walls, columns, piles, and cross-cutting conditions such as exposed concrete or a water-retaining structure), then a short set of follow-up questions revealed by those answers. Most read straight off the drawings; a few come from the geotechnical report, the site, or a decision you are still making. **"Not sure" counts as yes** — the entry surfaces, flagged as unconfirmed. That asymmetry is deliberate: a suggestion you don't need costs one line to skim, while an entry that never surfaces is missed silently.

Results come back in two groups:

- **Every job** — a small number of *standing* entries that apply to any reinforced-concrete design (every job has formwork to build and strip, and a drawing set with callouts, details and schedules). The group is collapsible and the preference is remembered, but nothing can hide these entries from a reader who has never seen them.
- **This job** — the entries your answers turned up, each showing which of your answers surfaced it.

Triage produces a **candidate list you curate**, not a verdict: you tick the entries worth keeping, and they go straight into a project review list. How maintainers decide when an entry surfaces is set out in [`tools/triage-rating-rubric.md`](tools/triage-rating-rubric.md).

### Searching
The home page has a search box that looks across **all five dimensions at once**. Describe your design problem in plain language — for example "wall close to a boundary", "stirrup size", or "curing" — and the framework returns the entries that best match, ranked with the strongest match first. You can also narrow results to a region.

Search is **automatic**: it reads the text already written in each entry (the name, design question, background and guidance) and matches your words against it. You don't need to know an entry's name, and nothing has to be tagged for an entry to be found. Rarer, more specific words (such as "boundary" or "stirrup") count for more than common ones (such as "wall" or "concrete"), and weak, incidental matches are dropped so results stay relevant. Maintainers can optionally reinforce this with [search keywords](#search-keywords-optional) on individual entries.

### Building project review lists
As you read, you can collect the entries that apply to a particular job into a **project review list**, then export that list as a project-specific constructability checklist. You can keep **several named lists at once** — one per project — and switch between them.

- **Adding entries.** On any live entry, use **Add to project review list**. A picker opens showing every list with a checkbox: tick one, tick several to add the entry to multiple projects at once, or un-tick to remove it. The button shows how many lists an entry is currently on, and you can create and name a new list from inside the picker.
- **Managing lists.** The **My project review lists** hub (the button in the top bar) shows every list with its entry count, and lets you open, rename, duplicate or delete each one, create new lists, or delete them all. The list you open becomes the one that exports and shares act on.
- **Naming and purpose.** Each list carries a name and an editable purpose statement (shown in exports). New lists suggest a generic "Project review list N" name you can keep or replace.
- **Exporting a checklist.** Any list can be exported to **PDF**, **Markdown**, or the clipboard, with links back to the full entries — ready for an email, design review or QA record.
- **Sharing.** **Copy share link** produces a link that reopens the live framework with that set of entries pre-selected — a review set that stays current, rather than a frozen PDF.
- **Backups across devices.** Lists are stored **in your browser only**, so clearing browser data or moving to another device won't carry them across. **Export file** saves one list and **Export all lists** saves every list as a single backup file; both re-import here later, on any device. Imports match by list, so re-importing updates a list rather than duplicating it.

### Running locally
1. Clone or download this repository
2. Serve the **`docs/`** folder with any local web server — e.g. `cd docs && python -m http.server`, or point VS Code Live Server at `docs/index.html`
3. Open the address it gives you in your browser

> **Note:** Opening `docs/index.html` directly as a file won't work — browsers block local JSON loading for security. You need a local server, or the live site.
>
> The maintainer **tools** are different: they're in `tools/`, and each is a single self-contained page you can just double-click. No server needed.

## Repository structure

```
├── docs/               # The published website — GitHub Pages serves the site from this folder
│   ├── index.html          # Framework interface (styling and rendering)
│   ├── data.json           # All framework content (entries, guidance, thresholds, comments)
│   ├── images/             # Example drawings and site photographs
│   ├── CHANGELOG.md        # Running record of what changed and when
│   └── manual/             # Maintainer's manual (step-by-step website — how to run everything)
├── tools/              # Maintainer tools — run locally in a browser; nothing is uploaded
│   ├── framework-data-manager.html      # Turn form responses into data.json; manage the inbox, drafts and comments
│   ├── framework-doctor.html            # Health-check data.json against the images folder
│   ├── framework-image-formatter.html   # Re-encode and rename images for the images/ folder
│   ├── evidence-rating-rubric.md        # How maintainers assign the four evidence-support levels
│   ├── triage-rating-rubric.md          # How maintainers decide when an entry surfaces on a job
│   └── entry-quality-rubric.md          # How maintainers judge whether an entry is well framed
├── examples/           # Example form submission (PDF)
├── LICENSE             # AGPL-3.0 (code)
├── LICENSE-CONTENT     # CC BY-SA 4.0 (content)
└── README.md
```

Two folders matter. **`docs/` is the published site** — everything the public sees is served straight out of it, which is why `data.json` and `images/` live there and not at the top level. **`tools/` is not part of the site**: the maintainer tools are pages you open on your own machine, so they sit outside `docs/`.

- **docs/** — the published website. GitHub Pages serves the live site from this folder, so anything in it is public.
- **docs/index.html** — the framework shell. Contains all CSS, navigation, and rendering logic. You generally don't need to edit this.
- **docs/data.json** — all framework content lives here. For routine additions you no longer hand-edit this file: the Data Manager (`tools/framework-data-manager.html`) reads the form responses and writes the updated file for you (see the [Maintainer's Manual](https://david-reset.github.io/Concrete-Structures-Constructability-Framework/manual/)). You only edit it by hand for the rare change the tools don't cover — the reactive-ground decision path. Each entry includes a `location` field specifying the country and optionally the state where the evidence was gathered. The file also carries a hidden `_processed` key that the Data Manager uses to remember which form responses it has already handled; the live site ignores it.
- **docs/images/** — all photographs and drawings referenced by entries in `data.json`.
- **docs/CHANGELOG.md** — the running record of changes; the Data Manager appends to it at export.
- **tools/** — three standalone, browser-based maintainer tools plus the three rubrics they use. Deliberately outside `docs/`, so they aren't published with the site. Each tool runs entirely on your own machine (nothing is uploaded); the [Maintainer's Manual](https://david-reset.github.io/Concrete-Structures-Constructability-Framework/manual/) explains how to use them.

## Ethics and anonymity

The framework includes real design scenarios and construction photographs to illustrate constructability issues. These are presented as **learning opportunities to improve future practice** — not as criticism of any individual designer, engineering firm, project, or client.

All design examples have been **de-identified**. No project names, company names, designer names, client names, or site locations are disclosed. Only the design details relevant to the constructability issue are shown, with all identifying information removed.

Contributors submitting entries through the suggestion form are similarly expected to de-identify any real project examples and ensure that no commercially sensitive, confidential, or personally identifiable information is included. Submissions are reviewed before being added to the framework to ensure these standards are maintained.

This approach is consistent with the principle that constructability knowledge — including knowledge gained from designs that proved difficult to construct — should be captured and shared to benefit the broader engineering and construction community, rather than remaining as unwritten lessons held by individuals.

## Contributing

### Choosing the right dimension

Each entry belongs to **one dimension only**, based on the **root cause** of the constructability issue — not just where the issue becomes visible.

For example, the "Off-form concrete walls near obstructions" entry sits under **Construction Methods**, not Detailing or Logistics. The wall detailing and site access are relevant, but the root cause is that the designer selected a construction method (conventional off-form concrete) without considering whether the site conditions could support it. If the same issue appeared multiple times across dimensions, the framework would become repetitive and harder to maintain.

When submitting an entry, ask: *what design decision caused this issue?* That points you to the right dimension.

Issues often touch more than one area even though each entry lives in a single dimension. Rather than duplicating an entry across dimensions, the framework links related entries together — so a designer reading one is pointed to the others worth considering, without the same issue being maintained in several places. These links are managed in the Data Manager (see the [Maintainer's Manual](https://david-reset.github.io/Concrete-Structures-Constructability-Framework/manual/)).

### Suggesting a new entry

If you have a constructability issue, design scenario, or practical insight that could benefit the framework, you can submit it via the <a href="https://docs.google.com/forms/d/e/1FAIpQLSdRkltPd-q5WRI_QFTWrsY-EGn0QlG2uf9zQtB_lYyQhSlq-Q/viewform" target="_blank">new entry suggestion form</a>. You can also reach it from the **"Suggest an entry"** button on the home page and at the foot of each dimension page (the dimension button pre-selects that dimension for you).

To see what a completed submission looks like, refer to the <a href="examples/Off-form-wall-example.pdf" target="_blank">example submission (PDF)</a> — this is the off-form wall entry as it was submitted through the form.

### Suggesting a change to an existing entry

If you believe an existing entry could be improved — for example, a threshold needs adjusting for your region, you have additional evidence or photographs, or you've identified an error — you can submit a change via the <a href="https://docs.google.com/forms/d/e/1FAIpQLSdTRRqO41OKp3Lxwz5CqVHL-B7IpAhitqnGqBWXYl1lmtizZA/viewform" target="_blank">edit suggestion form</a>, or via the **"Suggest a change"** button at the bottom of the entry itself (which opens the form already linked to that entry).

### Leaving a comment on an entry

To share a practical observation, a question, or regional feedback on a specific entry — without proposing a formal change — use the **"Add a comment"** button at the bottom of the entry, or the <a href="https://docs.google.com/forms/d/e/1FAIpQLScAywdw3JvZLIvUXrrGGxKNk60BZGkV3s5Mtx_QsEsZkI0WGw/viewform" target="_blank">comment form</a> directly. Approved comments are shown beneath the entry, anonymously by default.

All submissions — new entries, edits, and comments — are reviewed before being incorporated into the framework to ensure quality, consistency, and adherence to the anonymity standards described above. Nothing submitted through a form appears on the site automatically.

### Maintaining the framework

If you look after this framework — reviewing submissions, publishing entries, managing images — the full step-by-step guide is the **[Maintainer's Manual](https://david-reset.github.io/Concrete-Structures-Constructability-Framework/manual/)**. It follows a real entry through each tool, from a form response all the way to going live, and assumes no prior familiarity. Start there.

The tools, in short: three browser-based tools live in the `tools/` folder. Each is a single HTML file you open locally — they run entirely in your browser, upload nothing, and read or write only the files you hand them (`docs/data.json`, images and `docs/CHANGELOG.md`).

- **Data Manager** (`tools/framework-data-manager.html`) — the main tool. Turns Google Form responses into structured `data.json`: work through an inbox of new entries, edits and comments, de-identify and tidy each one, review unpublished drafts, and export the updated file. It also manages the "related entries" links between entries and repairs broken ones.
- **Framework Doctor** (`tools/framework-doctor.html`) — a read-only health check on `docs/`. Reports missing images, duplicate entry ids, broken cross-references, case-mismatched filenames (which work locally but break on the live server), finished drafts you forgot to publish, oversized images and internal notes about to be published. It changes nothing. Run it before you commit.
- **Image Formatter** (`tools/framework-image-formatter.html`) — re-encodes and uniquely names images for the `docs/images/` folder, and strips embedded GPS and camera metadata in the process.

The three rubrics beside them are written references, not programs. The Data Manager can load them and use them to drive an AI review; you can equally read them yourself:

- **Evidence rating rubric** (`tools/evidence-rating-rubric.md`) — how to assign an entry's evidence support (Established / Directional / Indicative / Reasoned). See [Evidence support](#evidence-support).
- **Triage rating rubric** (`tools/triage-rating-rubric.md`) — how to decide which jobs an entry should surface on, and when an entry is *standing* (shown on every job). See [Guided triage](#guided-triage).
- **Entry quality rubric** (`tools/entry-quality-rubric.md`) — how to judge whether an entry is *well framed*: one clear question, one parameter you can act on, bands that follow from it.

Almost everything is done inside the tools. The one thing edited by hand in `data.json` is the branching *decision path* that links the reactive-ground entries together; the manual shows exactly what that looks like.

### Search keywords (optional)

Search already works automatically on the text written in an entry, so most entries need nothing extra. The optional `keywords` field is a top-up: a place to add words a searcher might type that the entry doesn't already contain. You set these in the Data Manager's **Search keywords** field when publishing an entry (or by hand in `data.json`); the guidance below applies either way.

Add a keyword only if **both** of these are true:

1. **Someone would actually type it** when looking for this entry — a real term people use (including trade slang and regional words like "reo"), an abbreviation, a common misspelling, or the plain-language way someone describes the problem before they know the formal name.
2. **It isn't already in the entry's written text** (name, question or background). If the word is already there, the search finds the entry anyway and the keyword does nothing.

```json
"keywords": ["upstand", "nib", "kerb", "reo size", "single-sided formwork"]
```

A couple of extra pointers:
- Don't bother with very common words like "concrete", "slab" or "design" — they appear in almost every entry, so they won't help anyone find *this* one (and can pull it into unrelated searches).
- A handful per entry is plenty. The best time to add a keyword is when you notice a search that *should* have found the entry but didn't.

### Minimum required fields for a new entry
- Dimension
- Stable `id` (lowercase hyphenated slug)
- Entry name
- Design question
- Design parameter
- At least one threshold band
- Location (country, and state if applicable)

All other fields (background, recommended actions, applicability and limitations, evidence, examples, site photos, search keywords) can be added later as evidence builds.

## Context

This framework was developed as a final year engineering project at Deakin University (SEJ441/SEJ446). It is informed by academic literature, industry consultation, and practical project experience in reinforced concrete construction.

The framework draws on the principle — embedded in the [Engineers Australia Code of Ethics (2022)](https://www.engineersaustralia.org.au/publications/code-ethics) — that engineers should practise engineering to foster the health, safety and wellbeing of the community, and incorporate social, health, safety, environmental and economic considerations into the engineering task. In the context of structural design, "the community" includes the construction workers and contractors who must physically build what is designed.

## Important

This framework provides **supplementary design-stage guidance**. It does not replace compliance with structural design standards (e.g. AS 3600), applicable codes, or professional engineering judgement. All guidance should be applied within compliant design solutions and with appropriate consideration of project-specific conditions.

Framework ratings (Best practice, Consider, Concern, Action required) are intended as prompts for design-stage evaluation, not prohibitions. A rating of 'Action required' may not mean the design cannot proceed — it means the designer should recognise the constructability challenge, consider alternatives, and make an informed decision in the context of their specific project. In some cases, the flagged detail may still be the most practical solution when weighed against the full design context.

## Authors and acknowledgements

**David Harvey**
Author and copyright holder
SEJ441 / SEJ446 Final Year Project

**Kazem Ghabraie**
Project supervisor
Associate Professor, Deakin University, School of Engineering

## Licence

Copyright (C) 2026 David Harvey

This project is released under two licences to ensure it remains open in perpetuity:

- The **code** (HTML, CSS, JavaScript — principally `index.html`) is licensed under the [GNU Affero General Public License v3.0 (AGPL-3.0)](https://www.gnu.org/licenses/agpl-3.0.html). The full licence text is in [`LICENSE`](LICENSE).
- The **content** (framework entries in `data.json`, written descriptions, design parameters, guidance text, drawings, and photographs) is licensed under [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/). The notice and attribution details are in [`LICENSE-CONTENT`](LICENSE-CONTENT).

Both are **copyleft** licences. Anyone may use, modify, and redistribute the framework, but any derivative work — including a modified version run as a web service — must remain open under the same terms. Together they ensure the framework cannot be forked, modified, and re-released as a closed or proprietary resource.

When reusing or adapting framework content, please attribute as:

> "Constructability Framework — RC Design Guidance" by David Harvey, licensed under CC BY-SA 4.0.
> Source: https://github.com/david-reset/Concrete-Structures-Constructability-Framework
