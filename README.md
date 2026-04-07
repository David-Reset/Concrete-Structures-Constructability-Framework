# Constructability Framework for Reinforced Concrete Design

A practical, evidence-based framework that helps structural engineers evaluate and improve the constructability of reinforced concrete design decisions during early project stages.

## What is this?

Structural design standards like AS 3600 ensure that reinforced concrete structures are safe and serviceable once completed. But structurally compliant designs can still be difficult, costly, or unsafe to construct if design decisions don't adequately consider construction processes, site constraints, material availability, and communication.
a
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
- **Recommended Actions** — what to do if you're in the concern or action required zone *(optional)*
- **Background** — why this matters for constructability *(optional)*
- **Evidence Basis** — how the guidance was established *(optional)*
- **Examples** — real design drawings tagged as Concern, Acceptable, or Recommended *(optional)*
- **Site Photos** — photographs showing what these issues look like in practice *(optional)*

Entries are date-stamped and designed to be updated as construction technology and practice evolve.

## Using the framework

### Live site
The framework is hosted at: **https://david-reset.github.io/Concrete-Structures-Constructability-Framework/**

Browse by dimension, read the general guidance, then explore specific entries relevant to your design decisions.

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
- **data.json** — all framework content lives here. This is the only file you edit to add, update, or remove entries.
- **images/** — all photographs and drawings referenced by entries in data.json.

## Contributing

### Suggesting an entry
If you have a constructability issue, design scenario, or practical insight that could benefit the framework, you can submit it via the **[suggestion form](https://forms.gle/5ppQRvJuzWaUkdg89)**.

Submissions are reviewed before being added to the framework to ensure quality and consistency.

### Adding an entry directly (maintainers)
1. Open `data.json`
2. Find the relevant dimension
3. Add a new entry object to the `items` array, following the structure of existing entries
4. Place any images in the `images/` folder with descriptive filenames
5. Reference images in the entry as `"images/your-filename.jpg"`
6. Commit and push

### Minimum required fields for a new entry
- Dimension
- Entry name
- Design question
- Design parameter
- At least one threshold band

All other fields (background, recommended actions, evidence, examples, site photos) can be added later as evidence builds.

## Context

This framework was developed as a final year engineering project at Deakin University (SEJ441/SEJ446). It is informed by academic literature, industry consultation, and practical project experience in reinforced concrete construction.

The framework draws on the principle — embedded in the [Engineers Australia Code of Ethics (2022)](https://www.engineersaustralia.org.au/publications/code-ethics) — that engineers should practise engineering to foster the health, safety and wellbeing of the community, and incorporate social, health, safety, environmental and economic considerations into the engineering task. In the context of structural design, "the community" includes the construction workers and contractors who must physically build what is designed.

## Important

This framework provides **supplementary design-stage guidance**. It does not replace compliance with structural design standards (e.g. AS 3600), applicable codes, or professional engineering judgement. All guidance should be applied within compliant design solutions and with appropriate consideration of project-specific conditions.

## Author

**David Harvey**
Deakin University
SEJ441 / SEJ446 Final Year Project
