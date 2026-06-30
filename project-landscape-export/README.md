# Cybersecurity Projects Landscape — Data Export

Complete export of the **Project Landscape** projects
(`/platform/collateral-projects`, `cocyber_collateral_projects` module).
Generated from the 89 published `collateral_project` nodes, reusing the same
normalization as the `/platform/collateral-projects/json` endpoint (controller
`CollateralProjectsJsonController::normalize_detail`).

- **89 projects** (87 ongoing, 2 ended).
- **958 participations** (project–partner pairs).
- Programmes: Digital Europe (45), Horizon Europe (44).

## Files

| File | Description |
|------|-------------|
| `projects.json` | Complete export: each project with all base fields, the full `objective`, and the `participants` array. |
| `projects.csv` | One row per project, flat fields (`focus` joined by `; `, `participants_count`, `objective` included). |
| `participants.csv` | *Long* format: one row per (project, participant) pair, with country, ISO code, organization type, coordinator flag, and EU contribution. |

## Per-project fields (`projects.json`)

`id` (CORDIS project id), `acronym`, `title`, `status`, `topic`, `cluster`,
`programme`, `endDate`, `endYear`, `budget` (EU contribution in M€), `coordinator`,
`dualUse` (dual-use score), `focus` (array), `website`, `euPortalUrl`,
`objective`, `participants[]`.

Each participant: `pic`, `name`, `shortName`, `country`, `countryCode`,
`orgType`, `isCoordinator`, `euContribution`.

## Notes

- `cluster` and `programme`, when not set on the node, are inferred from the
  `topic` (same logic as the controller).
- 2 projects have no associated participants (CURIUM, SPECTRO).
- `budget` is the EU contribution in millions of euros (`field_eu_mln`).
