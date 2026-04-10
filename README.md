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

Every entry in the framework follows the same format:

- **Design Question** — what specific design question is being answered
- **Design Parameter** — what the engineer can measure, count, or assess from their drawings
- **Design Guidance** — threshold bands rated as Good practice, Consider, Concern, or Action required
- **Location** — the country and/or state where the evidence was gathered (see [Regional applicability](#regional-applicability))
- **Recommended Actions** — what to do if you're in the concern or action required zone *(optional)*
- **Background** — why this matters for constructability *(optional)*
- **Evidence Basis** — how the guidance was established *(optional)*
- **Examples** — real design drawings tagged as Concern, Acceptable, or Recommended *(optional)*
- **Site Photos** — photographs showing what these issues look like in practice *(optional)*

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

### Running locally
1. Clone or download this repository
2. Serve the files using any local web server (e.g. `python -m http.server` or VS Code Live Server)
3. Open `index.html` in your browser

> **Note:** Opening index.html directly as a file won't work — browsers block local JSON loading for security. You need a local server or host it online.

## Repository structure

```
├── index.html          # Framework interface (styling and rendering)
├── data.json           # All framework content (entries, guidance, thresholds)
├── images/             # Example drawings and site photographs
└── README.md
```

- **index.html** — the framework shell. Contains all CSS, navigation, and rendering logic. You generally don't need to edit this.
- **data.json** — all framework content lives here. This is the only file you edit to add, update, or remove entries. Each entry includes a `location` field specifying the country and optionally the state where the evidence was gathered.
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

### Suggesting a new entry

If you have a constructability issue, design scenario, or practical insight that could benefit the framework, you can submit it via the <a href="https://forms.gle/5ppQRvJuzWaUkdg89" target="_blank">new entry suggestion form</a>.

To see what a completed submission looks like, refer to the <a href="examples/Off-form-wall-example.pdf" target="_blank">example submission (PDF)</a> — this is the off-form wall entry as it was submitted through the form.

### Suggesting a change to an existing entry

If you believe an existing entry could be improved — for example, a threshold needs adjusting for your region, you have additional evidence or photographs, or you've identified an error — you can submit a change via the <a href="https://forms.gle/xJ5tpUf7zozpkbcg6" target="_blank">edit suggestion form</a>.

All submissions (new entries and edits) are reviewed before being incorporated into the framework to ensure quality, consistency, and adherence to the anonymity standards described above.

### Adding an entry directly (maintainers)
1. Open `data.json`
2. Find the relevant dimension
3. Add a new entry object to the `items` array, following the structure of existing entries
4. Include the `location` field: `"location": {"country": "Australia", "state": "NSW"}` — use just `country` if the evidence applies nationally, or include `state` if it is region-specific
5. Place any images in the `images/` folder with descriptive filenames
6. Reference images in the entry as `"images/your-filename.jpg"`
7. Commit and push

### Minimum required fields for a new entry
- Dimension
- Entry name
- Design question
- Design parameter
- At least one threshold band
- Location (country, and state if applicable)

All other fields (background, recommended actions, evidence, examples, site photos) can be added later as evidence builds.

## Context

This framework was developed as a final year engineering project at Deakin University (SEJ441/SEJ446). It is informed by academic literature, industry consultation, and practical project experience in reinforced concrete construction.

The framework draws on the principle — embedded in the [Engineers Australia Code of Ethics (2022)](https://www.engineersaustralia.org.au/publications/code-ethics) — that engineers should practise engineering to foster the health, safety and wellbeing of the community, and incorporate social, health, safety, environmental and economic considerations into the engineering task. In the context of structural design, "the community" includes the construction workers and contractors who must physically build what is designed.

## Important

This framework provides **supplementary design-stage guidance**. It does not replace compliance with structural design standards (e.g. AS 3600), applicable codes, or professional engineering judgement. All guidance should be applied within compliant design solutions and with appropriate consideration of project-specific conditions.

## Authors

**David Harvey**
SEJ441 / SEJ446 Final Year Project

**Kazem Ghabraie**
Associate Professor
Deakin University, School of Engineering
