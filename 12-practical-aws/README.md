# L12 · Practical AWS for Data Engineering

| Tier | Time | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| 5 · Practical Cloud | 30 hours | ●●●○○ | L07, preferably L09 | Cloud-deployed flagship |

## What you will learn

Deploy the flagship with a small, secure and observable AWS architecture. The default target is **S3 raw/curated storage + a Dockerized pipeline/Airflow on one EC2 instance + PostgreSQL on RDS + CloudWatch**. If cost is the binding constraint, run PostgreSQL on the EC2 instance and document the reliability/security trade-off. Build on existing Cloud Practitioner knowledge; do not repeat a broad certification syllabus.

## Diagnostic gate · 45 minutes

Without a certification review, sketch the target architecture and explain the request/data path, IAM role, security-group rules, secret retrieval, log destination, main cost drivers, and teardown order. Write the minimum permissions the EC2 workload needs in plain language.

- Use the result to skip familiar service introductions and open only the official documentation needed for implementation.
- Cloud Practitioner knowledge can shorten study, but it does **not** skip this level: completion still requires a deployed, observable, cost-controlled pipeline with no long-lived credentials.

## Topics and learning resources

| Order | Topic | Primary resource | Arabic / alternative | Action |
|---:|---|---|---|---|
| 1 | Architecture and cost guardrail | [AWS Budgets](https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html) + [AWS Pricing Calculator](https://calculator.aws/) | — | Draw the default architecture, estimate it and define teardown rules before provisioning |
| 2 | S3 raw and curated zones | [S3 user guide](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html) + [lifecycle rules](https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lifecycle-mgmt.html) | AWS Skill Builder only for a specific gap | Store immutable raw and curated objects with deliberate prefixes, encryption and retention |
| 3 | IAM role and secrets | [EC2 IAM roles](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html), [IAM best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html) + [Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html) | — | Give the workload an instance role and retrieve secrets without long-lived access keys |
| 4 | Network boundary | [VPC security groups](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-security-groups.html) + [RDS access control](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.RDSSecurityGroups.html) | — | Permit only required traffic; keep PostgreSQL off the public internet |
| 5 | Compute and database | [EC2 user guide](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html) + [RDS for PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html) | — | Run the existing Dockerized pipeline on one EC2 instance; use RDS unless the documented cost fallback is chosen |
| 6 | Logs and failure signal | [CloudWatch Logs](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html) + [CloudWatch agent](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Install-CloudWatch-Agent.html) | — | Centralize pipeline logs and make one failed run visible |
| 7 | Security, cost and teardown | [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html) selected security/cost/reliability questions | — | Document access, costs, limits, backup choice and tested cleanup |

## Practice

- Create budget alerts before deploying billable resources.
- Upload sample raw/curated data with a defensible naming/prefix strategy.
- Give the EC2 workload only the S3/secret/log actions and resources it needs; do not put access keys in `.env`.
- Prove PostgreSQL is reachable from the workload but not publicly reachable.
- Run the pipeline, inspect centralized logs, trigger one failure, then tear resources down safely.

## Project application

Deploy the [flagship](../projects/flagship.md). Evidence includes an architecture diagram, sanitized configuration, successful run, CloudWatch logs, security/cost notes and teardown steps.

## Interview check

Explain object storage vs database, IAM role vs user, least privilege, security-group flow, secret handling, EC2/RDS choice and fallback, monitoring path, failure diagnosis and main cost drivers.

## Completion criteria

- [ ] The architecture is deployed and reproducible from documented steps.
- [ ] Credentials are absent from code and repository history.
- [ ] The workload uses an IAM role and the database is not publicly exposed.
- [ ] Logs identify a successful and a failed run.
- [ ] Cost guardrails and teardown instructions are tested.

## Next

Keep applying. Open [L13 · Job-Triggered Electives](../13-job-triggered-electives/README.md) only when repeated target-job evidence identifies the next gap.

Service choices and boundaries are in [`resources.md`](resources.md).
