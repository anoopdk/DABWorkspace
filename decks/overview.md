# Databricks Asset Bundle Workspace Starter

> Zynx Technologies | 3-slide delivery overview

---

## Slide 1: Context & problem

- Zynx x Digital Platform Client
- Engagement: Enablement / Foundation Delivery
- The Digital Platform Client needed a clean Databricks Asset Bundle (DAB) workspace baseline so engineering teams could deploy notebooks and jobs consistently across dev and prod targets without manual workspace drift.
- Engagement levels: Platform Assessment -> Foundation Scaffolding -> Job / Notebook Wiring -> Enablement Handover

---

## Slide 2: Solution architecture & stack

- Zynx delivered a DAB project scaffold (`dabproj1`) with bundle manifest, job resources, variables, notebook sources, fixtures, and local toolchain guidance for CLI and IDE workflows.
- Stack: Databricks Asset Bundles, Python, Notebooks, Jobs YAML, uv / pyproject
- Architecture documented in docs/03-architecture.md with Mermaid diagrams

---

## Slide 3: Implementation highlights & inspection

- Key evidence: dabproj1/databricks.yml, dabproj1/resources/, dabproj1/src/
- Open docs/audit/PROJECT-FACTSHEET.md for the audit index
- Repository standardised to Zynx industrial portfolio structure
- Portfolio tag target: 1.0.0-portfolio
