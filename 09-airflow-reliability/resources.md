# L09 Resources · Airflow Reliability

## Recommended path

Read the audited book sections just before each failure experiment, then verify current behavior in Airflow 3 documentation.

## Arabic / Egyptian

No complete Arabic reliability path was strong enough to displace the audited book plus current docs. Use Arabic explanations only for a specific concept.

## English alternatives

- [Astronomer Learn](https://www.astronomer.io/docs/learn/) tutorials on retries, scheduling, backfills, sensors and testing.
- [Data Engineering Zoomcamp](https://github.com/DataTalksClub/data-engineering-zoomcamp) for an additional orchestration example, not another full course.

## Audited book sections

- *Data Pipelines with Apache Airflow*, 2e: Ch. 6 §§6.1, 6.4–6.6; Ch. 10 §§10.1, 10.4; Ch. 12 §§12.1–12.3; Ch. 13 §§13.2–13.6.
- Treat all UI screenshots and version-specific syntax as potentially outdated; check current docs.

## Practice / labs

- Transient API failure → retry → success.
- Invalid schema → fail without repeated destructive work.
- Three-interval backfill with reconciled counts.
- Long-running task → timeout → actionable log.

## Reference

- [Airflow backfill](https://airflow.apache.org/docs/apache-airflow/stable/core-concepts/backfill.html)
- [Airflow best practices](https://airflow.apache.org/docs/apache-airflow/stable/best-practices.html)
- [Airflow UI](https://airflow.apache.org/docs/apache-airflow/stable/ui.html)

## Later / skip

- Later: remote executors, HA, custom providers, deferrable operators and Kubernetes.
- Skip SLA/alerting tool sprawl; one useful failure signal and runbook is enough now.
