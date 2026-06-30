# COcyber Map — Data Export

Complete export of the COcyber Map data (`/platform/cocyber-map`, the
`cocybermap` module). Generated from the 71 published `dataset` nodes and their
source CSV files (`public://dataset/`).

- **71 indicators** across 3 categories: Cybersecurity related projects (27),
  Cybersecurity skills (35), Cybersecurity related tenders (9).
- **2,122 data rows** in total (values by country).

## Files

| File | Description |
|------|-------------|
| `indicators.csv` / `indicators.json` | Index of the 71 indicators with their metadata (title, category, type, unit of measurement, reference year, source, description) and references to the data files. |
| `cocyber-map-full.json` | Complete export: each indicator with its metadata **and** all the nested data rows (`data`). |
| `cocyber-map-full.csv` | Complete export in *long* format: one row per (indicator, country) pair, with metadata repeated plus a `value` column. |
| `data/{nid}.csv` | Raw data for a single indicator (a copy of the source CSV), renamed by node id. |
| `data/{nid}.json` | The same per-indicator data in JSON. |

## Data columns per indicator

The files in `data/` keep the original columns: `Country`, `Abbr` (ISO),
`Indicator`, `Data` (the value).

## Notes

- `nid` is the Drupal node identifier, used as the key across all files.
- `source_file` in `indicators.*` gives the name of the original source CSV file
  (e.g. `6.csv`), which differs from the exported `data/{nid}.csv` file.
- Values are left exactly as in the source (e.g. `3.34%`, `635533.58`), without
  normalisation, to stay faithful to the original data.
