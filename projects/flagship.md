# Flagship — API-to-Warehouse Data Platform

## Purpose

Build one small but professional batch data platform that proves the fundamentals requested across early-career Data Engineering roles.

Choose a public API with stable historical records and a business process you can explain—for example, public transport, weather observations, e-commerce-like sample events, or another domain with measurable events. Avoid a source that requires scraping or complicated authentication.

## Evolution by level

| Level | Increment | Inspectable evidence |
|---|---|---|
| L01 · SQL | Analytical and validation queries | Independent SQL files, expected results, comments explaining non-obvious logic |
| L02 · PostgreSQL | Constraints, transactions and one measured performance decision | DDL constraints plus before/after plan note |
| L03 · Modeling | Business process, grain, fact-table type, measures, dimensions, keys, SCD decision, DDL | `docs/model.md`, star diagram, migrations/DDL, seed data, five business queries |
| L04 · Python | Maintainable package, CLI, configuration, logging and DB boundary | Package structure, reproducible command, transaction demonstration |
| L05 · ETL | Extract → stage → transform → load; pagination; incremental/late-arrival state; idempotency | Raw landing samples, state strategy, identical/overlap rerun and reconciliation evidence |
| L06 · Quality | Unit/integration/contract tests, quality dimensions and failure behavior | Passing tests, quality SQL, database-boundary and deliberate-failure evidence |
| L07 · Delivery | Git hygiene, Docker Compose, health checks, runbook and minimal CI | Clean checkout starts in one command; CI evidence |
| L08 · Airflow | DAG, schedule, dependencies, connections and interval handling | DAG code and successful scheduled-run evidence |
| L09 · Reliability | Retries, timeouts, trigger rules, backfills and monitoring | Failed/recovered runs, reconciled backfill, failure-propagation and recovery note |
| L12 · AWS | S3 raw/curated, EC2-hosted Dockerized workload, RDS PostgreSQL, IAM role, secrets, network boundary, CloudWatch and cost guardrails | Architecture diagram, deployment steps, logs, non-public DB evidence, teardown/cost note |

## Minimum architecture

`Public API → raw landing → validated staging → dimensional PostgreSQL warehouse → analytical SQL`

Airflow orchestrates existing pipeline functions; it must not contain the business logic itself. AWS replaces or extends local infrastructure only after the local system is repeatable.

The default cloud implementation is `API → EC2-hosted Dockerized pipeline/Airflow → S3 raw/curated + private RDS PostgreSQL → CloudWatch`. A single-EC2 PostgreSQL fallback is acceptable only when cost is the reason and the trade-off is explicit.

## Non-negotiable engineering behavior

- A rerun for the same interval does not create accidental duplicates.
- Credentials are not committed.
- Network calls have explicit timeouts and useful errors.
- Schema, uniqueness, null, accepted-value, and referential checks cover critical fields.
- Logs identify the run, interval, input/output counts, and failure point.
- The README includes architecture, setup, commands, trade-offs, known limits, and evidence.
- A clean machine can start the local stack from documented commands.

## Suggested repository shape

```text
api-to-warehouse-data-platform/
├── README.md
├── pyproject.toml
├── compose.yaml
├── .env.example
├── src/
│   └── pipeline/
│       ├── extract.py
│       ├── transform.py
│       ├── load.py
│       ├── quality.py
│       └── config.py
├── sql/
│   ├── ddl/
│   ├── transformations/
│   ├── quality/
│   └── analysis/
├── tests/
├── airflow/dags/
└── docs/
    ├── architecture.md
    ├── model.md
    └── runbook.md
```

Create folders only when their level begins; an empty skeleton is not evidence.

## Recruiter-verifiable claims

By the end, a reviewer should be able to verify that you can model data, write SQL, build and test an incremental batch pipeline, containerize it, orchestrate failures and backfills, deploy it safely, and explain the choices.
