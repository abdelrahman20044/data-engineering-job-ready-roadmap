# Module 05 — Airflow

## Why this matters

Airflow appeared in about 29% of the early-career sample. It is not as universal as SQL/Python, so it comes after a working tested pipeline. Now it solves a real problem: scheduling, dependencies, retries, backfills, and operational visibility.

## Prerequisites

Module 04 and a command-driven flagship whose business logic works without Airflow.

## Outcome

You can orchestrate the existing pipeline with a small Airflow 3 DAG, reason about data intervals/logical dates, recover failures, backfill safely, and keep business logic outside DAG files.

## Topic path

### 1. Architecture, DAGs, tasks, and dependencies

**Learn**

- [Astronomer Academy — Airflow 101](https://academy.astronomer.io/path/airflow-101): use it as the structured first pass through architecture, DAGs, tasks/operators, dependencies, and the UI.
- [Airflow 101: Building Your First Workflow](https://airflow.apache.org/docs/apache-airflow/stable/tutorial/fundamentals.html) for the current official implementation.

**Read**

- *Data Pipelines with Apache Airflow*, 2e: Ch. 1 §§1.1–1.3; Ch. 2 §§2.2–2.6; Ch. 3 §§3.4–3.7.

**Practice**

- Build a three-task toy DAG, inspect graph/grid views, and explain which component parses, schedules, and executes it.

**Apply**

- Wrap existing flagship commands/functions as thin tasks. Do not rewrite extraction/transformation logic inside the DAG file.

### 2. Scheduling, data intervals, catchup, and parameters

**Learn / reference**

- [Airflow DAG Runs](https://airflow.apache.org/docs/apache-airflow/stable/core-concepts/dag-run.html) for schedule behavior, data intervals, logical date, catchup, and run states.

**Read**

- Airflow book: Ch. 5 §§5.2–5.4; Ch. 6 §§6.1 and 6.4–6.6.

**Practice**

- On paper, map three daily DAG runs to their data intervals. Predict what catchup will create after two missed days, then verify locally.

**Apply**

- Pass interval boundaries explicitly to the flagship. Never use “current time” when the task should process the run's interval.

### 3. Retries, timeouts, idempotency, and connections

**Learn / reference**

- [Airflow core concepts](https://airflow.apache.org/docs/apache-airflow/stable/core-concepts/index.html) and current provider/connection docs linked from it.

**Practice**

- Configure bounded retries and a timeout for a simulated transient failure. Confirm a permanent data-contract failure does not retry endlessly.

**Apply**

- Store connection metadata outside code, use explicit retry/timeout behavior, and preserve the pipeline's idempotency across task retries.

### 4. Backfills, observability, and recovery

**Learn / reference**

- [Airflow backfill](https://airflow.apache.org/docs/apache-airflow/stable/core-concepts/backfill.html).
- [Airflow UI overview](https://airflow.apache.org/docs/apache-airflow/stable/ui.html).

**Read**

- Airflow book: Ch. 10 §§10.1 and 10.4; Ch. 12 §§12.1–12.3; Ch. 13 §§13.2–13.6.

**Practice**

- Cause one task to fail, diagnose it from task logs, fix it, clear/re-run only the necessary work, and run a two-interval backfill.

**Apply**

- Add a failure/recovery note showing the original signal, root cause, chosen rerun scope, and proof that target data stayed correct.

## Module practice

- [ ] Toy DAG completed before modifying the flagship.
- [ ] Logical date/data interval explained with concrete timestamps.
- [ ] Transient vs permanent failure behavior demonstrated.
- [ ] Backfill of two intervals succeeds without duplicates.
- [ ] Business logic remains importable/testable without Airflow.

## Build

Flagship Phase 3: a production-shaped DAG around the existing pipeline, including task dependencies, interval parameters, retries/timeouts, logs, backfill instructions, and a recovery example.

## Interview check

Explain without notes:

1. DAG vs DAG run vs task vs task instance.
2. Logical date/data interval vs wall-clock execution time.
3. Retries vs reruns vs backfills.
4. Catchup behavior.
5. Why tasks should be idempotent.
6. Why orchestration code should not own transformation business logic.

## Evidence

DAG code, graph/grid screenshot, successful scheduled run, deliberate failure logs, recovery/backfill note, and proof of correct target counts.

## Done when

You can predict scheduling behavior, recover one failure deliberately, backfill safely, and explain the DAG without treating Airflow as a cron wrapper.

## Next

[Module 06 — Spark & PySpark](../06-spark-pyspark/README.md)
