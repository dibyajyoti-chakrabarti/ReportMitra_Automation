# ReportMitra Infrastructure Automation

This repository manages **cost-optimized AWS infrastructure automation**
for the ReportMitra project using **GitHub Actions + AWS OIDC**.

## Key Highlights
- No AWS access keys used
- Secure GitHub → AWS authentication via OIDC
- Least-privilege IAM role
- Automated daily start/stop of EC2 and RDS
- Manual override workflows for testing and recovery

## Automation Schedule (IST)
- Start Infrastructure: **10:20 AM**
- Stop Infrastructure: **12:25 PM**

> Schedules are intentionally offset to account for GitHub Actions cron drift.

## Security Model
- GitHub Actions assumes an AWS IAM role using OpenID Connect
- No secrets or credentials are stored in this repository
- Role trust is scoped to this repo and the `main` branch only

## Workflows
- `infra-start.yml` – Scheduled + manual start
- `infra-stop.yml` – Scheduled + manual stop
- `infra-start-manual.yml` – Manual emergency/testing start

This setup reflects real-world DevOps best practices.
