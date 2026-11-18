# Databricks Asset Bundle Workspace Starter

**Delivered by:** [Zynx Technologies Ltd](https://www.zynxtechnologies.com/)  
**Portfolio host (pre-fork):** `anoopdk/DABWorkspace`  
**Domain client (sanitised):** Zynx x Digital Platform Client  
**Engagement type:** Enablement / Foundation Delivery  
**Portfolio version:** `1.0.0-portfolio`

> Inspection note: Client identity is domain-aliased for public portfolio use. This repository is structured for authenticity review of delivery artefacts, architecture, and engagement scope.

## Project overview

The Digital Platform Client needed a clean Databricks Asset Bundle (DAB) workspace baseline so engineering teams could deploy notebooks and jobs consistently across dev and prod targets without manual workspace drift.

### Solution delivered

Zynx delivered a DAB project scaffold (`dabproj1`) with bundle manifest, job resources, variables, notebook sources, fixtures, and local toolchain guidance for CLI and IDE workflows.

## Engagement levels

| # | Level |
| --- | --- |
| 1 | Platform Assessment |
| 2 | Foundation Scaffolding |
| 3 | Job / Notebook Wiring |
| 4 | Enablement Handover |

| Field | Value |
| --- | --- |
| Engagement posture | Delivery portfolio artefact prepared for audit / inspection |
| Confidentiality | Domain alias only; no real client legal name in public docs |
| Primary artefacts | Code/notebooks/docs already in-repo + Zynx standard pack under `docs/` and `decks/` |

## Architecture

```mermaid
flowchart LR
  DEV[Local IDE / CLI] --> BUNDLE[databricks.yml bundle]
  BUNDLE --> RES[resources/jobs + variables]
  BUNDLE --> SRC[src notebooks]
  BUNDLE --> DEVWS[Dev workspace deploy]
  BUNDLE --> PRDWS[Prod workspace deploy]
```

### Implementation flow

```mermaid
flowchart TB
  T[Template scaffold] --> C[Configure targets]
  C --> D[databricks bundle deploy]
  D --> R[databricks bundle run]
  R --> V[Validate jobs in workspace]
```

## Technology stack

`Databricks Asset Bundles`, `Python`, `Notebooks`, `Jobs YAML`, `uv / pyproject`

## Repository map

| Path | Purpose |
| --- | --- |
| `README.md` | Project overview + engagement levels |
| `docs/` | Problem, solution, architecture, implementation, runbook, audit factsheet |
| `decks/` | 3-slide delivery overview (Markdown + HTML) |
| `src/` / project subtree | Implementation assets (or placeholders where design-led) |
| `tests/` | Tests or placeholders |
| `scripts/` | Operational / helper scripts |
| `configs/` | Non-secret configuration templates |
| `.env.example` | Environment variable placeholders |

### Key existing delivery paths

- `dabproj1/databricks.yml`
- `dabproj1/resources/`
- `dabproj1/src/`

## How to inspect this repository

1. Read this README (overview + engagement).
2. Open `docs/audit/PROJECT-FACTSHEET.md`.
3. Review architecture in `docs/03-architecture.md`.
4. Walk implementation evidence listed in the factsheet.
5. Open `decks/overview.html` for the 3-slide executive summary.

## Related Zynx context

Zynx Technologies Ltd provides IT consulting across cloud, data analytics, and digital delivery. This repository is part of the public delivery portfolio hosted on `anoopdk` prior to organisation-level fork.

## License

See `LICENSE`.
