# L09 · Backfills, Recovery & Reliability

| Tier | Time | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| 3 · Production Orchestration | 10 hours | ●●●○○ | L08 | Production-style flagship |

## What you will learn

Make an Airflow pipeline safe to retry, backfill and diagnose. Reliability comes from idempotent task behavior plus explicit operational evidence—not from adding more operators.

## Topics and learning resources

| Order | Topic | Primary resource | Arabic / alternative | Action |
|---:|---|---|---|---|
| 1 | Retries and timeouts | Airflow task/DAG docs + book Ch. 6 §§6.1, 6.4–6.6 | — | Set bounded retries, delays and timeouts by failure type |
| 2 | Idempotent task design | [Airflow best practices](https://airflow.apache.org/docs/apache-airflow/stable/best-practices.html) | — | Make every task safe for the same interval to rerun |
| 3 | Catchup and backfills | [Airflow backfill](https://airflow.apache.org/docs/apache-airflow/stable/core-concepts/backfill.html) + book Ch. 10 §§10.1, 10.4 | — | Backfill a small historical range and verify counts |
| 4 | Inter-task data and sensors | Book Ch. 12 §§12.1–12.3 | Astronomer Learn | Pass references/metadata, not large payloads; add only a justified wait |
| 5 | Monitoring and operations | Book Ch. 13 §§13.2–13.6 + Airflow UI docs | — | Diagnose one failed run and write the recovery steps |

## Practice

- Inject a transient failure and observe retry behavior.
- Rerun a successful interval and prove no duplicate effects.
- Backfill at least three historical intervals.
- Make one task time out; capture the useful evidence and improve configuration.
- Document what an operator checks first when a run fails.

## Project application

Add retry/timeout policies, interval-aware state, backfill evidence, failure screenshots/log excerpts and a short runbook to the flagship.

## Interview check

Explain retryable vs non-retryable failures, catchup vs backfill, idempotency, XCom limitations, sensors vs polling inside tasks, timeout choices and first-line failure diagnosis.

## Completion criteria

- [ ] Same-interval reruns are safe.
- [ ] A small historical backfill reconciles successfully.
- [ ] One transient and one permanent failure are distinguishable.
- [ ] The runbook enables another person to diagnose and recover the demo.

## Next

Choose [L10 · PySpark DataFrames & Parquet](../10-pyspark-dataframes/README.md) for the separate Spark project, or L12 after L11 to deploy the flagship.

References and version cautions are in [`resources.md`](resources.md).
