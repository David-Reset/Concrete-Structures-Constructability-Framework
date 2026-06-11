# Framework changelog

## 2026-06-09

**Summary:** 1 added · 0 edited · 0 deleted

### Added
- **Structural steel vs concrete for isolated vertical members** (Construction Methods) — placeholder; spun out of the pour-staging entry as a distinct material-choice question.

### Notes
_Platform changes, consolidated. These were built by editing the site rather than through the data manager, so they have no per-entry date; exact dates across late May–early June are approximate._
- Project **review list**: collect relevant entries into a private, browser-local list, give it a project name and purpose, and export it as a project-specific constructability checklist (PDF / Markdown / email-ready) with links back to the full entries.
- New **comment** contribution pathway, alongside the existing "suggest a new entry" and "suggest a change" forms — comments sit beneath an entry without altering it, and are reviewed and de-identified before publishing.
- Guide sections added and rendered on the site: **"Using the framework on a project"** (the review-list workflow) and **"Contributing feedback"** (the three pathways).
- Maintainer tooling — the **Framework Review Console** (data manager): loads `data.json`, CSV form submissions and the current `CHANGELOG.md`; provides a review inbox (accept/reject submissions), field-level diffing, image add/delete tracking, and one-step export of an updated `data.json` plus a dated changelog section. Handled submissions are tracked in `_processed` so they are not shown again.

## 2026-06-08

**Summary:** 1 added · 0 edited · 0 deleted

### Added
- **Optional pour breaks to keep concrete trades flowing** (Construction Methods)

## 2026-06-05

**Summary:** 2 added · 0 edited · 0 deleted

### Added
- **Curing shortfall in suspended slabs and beams** (Construction Methods)
- **Casting suspended members on freshly placed columns and walls** (Construction Methods) — draft; not yet live.

## 2026-06-02

**Summary:** 3 added · 0 edited · 0 deleted

### Added
- **Conventional RC vs post-tensioned: formwork cycling on repeated floors** (Construction Methods)
- **Drip grooves on exposed soffit edges** (Detailing) — cross-linked with the chamfered-corner entry as a related edge treatment.
- **Confined-space entry at pier and shaft bases** (Safety in Design)

## 2026-05-27

**Summary:** 1 added · 0 edited · 0 deleted

### Added
- **Chamfered exposed external corners** (Detailing)

### Notes
- Review pass over earlier Design Communication entries (reinforcement callout clarity; details and schedule references).

## 2026-05-18

**Summary:** 1 added · 0 edited · 0 deleted

### Added
- **Flat soffit detailing at minor slab setdowns** (Detailing)

## 2026-05-13

**Summary:** 1 added · 0 edited · 0 deleted

### Added
- **Details and schedule references** (Design Communication)

### Notes
- Applied the new **Applicability and Limitations** field and the reordering pass to the live entries (suspended slab folds, reinforcement mat fall-through).

## 2026-05-12

### Notes
- Added an **Applicability and Limitations** section to every entry, placed before Recommended Actions so users see when an entry applies before choosing a response.
- Finalised dual licensing: **code under AGPL-3.0**, **content under CC BY-SA 4.0**.
- Refined the target audience to experienced design engineers with limited site experience.

## 2026-05-06

### Notes
- First presentation-ready build of the public site.
- Added the **region filter** (view entries by country or state, with country-level entries shown under any state) and **automatic relevance-ranked search** across all five dimensions.

## 2026-04-15

### Notes
- Published the public **GitHub repository** and live site, with `index.html` (interface), `data.json` (content) and `images/` separated.
- One fully built entry for each of the five dimensions, each backed by literature, supplier or project-experience evidence.
- Added the **form-based contribution pathway** (new-entry and edit-suggestion forms), with all submissions reviewed and de-identified before inclusion.

## 2026-04-08

### Notes
- Established the **four-level rating system** (Good practice / Consider / Concern / Action required).
- Adopted the **root-cause classification rule**: each entry belongs to exactly one dimension, chosen by the design decision that caused the issue.

## 2026-04-02

**Summary:** 3 added · 0 edited · 0 deleted

### Added
- **Off-form concrete upturns near obstructions** (Construction Methods)
- **Stirrup bar size availability and site adaptability** (Logistics)
- **Reinforcement callout clarity** (Design Communication)

## 2026-04-01

### Notes
- Renamed the dimension **Material Availability → Logistics**, broadening it to cover supply, site access, equipment and procurement.
- Reframed the framework as **dynamic and updateable** rather than a fixed checklist.

## 2026-03-15

**Summary:** 1 added · 0 edited · 0 deleted

### Added
- **Reinforcement mat fall-through risk** (Safety in Design)

## 2026-03-11

### Notes
- Established the five constructability dimensions: Safety in Design, Detailing, Material Availability (later Logistics), Construction Methods, Design Communication.
- First worked safety principle: 200 × 200 mm practical maximum top-mat spacing to limit fall-through during placement.

## 2026-03-10

**Summary:** 1 added · 0 edited · 0 deleted

### Added
- **Suspended slab level changes (folds)** (Detailing)

## 2026-03-04

### Notes
- Project inception: scope agreed as a constructability-aware framework for reinforced concrete design; literature review begun.

---

_History before the first data-manager export was reconstructed from the project supervision log and the `dateAdded` / `dateReviewed` fields in `data.json`. Entry dates are taken from the data; milestone and platform dates are approximate. From here on, each export from the Framework Review Console prepends a new dated section directly beneath the title above._
