# L08 Resources · Airflow Foundations

## Recommended path

1. Audited Airflow book sections for the mental model.
2. The current [TaskFlow tutorial](https://airflow.apache.org/docs/apache-airflow/stable/tutorial/taskflow.html) and [Docker quick start](https://airflow.apache.org/docs/apache-airflow/stable/howto/docker-compose/index.html) for first practice.
3. [Astronomer Airflow 101](https://academy.astronomer.io/path/airflow-101) only if a second structured explanation is useful; access may require an account.

## Arabic / Egyptian

No Arabic course is mandatory. Use a selected Arabic Airflow explanation only when it clarifies the scheduler/DAG mental model; verify examples against current Airflow 3 documentation.

## English alternatives

- [Data Engineering Zoomcamp](https://github.com/DataTalksClub/data-engineering-zoomcamp) selected workflow-orchestration module.
- [Astronomer Learn](https://www.astronomer.io/docs/learn/) for focused concepts and examples.

## Audited book sections

- *Data Pipelines with Apache Airflow*, 2e: Ch. 1 §§1.1–1.3; Ch. 2 §§2.2–2.6; Ch. 3 §§3.4–3.7; Ch. 5 §§5.2–5.4.
- Check older syntax and UI descriptions against current Airflow docs.

## Practice / labs

- Two-task hello-DAG only as a smoke test; immediately move to the flagship.
- Schedule a historical interval and verify the interval reaching each task.
- Break a connection and diagnose the task log.

## Reference

- [Apache Airflow documentation](https://airflow.apache.org/docs/apache-airflow/stable/)
- [TaskFlow tutorial](https://airflow.apache.org/docs/apache-airflow/stable/tutorial/taskflow.html)
- [Connections](https://airflow.apache.org/docs/apache-airflow/stable/howto/connection.html), [variables](https://airflow.apache.org/docs/apache-airflow/stable/core-concepts/variables.html) and [DAG runs/data intervals](https://airflow.apache.org/docs/apache-airflow/stable/core-concepts/dag-run.html)
- [Airflow best practices](https://airflow.apache.org/docs/apache-airflow/stable/best-practices.html)

## Later / skip

- L09 owns retries, backfills, recovery, sensors and monitoring.
- Later: asset-aware scheduling/datasets when a target job or project needs cross-pipeline dependencies.
- Skip custom operators/executors, Kubernetes deployment and provider sprawl.
