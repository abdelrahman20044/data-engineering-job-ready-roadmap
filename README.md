# Abdelrahman's Job-Ready Data Engineering Roadmap

A compact, market-evidence-backed curriculum for a first Data Engineering internship or junior role in Egypt/MENA.

This repository is a **learning path**, not a dashboard. Every level answers four questions: what to learn, where to learn it, what to practise, and what proves completion.

## Start here

> **Current level:** [L01 · Advanced SQL Practice](01-sql-advanced-practice/README.md)<br>
> **First action:** take the 90-minute PostgreSQL diagnostic with hints and answers closed.<br>
> **Then:** study only the topics the diagnostic exposes; do not restart SQL from zero.

Open the level's `README.md` for the recommended path. Open its `resources.md` only when you need an alternative, Arabic explanation, book, lab, or reference.

## How the roadmap works

| File | Purpose |
|---|---|
| `README.md` inside a level | Ordered topics mapped directly to the resource you should use |
| `resources.md` inside a level | Vetted alternatives, Arabic/English resources, books, practice, references, and later material |
| [`projects/`](projects/flagship.md) | Implementation contracts that turn learning into proof |
| [`docs/`](docs/application-milestone.md) | Application milestone, curriculum rationale, and resource-audit record |

Difficulty: `●○○○○` introductory → `●●●●●` advanced. Hours are working estimates, not promises; diagnostics can shorten them.

## Tier 1 · SQL & Data Foundations — about 48 hours

| Level | Hours | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| [L01 · Advanced SQL Practice](01-sql-advanced-practice/README.md) | 14 | ●●●○○ | Existing SQL foundations | L02, L03 |
| [L02 · PostgreSQL & Performance Essentials](02-postgresql-performance/README.md) | 10 | ●●●○○ | L01 | L03, L11 |
| [L03 · Dimensional Modeling & Warehousing](03-dimensional-modeling-warehouse/README.md) | 24 | ●●●○○ | L01 | L05, flagship warehouse |

## Tier 2 · Build Reliable Pipelines — about 66 hours

| Level | Hours | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| [L04 · Python for Data Engineering](04-python-for-data-engineering/README.md) | 14 | ●●○○○ | Programming experience | L05, L06 |
| [L05 · API Ingestion, ETL & Incremental Loads](05-etl-api-incremental-loads/README.md) | 24 | ●●●○○ | L03, L04 | L06, L08 |
| [L06 · Testing & Data Quality](06-testing-data-quality/README.md) | 16 | ●●●○○ | L05 | L07, application milestone |
| [L07 · Git, Docker & Reproducible Delivery](07-git-docker-delivery/README.md) | 12 | ●●○○○ | L04–L06 | L08, application milestone |

## Tier 3 · Production Orchestration — about 26 hours

| Level | Hours | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| [L08 · Airflow & Orchestration](08-airflow-orchestration/README.md) | 16 | ●●●○○ | L05–L07 | L09 |
| [L09 · Backfills, Recovery & Reliability](09-airflow-reliability/README.md) | 10 | ●●●○○ | L08 | Production-style flagship |

## Tier 4 · Distributed Processing — about 40 hours

| Level | Hours | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| [L10 · PySpark DataFrames & Parquet](10-pyspark-dataframes/README.md) | 24 | ●●●○○ | L02, L04 | L11 |
| [L11 · Spark Performance Essentials](11-spark-performance/README.md) | 16 | ●●●●○ | L10 | Interview-ready Spark project |

## Tier 5 · Practical Cloud — about 24 hours

| Level | Hours | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| [L12 · Practical AWS for Data Engineering](12-practical-aws/README.md) | 24 | ●●●○○ | L07, preferably L09 | Cloud-deployed flagship |

## Tier 6 · Job-Triggered Extensions — variable

| Level | Hours | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| [L13 · Job-Triggered Electives](13-job-triggered-electives/README.md) | As justified | varies | Repeated demand from target jobs | One targeted stack gap |

Electives include dbt, Azure/ADF/Fabric/Databricks, Kafka, Hadoop/Hive refreshers, BI, and deeper CI/IaC. None delays the core path without repeated job-market evidence.

## Project path

### Flagship · API-to-Warehouse Data Platform

L01–L03 design the warehouse → L04–L05 build the Python pipeline → L06–L07 make it tested and reproducible → L08–L09 orchestrate and recover it → L12 deploy it on AWS.

Full contract: [`projects/flagship.md`](projects/flagship.md).

### Separate Spark project

L10–L11 build the PySpark mobility/clickstream pipeline. Spark stays separate because partitions, shuffles, Parquet, execution plans, and performance experiments require a scale-appropriate workload.

Full contract: [`projects/spark-project.md`](projects/spark-project.md).

## When to apply

- Apply selectively now to strong-fit internships and fresh-graduate roles.
- Start a consistent weekly cadence after **L07**, when the flagship has a defensible warehouse plus a tested, Dockerized, rerunnable pipeline.
- Add Airflow, Spark, and AWS evidence while applications are active.

Evidence checklist: [`docs/application-milestone.md`](docs/application-milestone.md).

## Study rule

**LEARN → PRACTISE → BUILD → DEBUG → EXPLAIN → PROVE → APPLY**

A watched course is not completion. A level is complete when the required output is inspectable and you can explain the decisions without notes.
