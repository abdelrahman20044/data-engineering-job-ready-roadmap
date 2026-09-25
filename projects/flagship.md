# Flagship — API-to-Warehouse Data Platform

## Purpose

Build one small but professional batch data platform that proves the fundamentals requested across early-career Data Engineering roles.

Choose a public API with stable historical records and a business process you can explain—for example, public transport, weather observations, e-commerce-like sample events, or another domain with measurable events. Avoid a source that requires scraping or complicated authentication.

## Evolution by module

| Module | Increment | Inspectable evidence |
|---|---|---|
| 01 SQL | Analytical and validation queries | Independent SQL files, expected results, comments explaining non-obvious logic |
| 02 Modeling | Business process, grain, dimensions, facts, keys, SCD decision, DDL | `docs/model.md`, ER/star diagram, migrations/DDL, seed data, five business queries |
| 03 Python ETL | Extract → stage → transform → load; pagination; incremental state; idempotency | Package structure, CLI/entry point, raw landing samples, rerun demonstration |
| 04 Quality/delivery | Tests, checks, logs, configuration, Docker Compose, runbook | Passing test output, deliberate-failure evidence, health checks, one-command startup |
| 05 Airflow | Schedule, dependencies, retries, timeouts, backfill, monitoring | DAG code, successful and failed run screenshots/log excerpts, recovery note |
| 07 AWS | S3 landing, least-privilege IAM, secrets, compute/database, CloudWatch, cost guardrails | Architecture diagram, deployment instructions/IaC later if useful, logs, teardown/cost note |

## Minimum architecture

`Public API → raw landing → validated staging → dimensional PostgreSQL warehouse → analytical SQL`

Airflow orchestrates existing pipeline functions; it must not contain the business logic itself. AWS replaces or extends local infrastructure only after the local system is repeatable.

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

Create folders only when their module begins; an empty skeleton is not evidence.

## Recruiter-verifiable claims

By the end, a reviewer should be able to verify that you can model data, write SQL, build and test an incremental batch pipeline, containerize it, orchestrate failures and backfills, deploy it safely, and explain the choices.
