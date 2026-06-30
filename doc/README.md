# aGorA Documentation

This folder collects project-level documentation for the full aGorA platform.

## Documentation map

- [System overview](./system/README.md)
- [Services and repositories](./services/README.md)
- [Infrastructure and operations](./operations/README.md)

## Project layout

- `agora-api` - FastAPI backend for auth, APIs, PR creation, and websocket updates
- `agora-frontend` - Next.js dashboard for workflow visibility and remediation review
- `agora-worker` - Celery-based AI remediation and investigation worker
- `agora-webhook` - GitHub webhook ingestion service
- `agora-mcp-github` - Read-only MCP server used by the AI workflows
- `agora-helm` - Helm charts deployed by ArgoCD
- `agora-infra` - Terraform for AWS and platform provisioning
- `agora-workflows` - Shared GitHub Actions workflows
- `profile` - GitHub organization profile README
- `agora` - Shared visual assets and the project slide deck

## Source material

Original work from the third and final reviews is available at [PACE-Stagecraft](https://github.com/PACE-Stagecraft/).

The presentation deck is available here: [aGorA Autonomous CI/CD deck](../agora/aGorA_Autonomous_CI_CD%20%281%29.pptx).
