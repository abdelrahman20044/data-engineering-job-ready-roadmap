# Module 06 — Spark & PySpark

## Why this matters

Spark/PySpark appeared in about 36% of early-career descriptions: valuable but not universal. This module demonstrates distributed-data reasoning on a separate dataset rather than forcing Spark into a small API pipeline.

## Prerequisites

Strong SQL, Python transformations, tests, and basic ETL reasoning from Modules 01–04. Airflow is complete but is not required inside this project.

## Outcome

You can build and test a PySpark batch pipeline using explicit schemas, DataFrames, joins/windows, partitioned Parquet, execution-plan reasoning, and one measured performance experiment.

## Topic path

### 1. Execution model and lazy evaluation

**Learn**

- DataTalksClub [Data Engineering Zoomcamp](https://github.com/DataTalksClub/data-engineering-zoomcamp): use only the current Batch Processing/Spark module and its homework.

**Read**

- *Learning Spark*, 2e: Ch. 2 pp. 25–31.

**Practice**

- Create a SparkSession; compare transformations vs actions; inspect a simple plan before and after an action.

**Apply**

- Initialize the separate Spark project with a documented local run and a dataset large enough to create multiple partitions.

### 2. DataFrames, explicit schemas, transformations, and windows

**Learn / reference**

- [Spark SQL, DataFrames and Datasets guide](https://spark.apache.org/docs/latest/sql-programming-guide.html).

**Read**

- *Learning Spark*, 2e: Ch. 3 pp. 47–68 and 76–82; Ch. 4 pp. 94–100.

**Practice**

- Read CSV/JSON with an explicit schema; handle malformed/null data; perform select/filter/derive/group/window operations without Python UDFs.

**Apply**

- Build clean bronze-to-silver transformations and one aggregate/windowed output for the mobility/clickstream dataset.

### 3. Joins, Parquet, and partition design

**Learn / reference**

- [Spark Parquet data source](https://spark.apache.org/docs/latest/sql-data-sources-parquet.html).

**Read**

- *Learning Spark*, 2e: Ch. 5 pp. 144–155.

**Practice**

- Join a fact-like event dataset to reference data; write Parquet partitioned by a query-relevant, bounded-cardinality key; compare file layout/counts.

**Apply**

- Produce partitioned Parquet and explain why the chosen partition key helps specific reads and where it can hurt.

### 4. Partitions, shuffles, caching, broadcast, and skew

**Learn / reference**

- [Spark performance tuning](https://spark.apache.org/docs/latest/sql-performance-tuning.html).

**Read**

- *Learning Spark*, 2e: Ch. 7 pp. 183–205.

**Practice**

- Use `explain()` and Spark UI to locate a shuffle. Compare one controlled before/after change: repartition/coalesce, broadcast join, or caching reused data.

**Apply**

- Commit the experiment method, input size, plan/UI evidence, timings, result, limitations, and whether the change is actually justified.

### 5. Testable Spark transformations

**Learn / practice**

- Reuse pytest fundamentals. Create a local Spark fixture and small deterministic input/output cases.

**Apply**

- Keep transformations as functions returning DataFrames; test schema and representative rows without asserting unordered output order accidentally.

## Module practice

- [ ] Zoomcamp Spark homework attempted independently.
- [ ] Explicit schema and malformed-row policy present.
- [ ] Join, aggregation, and window operation implemented.
- [ ] Parquet partition choice connected to a query pattern.
- [ ] One performance hypothesis tested with evidence.

## Build

Complete [`projects/spark-project.md`](../projects/spark-project.md). Do not add Kafka/Databricks/lakehouse tools unless an elective trigger exists.

## Interview check

Explain without notes:

1. Transformation vs action and lazy evaluation.
2. Narrow vs wide transformation.
3. What causes a shuffle.
4. Partitioning vs bucketing at a high level.
5. When broadcast joins or caching help—and when they hurt.
6. Why Parquet helps analytical workloads.
7. What your experiment proved and did not prove.

## Evidence

Pipeline code, tests, explicit schema, Parquet layout, plan/UI evidence, experiment write-up, and a clear README in the separate Spark project.

## Done when

The project runs from documented steps, tests pass, the plan/UI supports your reasoning, and you can discuss partitions/shuffles without memorized slogans.

## Next

[Module 07 — Practical AWS](../07-practical-aws/README.md)
