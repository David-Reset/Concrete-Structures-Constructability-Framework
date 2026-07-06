# Framework changelog

## 2026-07-06

**Summary:** 1 reviewed

### Reviewed
- **Suspended slabs: is the soffit-formwork zone workable?** (Construction Methods)

## 2026-07-03

**Summary:** 2 reviewed

### Reviewed
- **Rock sockets vs. likely available drilling plant** (Logistics)
- **Concrete columns/walls vs a blockwork-and-steel combination** (Construction Methods)

## 2026-07-02

**Summary:** 1 reviewed

### Reviewed
- **Non-combustible substructure and floor in bushfire areas** (Construction Methods)

## 2026-06-30

**Summary:** 2 reviewed

### Reviewed
- **Temporary loading of permanent works during construction** (Safety in Design)
- **Formwork and falsework complexity** (Safety in Design)

### Notes
_Maintainer tooling (Framework Review Console)._
- **Triage is now data-driven.** The questionnaire (gates, questions, universal opt-ins) moved out of `index.html` into a `triageConfig` block in `data.json`, so the live site reads it as data. A new **Triage** tab edits each entry's trigger with a plain-English "Surfaces when…" summary, shows how every fact surfaces, validates the set, runs a dry-run simulator, and edits the questions themselves — with safe rename/delete that repoints affected triggers.
- **Editable tags and automatic review dates.** Element and lifecycle tags now live in `data.json` (`config`) and can be added inline while tagging an entry, or renamed/removed in a tag manager that repoints or strips affected entries. Saving an edited entry now stamps its review date automatically.
- **Leaner changelog.** Exports record only what changed — added / reviewed / deleted / commented entries — dropping zero-count lines and the per-image file list (the file list still appears in the export dialog).

## 2026-06-27

**Summary:** 3 added

### Added
- **Non-combustible substructure and floor in bushfire areas** (Construction Methods)
- **Fire protection cost of steel beams in concrete floors** (Construction Methods)
- **Construction-joint necessity: where a pour must be broken, and where to place it** (Construction Methods)

## 2026-06-26

**Summary:** 1 reviewed

### Reviewed
- **Waffle pod depth availability** (Logistics)

## 2026-06-25

**Summary:** 1 added · 4 reviewed

### Added
- **Waterproofing buildability** (Detailing)

### Reviewed
- **Ground-bearing choice: stiffened raft vs. waffle pod slab** (Construction Methods)
- **Piling plant on access-constrained sites** (Logistics)
- **Slab edges and openings that can accept fall protection** (Safety in Design)
- **Bored concrete piles vs. screw piles** (Construction Methods)

### Notes
- **Related-entries tightening pass.** Pruned the related-entries graph from 91 links to 71. Removed two kinds of weak link: mutually-exclusive alternatives (e.g. the pile-supported and ground-bearing slab choices no longer cross-link, since choosing one rules the other out) and broad thematic glue (links justified only by a shared category — "early system-selection decision", "keeping workers safe during construction" — rather than a shared physical element or decision). Upstream/parent decisions and genuine co-occurring concerns were kept. Three entries now carry no related entries by design (off-form upturns near obstructions, reinforcement mat fall-through risk, confined-space entry at pier and shaft bases); each remains reachable via incoming links.

## 2026-06-24

**Summary:** 3 added · 2 reviewed

### Added
- **Pile-supported choice: flat plate vs beam-and-slab** (Construction Methods)
- **Repetition and the formwork learning curve** (Detailing)
- **Slab edges and openings that can accept fall protection** (Safety in Design)

### Reviewed
- **Ground-bearing choice: stiffened raft vs. waffle pod slab** (Construction Methods)
- **Reactive-ground strategy: found below vs. stiffen on top** (Construction Methods)

## 2026-06-23

**Summary:** 3 added

### Added
- **Ground-bearing choice: stiffened raft vs. waffle pod slab** (Construction Methods)
- **Reactive-ground strategy: found below vs. stiffen on top** (Construction Methods)
- **Waffle pod depth availability** (Logistics)

### Notes
- Foundation cluster for light ground floors added: the upstream reactive-ground strategy (found below vs. stiffen on top) and the two slab choices beneath it — ground-bearing (raft vs. waffle pod) and pile-supported (flat plate vs. beam-and-slab, added the following day) — plus the waffle pod depth-availability logistics check.

## 2026-06-22

**Summary:** 3 added

### Added
- **Temporary stability of retained or part-built structure** (Safety in Design)
- **Formwork and falsework complexity** (Safety in Design)
- **Isometric overview views in structural drawing sets** (Design Communication)

## 2026-06-21

### Notes
_Platform changes. The project review list, previously a single browser-local list, is now a workspace of multiple named lists._
- **Multiple project review lists.** You can now keep a separate review list for each project and switch between them from a **My project review lists** hub. The hub shows every list with its entry count and lets you open, rename, duplicate, delete, or delete-all.
- **Explicit add-to-list picker.** Adding an entry no longer drops it into a hidden "active" list. A picker opens showing every list with a checkbox — tick one, tick several to add to multiple projects at once, or un-tick to remove. The entry button shows how many lists an entry is on. New lists can be created and named inline via a styled dialog that suggests "Project review list N" and clears as you type.
- **Per-list and whole-workspace export/import.** **Export file** saves a single list; **Export all lists** saves every list as one backup file; either re-imports on any device. Imports reconcile by list, so re-importing updates the matching list instead of creating duplicates.
- The share-link, related-entries and triage flows now target the chosen list(s) rather than a single active list. The top-bar count now shows the number of lists that contain entries.
- _The entry sections dated 2026-06-12 to 2026-06-19 below were reconstructed from the `dateAdded` / `dateReviewed` fields in `data.json` to bring the log up to date; they were not exported individually at the time._

## 2026-06-19

**Summary:** 2 added

### Added
- **Bored concrete piles vs. screw piles** (Construction Methods)
- **Piling plant on access-constrained sites** (Logistics)

## 2026-06-18

**Summary:** 1 added · 1 reviewed

### Added
- **PVC permanent formwork vs core-filled blockwork** (Construction Methods)

### Reviewed
- **Waterproofing the non-moving construction joint at wall base** (Detailing)

## 2026-06-17

**Summary:** 1 added · 1 reviewed

### Added
- **Waterproofing the non-moving construction joint at wall base** (Detailing)

### Reviewed
- **Beam soffit formwork proportions** (Detailing)

## 2026-06-16

**Summary:** 1 added · 1 reviewed

### Added
- **Beam soffit formwork proportions** (Detailing)

### Reviewed
- **Foundation selection and the latent safety risk of screw piles** (Safety in Design)

## 2026-06-15

**Summary:** 7 added · 1 reviewed

### Added
- **Avoiding unnecessary large bars in slab reinforcement** (Detailing)
- **Drawing clarity for isolated large slab reinforcement** (Design Communication)
- **Reducing grinder cutting from large slab reinforcement bars** (Safety in Design)
- **Slab bar diameter and on-site bending equipment** (Logistics)
- **Foundation selection and the latent safety risk of screw piles** (Safety in Design)
- **Rock sockets: founding on rock vs. a drilled socket** (Construction Methods)
- **Rock sockets vs. likely available drilling plant** (Logistics)

### Reviewed
- **Concrete columns/walls vs a blockwork-and-steel combination** (Construction Methods)

### Notes
- Two themed clusters added: large-diameter slab reinforcement (bar selection, drawing clarity, on-site bending, grinder cutting) and pile / rock-socket foundation choices (founding vs drilled socket, plant availability, screw-pile safety).

## 2026-06-12

**Summary:** 1 reviewed

### Reviewed
- **Pour sequencing for deep vertical concrete elements at slab interfaces** (Construction Methods)

## 2026-06-09

**Summary:** 1 added

### Added
- **Structural steel vs concrete for isolated vertical members** (Construction Methods)

### Notes
_Platform changes, consolidated. These were built by editing the site rather than through the data manager, so they have no per-entry date; exact dates across late May–early June are approximate._
- Project **review list**: collect relevant entries into a private, browser-local list, give it a project name and purpose, and export it as a project-specific constructability checklist (PDF / Markdown / email-ready) with links back to the full entries.
- New **comment** contribution pathway, alongside the existing "suggest a new entry" and "suggest a change" forms — comments sit beneath an entry without altering it, and are reviewed and de-identified before publishing.
- Guide sections added and rendered on the site: **"Using the framework on a project"** (the review-list workflow) and **"Contributing feedback"** (the three pathways).
- Maintainer tooling — the **Framework Review Console** (data manager): loads `data.json`, CSV form submissions and the current `CHANGELOG.md`; provides a review inbox (accept/reject submissions), field-level diffing, image add/delete tracking, and one-step export of an updated `data.json` plus a dated changelog section. Handled submissions are tracked in `_processed` so they are not shown again.

## 2026-06-08

**Summary:** 1 added

### Added
- **Optional pour breaks to keep concrete trades flowing** (Construction Methods)

## 2026-06-05

**Summary:** 2 added

### Added
- **Curing shortfall in suspended slabs and beams** (Construction Methods)
- **Casting suspended members on freshly placed columns and walls** (Construction Methods)

## 2026-06-02

**Summary:** 3 added

### Added
- **Conventional RC vs post-tensioned: formwork cycling on repeated floors** (Construction Methods)
- **Drip grooves on exposed soffit edges** (Detailing)
- **Confined-space entry at pier and shaft bases** (Safety in Design)

## 2026-05-27

**Summary:** 1 added

### Added
- **Chamfered exposed external corners** (Detailing)

### Notes
- Review pass over earlier Design Communication entries (reinforcement callout clarity; details and schedule references).

## 2026-05-18

**Summary:** 1 added

### Added
- **Flat soffit detailing at minor slab setdowns** (Detailing)

## 2026-05-13

**Summary:** 1 added

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

**Summary:** 3 added

### Added
- **Off-form concrete upturns near obstructions** (Construction Methods)
- **Stirrup bar size availability and site adaptability** (Logistics)
- **Reinforcement callout clarity** (Design Communication)

## 2026-04-01

### Notes
- Renamed the dimension **Material Availability → Logistics**, broadening it to cover supply, site access, equipment and procurement.
- Reframed the framework as **dynamic and updateable** rather than a fixed checklist.

## 2026-03-15

**Summary:** 1 added

### Added
- **Reinforcement mat fall-through risk** (Safety in Design)

## 2026-03-11

### Notes
- Established the five constructability dimensions: Safety in Design, Detailing, Material Availability (later Logistics), Construction Methods, Design Communication.
- First worked safety principle: 200 × 200 mm practical maximum top-mat spacing to limit fall-through during placement.

## 2026-03-10

**Summary:** 1 added

### Added
- **Suspended slab level changes (folds)** (Detailing)

## 2026-03-04

### Notes
- Project inception: scope agreed as a constructability-aware framework for reinforced concrete design; literature review begun.

---

_History before the first data-manager export was reconstructed from the project supervision log and the `dateAdded` / `dateReviewed` fields in `data.json`. Entry dates are taken from the data; milestone and platform dates are approximate. From here on, each export from the Framework Review Console prepends a new dated section directly beneath the title above._
