## 🚀 CI/CD Status

![Build & Auto-Deploy](https://github.com/ritesh355/portfolio/actions/workflows/main.yml/badge.svg)

## 🔄 Deployment Workflow

```mermaid
flowchart LR
  A[Push to GitHub] --> B[GitHub Actions]
  B --> C[Build & Test]
  C --> D[Docker Build]
  D --> E[Push to Docker Hub]
  E --> F[SSH to EC2]
  F --> G[Pull New Image]
  G --> H[Stop & Remove Old Container]
  H --> I[Run New Container]
  I --> J{Is New Running?}
  J -- yes --> K[Success]
  J -- no --> L[Rollback to Previous]


----
## 🔄 Workflow Diagram
![Workflow Diagram](./assets/workflow.png)

