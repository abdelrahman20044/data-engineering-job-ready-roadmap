# PySpark Mobility / Clickstream Pipeline

## Why it is separate

Spark should process a dataset large and partitioned enough to make distributed reasoning visible. Forcing Spark into the flagship API workload would add a tool without a credible need.

## Outcome

Read raw files with an explicit schema, clean and transform them with DataFrames, join reference data, write partitioned Parquet, inspect execution plans/UI, and explain a small performance experiment.

## Required evidence

- [ ] Explicit input schema and malformed-row policy.
- [ ] DataFrame transformations, joins, aggregations, and at least one window calculation.
- [ ] Parquet output partitioned by a defensible key.
- [ ] Tests for transformation logic on small fixtures.
- [ ] Before/after experiment involving repartitioning, a broadcast join, caching, or skew handling.
- [ ] `explain()` output or Spark UI evidence connected to the written conclusion.
- [ ] README explaining lazy evaluation, narrow vs wide operations, shuffle boundaries, partition choice, and limits of the local experiment.

## Guardrails

- Prefer built-in Spark SQL/DataFrame functions over Python UDFs.
- Do not claim cluster-scale performance from a laptop run.
- Do not add Kafka, Delta Lake, or Databricks unless a target role or a clear project requirement triggers the elective.
- One measured experiment is more valuable than a list of tuning options.
