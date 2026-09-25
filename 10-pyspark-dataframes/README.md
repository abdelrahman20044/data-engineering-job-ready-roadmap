# L10 · PySpark DataFrames & Parquet

| Tier | Time | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| 4 · Distributed Processing | 24 hours | ●●●○○ | L02, L04 | L11 |

## What you will learn

Build a separate PySpark pipeline using explicit schemas, DataFrame transformations and partitioned Parquet. Understand lazy evaluation well enough to avoid treating Spark as “pandas on a cluster.”

## Topics and learning resources

| Order | Topic | Primary resource | Arabic / alternative | Action |
|---:|---|---|---|---|
| 1 | Spark model and session | *Learning Spark*, 2e, Ch. 2 pp. 25–31 | Garage Education Spark chapter | Create a local session and explain driver/executor conceptually |
| 2 | DataFrames and schemas | Book Ch. 3 pp. 47–68 | [Spark SQL guide](https://spark.apache.org/docs/latest/sql-programming-guide.html) | Read raw data with an explicit schema and malformed-row policy |
| 3 | Transformations and actions | Book Ch. 3 pp. 76–82 | [DE Zoomcamp module 5](https://github.com/DataTalksClub/data-engineering-zoomcamp/tree/main/05-batch) | Demonstrate lazy execution and inspect a plan |
| 4 | Joins, aggregations, windows | [PySpark API](https://spark.apache.org/docs/latest/api/python/reference/pyspark.sql/index.html) | Garage Education | Build the project’s core transformations without Python UDFs |
| 5 | Parquet and partitioned data | Book Ch. 4 pp. 94–100; Ch. 5 pp. 144–155 | Tech Vault Parquet material | Write and read partitioned Parquet with a defensible key |

## Practice

- Define the schema and malformed-record policy before transformations.
- Use joins, aggregations and at least one window calculation.
- Compare a built-in expression with a Python UDF conceptually; use the built-in.
- Write partitioned Parquet and demonstrate partition pruning where possible.

## Project application

Start the [separate Spark project](../projects/spark-project.md) with mobility/clickstream-like data large enough to expose partitions and plans. Add transformation tests on small fixtures.

## Interview check

Explain DataFrame vs RDD at your level, schema inference risks, transformation vs action, lazy evaluation, built-ins vs UDFs, Parquet benefits and partition-column trade-offs.

## Completion criteria

- [ ] Explicit schema and malformed-row policy exist.
- [ ] Required joins, aggregations and window logic work.
- [ ] Output is partitioned Parquet with a written rationale.
- [ ] Transformations have small deterministic tests.

## Next

Continue to [L11 · Spark Performance Essentials](../11-spark-performance/README.md).

Arabic/English alternatives and exact book pages are in [`resources.md`](resources.md).
