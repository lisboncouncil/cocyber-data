# COcyber Data

Open data from the **[COcyber project](https://cocyber.eu)**.

This repository gathers the public datasets produced by COcyber and publishes them
in open, reusable formats (CSV and JSON) for researchers, policymakers and anyone
working on the European cybersecurity landscape.

## Datasets

| Folder | Description |
|--------|-------------|
| [`cocyber-map-export/`](cocyber-map-export/) | Complete export of the **COcyber Map**: 71 indicators across 3 categories (Cybersecurity related projects, Cybersecurity skills, Cybersecurity related tenders) with 2,122 data rows by country. See the [folder README](cocyber-map-export/README.md) for the full file layout. |
| [`project-landscape-export/`](project-landscape-export/) | Complete export of the **Cybersecurity Projects Landscape**: 89 EU-funded projects (Digital Europe and Horizon Europe) with 958 participations across partners and countries. See the [folder README](project-landscape-export/README.md) for the full file layout. |
| [`knowledge-base/`](knowledge-base/) | The COcyber **knowledge base**: a curated bibliography of cybersecurity research. `kb-export.csv` holds the cleaned export (580 references), while `kb-source.csv` holds the full source records (916 entries) with abstracts, DOIs, keywords and licensing metadata. |

## Formats

- **CSV** — for spreadsheets and quick analysis.
- **JSON** — for programmatic use, including the COcyber Map's complete export
  with nested per-country data.

Values are published as collected from the original sources, without
normalisation, to stay faithful to the source data.

## Licence

This work is licensed under a [Creative Commons Attribution 4.0 International
Licence (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You are free
to share and adapt the data for any purpose, provided you give appropriate credit
to the COcyber project. See the [`LICENSE`](LICENSE) file for the full text.

Note: individual references in the knowledge base may carry their own upstream
licences — see the `License` / `license` columns in the knowledge-base files.

## About COcyber

This repository is part of the **COcyber project** ([cocyber.eu](https://cocyber.eu)).

> Project 101158606 — DIGITAL-ECCC-2023-DEPLOY-CYBER-04 — Funded by the European Union.

The views and opinions expressed are however those of the author(s) only and do
not necessarily reflect those of the European Union or the European Cybersecurity
Competence Centre (ECCC). Neither the European Union nor the granting authority
can be held responsible for them.
