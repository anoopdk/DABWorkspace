# Architecture

## Context diagram

```mermaid
flowchart LR
  DEV[Local IDE / CLI] --> BUNDLE[databricks.yml bundle]
  BUNDLE --> RES[resources/jobs + variables]
  BUNDLE --> SRC[src notebooks]
  BUNDLE --> DEVWS[Dev workspace deploy]
  BUNDLE --> PRDWS[Prod workspace deploy]
```

## Implementation flow

```mermaid
flowchart TB
  T[Template scaffold] --> C[Configure targets]
  C --> D[databricks bundle deploy]
  D --> R[databricks bundle run]
  R --> V[Validate jobs in workspace]
```

## Design notes

- Prefer layered medallion / governed platform patterns where applicable.
- Keep configuration and secrets outside Git.
- Preserve auditability: documentation must match repository evidence.
