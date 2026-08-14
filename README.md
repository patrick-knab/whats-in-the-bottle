# What’s in the Bottle? — CBM field guide

An interactive, single-page companion website for **“What’s in the Bottle? A Survey and Roadmap of Concept Bottleneck Models”** by Patrick Knab, David Steinmann, Christian Bartelt, and co-authors.

The site is designed to give readers a fast overview of the CBM landscape before they dive into the full survey. It explains the canonical `x → c → y` framework, makes the survey’s four-module taxonomy browseable, curates representative literature by research question, and surfaces current challenges and open problems.

## Run locally

This is a static website with no build step or runtime dependencies. From this directory, either open `index.html` directly in a browser or start a small local server:

```bash
python3 -m http.server 8000
```

Then visit <http://localhost:8000>.

## What is included

- Framework overview: input → concept bottleneck → output, including inspection and intervention.
- Supplied paper figures: the pipeline, taxonomy, and intervention figures are rendered as web-ready PNGs in `assets/`.
- Taxonomy explorer: input, concept, output, and training modules; concept semantics and grounding are called out separately.
- Literature explorer: a prominent taxonomy matrix with grouped Input / Concept / Output / Training columns, full-text search, contribution filters, module filters, pagination, and sortable Paper / Year headers. It includes named primary CBM method papers, including newly added 2026 work; surveys, context papers, and umbrella placeholders are excluded from the matrix.
- Research trajectory: a compact view from the 2020 canonical CBM through current extensions.
- Open problems: concept quality, grounding, completeness, leakage, intervention utility, and scale.
- Responsive layout and accessible keyboard interactions for the taxonomy cards and literature filters.

## Content and sources

The primary source is the paper’s [OpenReview page](https://openreview.net/forum?id=IF5vnqxBEW). Publication metadata and the abstract are also available from the [DFKI publication page](https://www.dfki.de/web/forschung/projekte-publikationen/publikation/17340). The canonical CBM reference links to [Koh et al. (2020), Concept Bottleneck Models](https://proceedings.mlr.press/v119/koh20a.html).

The page includes a copyable BibTeX citation for the survey:

```bibtex
@article{
knab2026whats,
title={What{\textquoteright}s in the Bottle? A Survey and Roadmap of Concept Bottleneck Models},
author={Patrick Knab and David Steinmann and Christian Bartelt and Kristian Kersting and Bernt Schiele and Thomas Seidl and Udo Schlegel and Wolfgang Stammer},
journal={Transactions on Machine Learning Research},
issn={2835-8856},
year={2026},
url={https://openreview.net/forum?id=IF5vnqxBEW},
note={}
}
```

The literature cards and matrix are intentionally a readable orientation layer, not a replacement for the survey’s complete categorization of more than 100 works. The matrix is restricted to named primary CBM research contributions; survey/roadmap papers, broad context pieces, and synthetic “line of work” groupings are not counted as works. Search links are provided for thematic threads where a single stable paper URL is not assumed.

## Project notes

- The website is intentionally authored as a self-contained `index.html` so it can be hosted as a static page with minimal setup.
- The supplied PDFs were rasterized to PNG for reliable browser rendering; the original PDFs remain in the user’s Downloads folder.
- The literature matrix is a curated orientation layer, not the survey’s complete 100+ paper dataset. It deliberately excludes surveys and umbrella entries, and its taxonomy labels follow the supplied taxonomy figure as comparative reading aids rather than new empirical claims.
- The added bibliography entries use the supplied BibTeX as their source of truth. Taxonomy cells are lightweight orientation labels inferred from titles and publication metadata when the BibTeX does not contain enough detail for a precise architectural classification; `Misc.` is used conservatively.
- The “Suggest an addition” button opens a form for an arXiv link, paper description, and taxonomy classification, then creates a prefilled email draft addressed to `patrick.knab@tu-clausthal.de`.
