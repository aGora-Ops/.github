# Infrastructure And Operations

## Runtime environment

The platform runs on AWS with Kubernetes as the execution layer. Infrastructure is managed with
Terraform, while application delivery is handled through Helm and ArgoCD.

## Operational building blocks

- Amazon EKS hosts the application workloads.
- Amazon RDS PostgreSQL stores workflow, remediation, and chat data.
- Amazon ElastiCache Redis supports pub/sub, rate limiting, and Celery broker duties.
- Amazon SQS decouples webhook ingestion from worker processing.
- Amazon ECR stores container images with immutable tags.
- CloudWatch, CloudTrail, GuardDuty, and AWS Config provide monitoring and security visibility.

## Delivery model

1. Source changes trigger GitHub Actions workflows.
2. Images are built, scanned, and published.
3. Deployment values are updated in `agora-helm`.
4. ArgoCD reconciles the cluster to the desired state.

## Documentation intent

This folder is meant to be the starting point for project-wide documentation. As the platform
evolves, this section can grow with runbooks, environment notes, architecture decisions, and
service ownership details.
