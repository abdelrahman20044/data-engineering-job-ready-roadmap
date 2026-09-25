# L12 · Practical AWS for Data Engineering

| Tier | Time | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| 5 · Practical Cloud | 24 hours | ●●●○○ | L07, preferably L09 | Cloud-deployed flagship |

## What you will learn

Deploy the flagship with a small, secure and observable AWS architecture. Build on existing Cloud Practitioner knowledge; do not repeat a broad certification syllabus.

## Topics and learning resources

| Order | Topic | Primary resource | Arabic / alternative | Action |
|---:|---|---|---|---|
| 1 | Architecture and cost guardrail | [AWS Architecture Center](https://aws.amazon.com/architecture/) + [AWS Budgets](https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html) | — | Draw the smallest architecture and set budget/teardown rules first |
| 2 | S3 landing and curated data | [S3 user guide](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html) | AWS Skill Builder data-engineering modules | Store raw/curated objects with clear prefixes and lifecycle choices |
| 3 | IAM and secrets | [IAM best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html) + [Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html) | — | Use least privilege and remove static credentials from code |
| 4 | Compute/database choice | AWS service docs for the chosen minimal option | AWS Skill Builder | Deploy the pipeline and PostgreSQL/warehouse component without a service tour |
| 5 | Logs and alerts | [CloudWatch logs](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html) | — | Centralize run logs and create one useful failure signal |
| 6 | Security, cost and teardown | [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html) selected pillars | — | Document access, cost estimate, limits and cleanup |

## Practice

- Create budget alerts before deploying billable resources.
- Upload sample raw/curated data with a defensible naming/prefix strategy.
- Give the workload only the actions/resources it needs.
- Run the pipeline, inspect logs, trigger one failure, then tear resources down safely.

## Project application

Deploy the [flagship](../projects/flagship.md). Evidence includes an architecture diagram, sanitized configuration, successful run, CloudWatch logs, security/cost notes and teardown steps.

## Interview check

Explain object storage vs database, IAM role vs user, least privilege, secret handling, compute choice, monitoring path, failure diagnosis and main cost drivers.

## Completion criteria

- [ ] The architecture is deployed and reproducible from documented steps.
- [ ] Credentials are absent from code and repository history.
- [ ] Logs identify a successful and a failed run.
- [ ] Cost guardrails and teardown instructions are tested.

## Next

Keep applying. Open [L13 · Job-Triggered Electives](../13-job-triggered-electives/README.md) only when repeated target-job evidence identifies the next gap.

Service choices and boundaries are in [`resources.md`](resources.md).
