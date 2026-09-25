# Abdelrahman's Job-Ready Data Engineering Roadmap

An evidence-backed learning path for a first Data Engineering internship or junior role in Egypt/MENA.

This repository is the **study interface**: open the current module, follow its ordered path, produce the required evidence, then move on. Notion remains the Career OS for opportunities, applications, market research, and reviews. Project repositories contain the proof of work.

## Start here

> **You are here:** Module 01 — SQL & PostgreSQL  
> **Do now:** complete the 90-minute SQL diagnostic in [`01-sql-and-postgresql/README.md`](01-sql-and-postgresql/README.md).  
> **Then:** use the results to skip mastered basics and practice only the gaps.  
> **First proof:** independently solved SQL plus the first warehouse schema and analysis queries in the flagship project.

Do not start a beginner SQL or Python course by default. Your existing knowledge is tested with diagnostic gates.

## The path

| Order | Module | Main outcome | Project increment |
|---:|---|---|---|
| 1 | [SQL & PostgreSQL](01-sql-and-postgresql/README.md) | Write and reason about production-quality analytical SQL | Diagnostic, analysis queries, validation queries |
| 2 | [Dimensional Modeling & Warehousing](02-dimensional-modeling-and-warehousing/README.md) | Turn a business process into a defensible star schema | Business process, grain, facts, dimensions, SCD decision, DDL |
| 3 | [Python ETL](03-python-etl/README.md) | Build a rerunnable API-to-PostgreSQL batch pipeline | Extraction, staging, transformations, incremental load |
| 4 | [Testing, Data Quality & Delivery](04-testing-quality-delivery/README.md) | Make the pipeline testable, observable, and reproducible | pytest, quality checks, logs, Docker Compose, runbook |
| 5 | [Airflow](05-airflow/README.md) | Orchestrate and recover the flagship pipeline | DAG, scheduling, retries, backfill, monitoring |
| 6 | [Spark & PySpark](06-spark-pyspark/README.md) | Process a larger dataset with distributed reasoning | Separate PySpark mobility/clickstream project |
| 7 | [Practical AWS](07-practical-aws/README.md) | Deploy and operate the flagship safely on one cloud | S3, IAM, secrets, compute/database, logs, cost controls |
| 8 | [Job-Triggered Electives](08-job-triggered-electives/README.md) | Close repeated gaps in target jobs without delaying applications | Only the elective justified by several target roles |

The operating loop in every module is:

**UNDERSTAND → PRACTICE → BUILD → DEBUG → EXPLAIN → PROVE → APPLY**

## Projects

### 1. Flagship — API-to-Warehouse Data Platform

This is one system that becomes more professional as the roadmap progresses; it is not restarted for every tool.

1. SQL/modeling: define the business process and grain; create the star schema and analytical queries.
2. Python/ETL: ingest a real API, stage raw data, transform it, and load PostgreSQL incrementally.
3. Quality/delivery: add tests, data checks, logs, configuration, Docker Compose, and a runbook.
4. Airflow: orchestrate the same pipeline with retries, schedules, backfills, and observable failures.
5. AWS: deploy a cost-controlled version with S3, least-privilege access, secrets, and monitoring.

Full contract: [`projects/flagship.md`](projects/flagship.md).

### 2. PySpark Mobility / Clickstream Pipeline

Spark stays separate because partitions, shuffles, Parquet, execution plans, and performance experiments would be artificial additions to the flagship's small batch workload.

Full contract: [`projects/spark-project.md`](projects/spark-project.md).

## When to apply

- **Now:** apply selectively to strong-fit internships and fresh-graduate roles. Do not wait for every module.
- **Active weekly cadence:** begin after Modules 1–4 produce a defensible warehouse design and one tested, Dockerized, rerunnable Python pipeline.
- **While applying:** add Airflow, Spark, and AWS evidence. These strengthen coverage; they are not universal prerequisites for sending the first application.

See [`docs/application-milestone.md`](docs/application-milestone.md) for the evidence checklist and the 60–70% rule.

## Completion means evidence, not consumption

A module is complete only when another engineer can inspect the output and you can explain the decisions without notes. Videos watched, pages read, and course certificates are inputs—not proof.

Use this progression:

- **Learning:** you can follow an explanation.
- **Practiced:** you can solve a new exercise independently.
- **Portfolio evidence:** the skill is visible in working code, tests, design docs, or execution output.
- **Interview ready:** you can explain trade-offs, failure modes, and your implementation without notes.

## Deliberately postponed

Kafka, advanced Hadoop administration, Kubernetes, Terraform, deep lakehouse internals, multi-cloud depth, and advanced governance are **not** on the critical path. Learn one only when repeated target-job evidence or a real project requirement justifies it.

## Repository roles

| Place | Source of truth for |
|---|---|
| This repository | What to learn, in what order, with which practice and completion evidence |
| Notion Career OS | Current state, opportunities, applications, market evidence, weekly reviews, decisions |
| Project repositories | Executable proof: code, tests, diagrams, logs, READMEs, deployment |

Design rationale and resource verification live under [`docs/`](docs/curriculum-decisions.md); they are intentionally outside the everyday path.
