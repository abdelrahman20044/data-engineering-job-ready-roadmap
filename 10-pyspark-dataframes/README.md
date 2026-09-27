# L10 · PySpark DataFrames & Parquet

| Tier | Time | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| 4 · Distributed Processing | 24 hours | ●●●○○ | L02, L04 | L11 |

## What you will learn

Build a separate PySpark pipeline using explicit schemas, DataFrame transformations and partitioned Parquet. Understand lazy evaluation well enough to avoid treating Spark as “pandas on a cluster.”

## Diagnostic gate · 60 minutes

With documentation closed, create a local Spark session, read a small file with an explicit schema, apply a filter and derived column, join reference data, calculate one window result, and write partitioned Parquet. Before the final action, predict which operations are lazy and where a shuffle may occur; then inspect the plan.

- If the pipeline works and your plan explanation is accurate, shorten the foundation reading and move to testing plus the project workload.
- If you depend on schema inference, Python UDFs, or trial-and-error joins, study only the matching topics below before retrying.

## Topics and learning resources

| Order | Topic | Primary resource | Arabic / alternative | Action |
|---:|---|---|---|---|
| 1 | Spark model and session | *Learning Spark*, 2e, Ch. 2 pp. 25–31 | [Garage Education Spark/PySpark](https://www.youtube.com/playlist?list=PLxNoJq6k39G9lTU9A65HwC0uWD-XkqqOi) | Create a local session and explain driver/executor conceptually |
| 2 | DataFrames and schemas | Book Ch. 3 pp. 47–68 | [Spark SQL getting started](https://spark.apache.org/docs/latest/sql-getting-started.html) | Read raw data with an explicit schema and malformed-row policy |
| 3 | Transformations and actions | Book Ch. 3 pp. 76–82 | [DE Zoomcamp module 5](https://github.com/DataTalksClub/data-engineering-zoomcamp/tree/main/05-batch) | Demonstrate lazy execution and inspect a plan |
| 4 | Joins, aggregations, windows | [PySpark SQL API](https://spark.apache.org/docs/latest/api/python/reference/pyspark.sql/index.html) | [Garage Education Spark/PySpark](https://www.youtube.com/playlist?list=PLxNoJq6k39G9lTU9A65HwC0uWD-XkqqOi) | Build core transformations with null/date handling and built-ins instead of Python UDFs |
| 5 | Parquet and partitioned data | Book Ch. 4 pp. 94–100; Ch. 5 pp. 144–155 + [Parquet data source](https://spark.apache.org/docs/latest/sql-data-sources-parquet.html) | [Tech Vault: Parquet](https://www.youtube.com/watch?v=MLmrz_UfJ0Q) | Write/read partitioned Parquet with a defensible key and file layout |
| 6 | DataFrame testing | [Testing PySpark](https://spark.apache.org/docs/latest/api/python/getting_started/testing_pyspark.html) | — | Assert transformed rows and schema on tiny deterministic fixtures |

## Practice

- Define the schema and malformed-record policy before transformations.
- Use joins, aggregations and at least one window calculation.
- Compare a built-in expression with a Python UDF conceptually; use the built-in.
- Write partitioned Parquet and demonstrate partition pruning where possible.

## Project application

Start the [separate Spark project](../projects/spark-project.md) with mobility/clickstream-like data large enough to expose partitions and plans. Add transformation tests on small fixtures.

## Interview check

Explain DataFrame vs RDD at your level, schema inference risks, transformation vs action, lazy evaluation, built-ins vs UDFs, deterministic DataFrame testing, Parquet benefits and partition-column trade-offs.

## Completion criteria

- [ ] Explicit schema and malformed-row policy exist.
- [ ] Required joins, aggregations and window logic work.
- [ ] Output is partitioned Parquet with a written rationale.
- [ ] Transformations have small deterministic tests.

## Next

Continue to [L11 · Spark Performance Essentials](../11-spark-performance/README.md).

Arabic/English alternatives and exact book pages are in [`resources.md`](resources.md).
