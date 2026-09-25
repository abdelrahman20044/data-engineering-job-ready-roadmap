# L11 · Spark Performance Essentials

| Tier | Time | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| 4 · Distributed Processing | 16 hours | ●●●●○ | L10 | Interview-ready Spark project |

## What you will learn

Read plans and UI evidence, reason about partitions and shuffles, and run one honest performance experiment. The goal is diagnosis—not memorizing tuning knobs or claiming cluster-scale results from a laptop.

## Topics and learning resources

| Order | Topic | Primary resource | Arabic / alternative | Action |
|---:|---|---|---|---|
| 1 | Jobs, stages and tasks | *Learning Spark*, 2e, Ch. 7 pp. 183–205 | Garage Education performance lessons | Connect lazy lineage to stage boundaries |
| 2 | Partitions and shuffles | [Spark performance tuning](https://spark.apache.org/docs/latest/sql-performance-tuning.html) | DE Zoomcamp Spark UI lesson | Identify narrow/wide operations and shuffle causes |
| 3 | File and partition sizing | Spark docs + project evidence | Tech Vault Parquet supplement | Compare `repartition` and `coalesce` deliberately |
| 4 | Join strategies | Spark tuning docs | — | Test a broadcastable lookup and inspect the plan |
| 5 | Caching and skew | Spark docs | — | Cache only reused expensive work; identify one skew symptom |
| 6 | Plans and UI | [`DataFrame.explain`](https://spark.apache.org/docs/latest/api/python/reference/pyspark.sql/api/pyspark.sql.DataFrame.explain.html) + Spark UI | — | Capture before/after evidence and state limitations |

## Practice

- Label narrow/wide transformations in the project.
- Run one controlled before/after experiment: repartitioning, broadcast join, caching or skew mitigation.
- Compare physical plans and relevant stage/task evidence.
- Record data size, machine constraints and why the result may not generalize.

## Project application

Complete the [Spark project](../projects/spark-project.md) with an experiment report, `explain()` output/Spark UI evidence and a README explaining the chosen optimization.

## Interview check

Explain jobs/stages/tasks, partition vs output partitioning, shuffle, broadcast joins, cache trade-offs, data skew, `repartition` vs `coalesce`, and how you would investigate a slow Spark job.

## Completion criteria

- [ ] One bottleneck hypothesis is tested with before/after evidence.
- [ ] Physical-plan/UI observations support the conclusion.
- [ ] Partition and join choices are defensible.
- [ ] Local-test limitations are explicit.

## Next

Continue to [L12 · Practical AWS for Data Engineering](../12-practical-aws/README.md) and deploy the flagship, not the Spark experiment by default.

Deeper references and later topics are in [`resources.md`](resources.md).
