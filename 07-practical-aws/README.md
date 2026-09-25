# Module 07 — Practical AWS

## Why this matters

Cloud appeared in about 62% of early-career descriptions. AWS is first because Cloud Practitioner foundations already exist; the missing evidence is deploying and operating a real pipeline, not another broad certification syllabus.

## Prerequisites

The tested, containerized, Airflow-orchestrated flagship from Modules 01–05. An AWS account with billing alerts and MFA.

## Outcome

You can deploy a small, cost-controlled version of the flagship using S3, least-privilege IAM, managed secrets, an appropriate compute/database choice, and CloudWatch logs/alarms—and explain the trade-offs.

## Cost/safety gate

Before creating resources:

- Enable MFA and create a budget alert.
- Record the chosen region and rough cost drivers.
- Write teardown steps first.
- Never use root credentials or commit access keys.
- Prefer short-lived demonstrations and free/low-cost options; remove resources when evidence is captured.

## Topic path

### 1. Architecture decision, not service memorization

**Learn**

- In AWS Skill Builder, search for **Data Engineering on AWS Learning Plans (includes labs)**. Use only content relevant to storage, pipeline compute, security, monitoring, and cost; skip broad certification review.

**Read / reference**

- *Fundamentals of Data Engineering*: revisit Ch. 2 pp. 33–48 and 59–68 for lifecycle/architecture trade-offs.

**Practice**

- Compare two small deployment options, such as EC2 + RDS vs container task + RDS. Consider setup effort, runtime model, Airflow needs, monitoring, and cost.

**Apply**

- Commit an architecture decision record selecting the smallest architecture that proves deployment. A short-lived EC2/Compose deployment is acceptable; managed Airflow is not required.

### 2. S3 raw landing and lifecycle

**Learn / reference**

- [Getting started with Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/GetStartedWithS3.html).
- [S3 security best practices](https://docs.aws.amazon.com/AmazonS3/latest/userguide/security-best-practices.html).

**Practice**

- Create a private bucket/prefix layout, upload sample raw data, retrieve it programmatically through a role, and deny public access.

**Apply**

- Replace/extend the local raw landing with S3. Use predictable run/interval keys and document retention/lifecycle intent.

### 3. IAM and secrets

**Learn / reference**

- [IAM security best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html).
- [AWS Secrets Manager best practices](https://docs.aws.amazon.com/secretsmanager/latest/userguide/best-practices.html).

**Practice**

- Start with an intentionally insufficient role, observe the denial, then grant only the actions/resources required.

**Apply**

- Use an instance/task role rather than embedded keys. Retrieve database/API secrets at runtime and redact them from logs.

### 4. Compute and database deployment

**Learn / reference**

- Use the official documentation for the service chosen in the architecture decision. Do not tour services that are not in the design.

**Practice**

- Deploy a minimal container, verify network access to the database/S3, and test failure behavior before deploying Airflow/pipeline components.

**Apply**

- Run at least one real interval in AWS. If RDS cost is unsuitable, document and justify a smaller temporary database choice rather than pretending local PostgreSQL is managed cloud evidence.

### 5. CloudWatch, alarms, and operational proof

**Learn / reference**

- [Getting started with CloudWatch Logs](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/CWL_GettingStarted.html).
- [What is CloudWatch Logs?](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/).

**Practice**

- Send pipeline logs to CloudWatch, find one run by run/interval ID, and trigger one visible failure/alarm path.

**Apply**

- Capture successful and failed run evidence, log location, alarm condition, and recovery action. Record actual cost for the experiment and execute teardown.

## Module practice

- [ ] Budget alert and teardown plan exist before deployment.
- [ ] Private S3 landing accessed through a role.
- [ ] A least-privilege denial/fix is documented.
- [ ] Secrets stay outside code/images/logs.
- [ ] Successful and failed cloud runs are observable.
- [ ] Resources are stopped/deleted after the demonstration unless a cost reason to retain them is written.

## Build

Flagship Phase 5: cloud architecture diagram/ADR, S3 raw zone, secure role/secret flow, deployed compute/database, CloudWatch evidence, cost note, and teardown instructions.

## Interview check

Explain without notes:

1. Why AWS was chosen first.
2. Why you chose the specific compute/database approach.
3. Identity policy vs resource policy at a useful level.
4. How credentials and network access are controlled.
5. How an operator finds and diagnoses a failed run.
6. Main cost drivers and how the design limits them.

## Evidence

Architecture diagram, decision record, redacted IAM policy, deployment/run instructions, S3 layout, CloudWatch screenshots/log excerpts, failure recovery, cost and teardown notes.

## Done when

The flagship has completed a real cloud run, another engineer can understand the security/operations choices, no secrets are exposed, and unused resources have been torn down.

## Next

[Module 08 — Job-Triggered Electives](../08-job-triggered-electives/README.md)
