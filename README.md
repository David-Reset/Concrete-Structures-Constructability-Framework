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
- **Examples** — real design drawings tagged as Concern, Acceptable, or Recommended *(optional)*
- **Supporting Images** — images, excerpts, diagrams, or site photographs that support the evidence or show what the issue looks like in practice *(optional)*
- **Related Entries** — links to other entries worth considering alongside this one (e.g. a chamfer detail and a drip groove on the same formed edge). Each link can carry a short note explaining why the other entry is relevant *(optional)*
- **Comments** — short community notes, observations, questions, or regional feedback left by readers and shown beneath the entry. Comments are reviewed and de-identified before they appear, and are shown anonymously by default *(optional)*
- **Search keywords** — extra words a searcher might type that aren't already written in the entry (synonyms, trade jargon, abbreviations), used to help the entry surface in search *(optional)*

Entries are date-stamped and designed to be updated as construction technology and practice evolve.

### Regional applicability

Constructability is influenced by local factors including material availability, labour practices, equipment access, supplier networks, and construction conventions. What is true in one region may not hold in another — even within the same country.

Every entry in the framework is tagged with the **location where its evidence was gathered** (e.g. "NSW, Australia"). This is not a claim that the guidance applies only to that location, but a transparent record of where the knowledge came from. Users can then judge for themselves whether the guidance is relevant to their own context.

The framework includes a **region filter** that allows users to view entries by country or by state/region within a country. Entries tagged at the country level (e.g. "Australia") appear when filtering by any state within that country. Entries tagged at the state level (e.g. "NSW, Australia") appear only when filtering by that specific state or by the country as a whole.

As the framework grows and receives contributions from different regions, users may find multiple entries addressing the same design question with different thresholds — for example, formwork clearance guidance based on NSW practices alongside separate guidance based on UK practices. This is expected and reflects the regional nature of construction knowledge.

## Using the framework

### Live site
The framework is hosted at: <a href="https://david-reset.github.io/Concrete-Structures-Constructability-Framework/" target="_blank"><strong>https://david-reset.github.io/Concrete-Structures-Constructability-Framework/</strong></a>

Browse by dimension, read the general guidance, then explore specific entries relevant to your design decisions. Use the region filter within each dimension to focus on entries relevant to your location.

### Searching
The home page has a search box that looks across **all five dimensions at once**. Describe your design problem in plain language — for example "wall close to a boundary", "stirrup size", or "curing" — and the framework returns the entries that best match, ranked with the strongest match first. You can also narrow results to a region.

Search is **automatic**: it reads the text already written in each entry (the name, design question, background and guidance) and matches your words against it. You don't need to know an entry's name, and nothing has to be tagged for an entry to be found. Rarer, more specific words (such as "boundary" or "stirrup") count for more than common ones (such as "wall" or "concrete"), and weak, incidental matches are dropped so results stay relevant. Maintainers can optionally reinforce this with [search keywords](#search-keywords-optional) on individual entries.

### Running locally
1. Clone or download this repository
2. Serve the files using any local web server (e.g. `python -m http.server` or VS Code Live Server)
3. Open `index.html` in your browser

> **Note:** Opening index.html directly as a file won't work — browsers block local JSON loading for security. You need a local server or host it online.

## Repository structure

```
├── index.html          # Framework interface (styling and rendering)
├── data.json           # All framework content (entries, guidance, thresholds, comments)
├── review.html         # Maintainer review console (turns form responses into data.json)
├── images/             # Example drawings and site photographs
└── README.md
```

- **index.html** — the framework shell. Contains all CSS, navigation, and rendering logic. You generally don't need to edit this.
- **data.json** — all framework content lives here. For routine additions you no longer hand-edit this file: the review console (`review.html`) reads the form responses and writes the updated file for you (see [Reviewing and publishing submissions](#reviewing-and-publishing-submissions-maintainers)). You can still edit it directly for advanced changes such as cross-references. Each entry includes a `location` field specifying the country and optionally the state where the evidence was gathered. The file also carries a hidden `_processed` key that the review console uses to remember which form responses it has already handled; the live site ignores it.
- **review.html** — a standalone, browser-based tool for maintainers. It runs entirely on your own machine (nothing is uploaded), turns the Google Form responses into properly structured entries, comments, and edits, and lets you review and de-identify each one before exporting an updated `data.json`.
- **images/** — all photographs and drawings referenced by entries in data.json.

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

Issues often touch more than one area even though each entry lives in a single dimension. Rather than duplicating an entry across dimensions, the framework links related entries together — so a designer reading one is pointed to the others worth considering, without the same issue being maintained in several places. See [Related entries](#related-entries-cross-references) below.

### Suggesting a new entry

If you have a constructability issue, design scenario, or practical insight that could benefit the framework, you can submit it via the <a href="https://docs.google.com/forms/d/e/1FAIpQLSdRkltPd-q5WRI_QFTWrsY-EGn0QlG2uf9zQtB_lYyQhSlq-Q/viewform" target="_blank">new entry suggestion form</a>. You can also reach it from the **"Suggest an entry"** button on the home page and at the foot of each dimension page (the dimension button pre-selects that dimension for you).

To see what a completed submission looks like, refer to the <a href="examples/Off-form-wall-example.pdf" target="_blank">example submission (PDF)</a> — this is the off-form wall entry as it was submitted through the form.

### Suggesting a change to an existing entry

If you believe an existing entry could be improved — for example, a threshold needs adjusting for your region, you have additional evidence or photographs, or you've identified an error — you can submit a change via the <a href="https://docs.google.com/forms/d/e/1FAIpQLSdTRRqO41OKp3Lxwz5CqVHL-B7IpAhitqnGqBWXYl1lmtizZA/viewform" target="_blank">edit suggestion form</a>, or via the **"Suggest a change"** button at the bottom of the entry itself (which opens the form already linked to that entry).

### Leaving a comment on an entry

To share a practical observation, a question, or regional feedback on a specific entry — without proposing a formal change — use the **"Add a comment"** button at the bottom of the entry, or the <a href="https://docs.google.com/forms/d/e/1FAIpQLScAywdw3JvZLIvUXrrGGxKNk60BZGkV3s5Mtx_QsEsZkI0WGw/viewform" target="_blank">comment form</a> directly. Approved comments are shown beneath the entry, anonymously by default.

All submissions — new entries, edits, and comments — are reviewed before being incorporated into the framework to ensure quality, consistency, and adherence to the anonymity standards described above. Nothing submitted through a form appears on the site automatically.

### Reviewing and publishing submissions (maintainers)

Form responses never go live on their own — nothing user-submitted is published until a maintainer has reviewed and de-identified it. This is handled by the **review console** (`review.html`), a self-contained tool that runs entirely in your browser (nothing is uploaded). It turns the raw form responses into properly structured entries, edits, and comments, lets you check and clean each one, and exports an updated `data.json`.

1. In Google Forms, open each form's **Responses** tab and download the responses as CSV (**⋮ → Download responses (.csv)**). You may have up to three CSVs — new entries, edits, and comments.
2. Open `review.html` in your browser (you can just double-click it — it works offline and uploads nothing).
3. Load the current `data.json`, then drag in the response CSV(s) — one, two, or all three, in any order. The console detects each form type automatically from the column headers and skips any response you've already processed. A **Loaded files** list shows what's in, and you can unload any file with its **×**.
4. Work through each item:
   - **New entries** arrive pre-filled and structured. Pick the dimension (if the submitter chose "Not sure"), confirm the auto-generated stable `id` (it warns if the id already exists), fill the `range` for each threshold band, add search keywords, and attach any de-identified images. A live preview beside each field shows exactly how it will look on the site.
   - **Edits** show the proposed change next to the live entry, so you apply it in place.
   - **Comments** show the parsed comment to approve, tidy, or skip; the displayed name follows the submitter's choice (or "Anonymous").
5. **De-identify as you go** — remove any project, company, client, or designer names, site addresses, or title blocks from text and images.
6. Accept or reject each item, then click **Download updated data.json**.
7. Add any new image files to the `images/` folder, then commit and push the updated `data.json` (and images).

Formatting is built in so you never need to write HTML: type normally, press Enter for line breaks, and use the **B** / **I** buttons or **Ctrl/⌘+B** / **Ctrl/⌘+I** to bold or italicise. The console also records which responses it has handled (via the hidden `_processed` key in `data.json`), so re-loading the same CSV later won't import anything twice.

### Editing data.json directly

For changes the review console doesn't cover — adding cross-references between entries, bulk edits, or fixing a small typo — you can still edit `data.json` by hand. Each entry is a JSON object inside its dimension's `items` array. A few rules to keep in mind:

- **Stable `id`** — every entry has a permanent `id`: a lowercase, hyphenated slug derived from the name (e.g. `"id": "drip-grooves-on-exposed-soffit-edges"`). This is the entry's permanent address — it appears in the entry's URL (`#dimId/id`) and is how other entries cross-reference it. **Once an entry is live, never change its `id`**, as doing so breaks shared links, bookmarks, and cross-references. The display `name` can change freely; the `id` should not.
- **`location`** — `"location": {"country": "Australia", "state": "NSW"}`; use just `country` if the evidence applies nationally, or include `state` if it is region-specific.
- **Images** — place files in the `images/` folder with descriptive filenames and reference them as `"images/your-filename.jpg"`. Keep filenames unique (the review console warns you if a name is already in use).
- Leave the `_processed` key alone — it belongs to the review console.

### Related entries (cross-references)

Cross-references are added by editing `data.json` directly — the review console doesn't manage them. An entry can point to others that a designer should consider alongside it. Add a `relatedEntries` array to the entry's `data` object:

```json
"relatedEntries": [
  {
    "id": "drip-grooves-on-exposed-soffit-edges",
    "note": "Both are edge treatments on the same formed face — coordinate them so the chamfer and drip groove don't clash."
  }
]
```

- Each link references the target by its stable `id` (not by position or display name), so links survive entries being reordered **and** renamed.
- `note` is optional — a short sentence explaining why the other entry is relevant. If omitted, just the link is shown.
- An entry can list as many related entries as needed, including entries in other dimensions.
- **Author each link once.** Links are automatically two-way: if entry A lists entry B, then entry B will also show A, without B needing a `relatedEntries` field of its own. There is no need — and you should avoid — adding the same pairing on both sides, as it will only drift out of sync. Add a link on both sides only if you genuinely want a *different* note in each direction.
- Links to entries that are not yet `available` are silently skipped, so you can author a link ahead of the target entry going live without producing a dead link.

### Search keywords (optional)

Search already works automatically on the text written in an entry, so most entries need nothing extra. The optional `keywords` field is a top-up: a place to add words a searcher might type that the entry doesn't already contain. You set these in the review console's **Search keywords** field when publishing an entry (or by hand in `data.json`); the guidance below applies either way.

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
