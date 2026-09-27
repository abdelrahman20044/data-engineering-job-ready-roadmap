# L08 · Airflow & Orchestration

| Tier | Time | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| 3 · Production Orchestration | 16 hours | ●●●○○ | L05–L07 | L09 |

## What you will learn

Use Airflow to schedule and observe existing pipeline functions. Keep business logic outside the DAG and understand time semantics before adding production-style reliability.

## Topics and learning resources

| Order | Topic | Primary resource | Arabic / alternative | Action |
|---:|---|---|---|---|
| 1 | Orchestration mental model | *Data Pipelines with Apache Airflow*, 2e, Ch. 1 §§1.1–1.3 | — | Contrast orchestration with transformation and execution |
| 2 | Architecture | Book Ch. 2 §§2.2–2.6 + [Airflow core concepts](https://airflow.apache.org/docs/apache-airflow/stable/core-concepts/index.html) | — | Explain scheduler, executor, workers and metadata DB at a working level |
| 3 | DAGs, tasks and dependencies | [Airflow TaskFlow tutorial](https://airflow.apache.org/docs/apache-airflow/stable/tutorial/taskflow.html) + book Ch. 3 §§3.4–3.7 | [Astronomer Airflow 101](https://academy.astronomer.io/path/airflow-101) | Build a small DAG that calls existing functions |
| 4 | Connections, variables and logs | [Airflow connections](https://airflow.apache.org/docs/apache-airflow/stable/howto/connection.html), [variables](https://airflow.apache.org/docs/apache-airflow/stable/core-concepts/variables.html) + book Ch. 5 §§5.2–5.4 | — | Keep credentials/config out of DAG code and inspect task logs |
| 5 | Logical date and data interval | [Airflow DAG runs](https://airflow.apache.org/docs/apache-airflow/stable/core-concepts/dag-run.html) | — | Pass an interval explicitly to the pipeline |
| 6 | Clean DAG design | [Airflow best practices](https://airflow.apache.org/docs/apache-airflow/stable/best-practices.html) | — | Keep DAG parsing light and tasks independently rerunnable |
| 7 | Local execution and validation | [Running Airflow in Docker](https://airflow.apache.org/docs/apache-airflow/stable/howto/docker-compose/index.html) | — | Parse/test the DAG locally before depending on the UI |

## Practice

- Orchestrate one extract → validate → load path using existing package functions.
- Trigger one manual run and one scheduled run for a known interval.
- Move credentials to an Airflow connection or environment-backed secret.
- Inspect task logs and document the run’s data interval.
- Run a DAG parse/import check and test one task for a fixed interval from the CLI.

## Project application

Add `airflow/dags/` to the flagship. The DAG must coordinate code from `src/`; it must not duplicate transformation logic.

## Interview check

Explain DAG vs task, scheduler vs executor, logical date/data interval, connection vs variable, why top-level DAG code matters and orchestration vs business logic.

## Completion criteria

- [ ] The DAG imports quickly and contains orchestration only.
- [ ] Dependencies represent the real data flow.
- [ ] A scheduled interval is processed correctly.
- [ ] Logs and credentials are handled deliberately.

## Next

Continue to [L09 · Backfills, Recovery & Reliability](../09-airflow-reliability/README.md).

Exact book sections and alternatives are in [`resources.md`](resources.md).
