# System Overview

## What aGorA does

aGorA monitors GitHub Actions failures, analyzes them with an AI remediation pipeline, and
surfaces suggested fixes for human approval. The platform is designed so the AI can suggest
changes, but only a human-triggered workflow can raise a pull request.

## End-to-end flow

1. GitHub sends a webhook when a workflow run fails.
2. `agora-webhook` verifies the payload and places a job on Amazon SQS.
3. `agora-worker` consumes the job, scrubs logs, runs the remediation graph, and stores results.
4. `agora-api` exposes remediation data to the dashboard and handles PR creation.
5. `agora-frontend` displays workflow history, AI findings, and review actions in real time.

## Core design principles

- Human approval remains mandatory before any code change is proposed upstream.
- Slow AI analysis is decoupled from webhook ingestion through queues.
- Observability, least privilege, and cost limits are part of the architecture rather than afterthoughts.
- Project structure is split by responsibility so application, infrastructure, and delivery concerns stay separable.
