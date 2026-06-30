# Services And Repositories

## Application services

- `agora-frontend` provides the user interface for runs, remediations, analytics, and chat.
- `agora-api` owns authentication, REST APIs, websocket fan-out, and pull request creation.
- `agora-webhook` receives GitHub events and hands off processing safely.
- `agora-worker` runs the asynchronous remediation pipeline and investigation flows.
- `agora-mcp-github` exposes read-only GitHub tools to the AI workflows.

## Platform repositories

- `agora-helm` contains deployable Helm values and manifests consumed by ArgoCD.
- `agora-infra` provisions AWS infrastructure and cluster-level platform services.
- `agora-workflows` stores shared GitHub Actions workflows used across repositories.

## Recommended reading

- `agora-api/README.md`
- `agora-frontend/README.md`
- `agora-worker/README.md`
- `agora-webhook/README.md`
- `agora-infra/README.md`
- `agora-helm/README.md`
- `agora-workflows/README.md`
