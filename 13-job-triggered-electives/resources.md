# L13 Resources · Job-Triggered Electives

Choose resources only after documenting the trigger. These are starting points, not assigned curriculum.

## dbt

- Primary starting point: [dbt Learn](https://learn.getdbt.com/)
- Reference: [dbt documentation](https://docs.getdbt.com/)
- Apply to the existing warehouse; do not create a second modeling curriculum.

## Microsoft data stack

- [Azure Data Factory introduction](https://learn.microsoft.com/en-us/azure/data-factory/introduction)
- [Microsoft Learn: Fabric](https://learn.microsoft.com/en-us/training/fabric/)
- [Azure Databricks: get started](https://learn.microsoft.com/en-us/azure/databricks/getting-started/)
- Select the one stack repeated by target roles; do not study all three by default.

## Managed warehouse

- [Snowflake tutorials](https://docs.snowflake.com/en/user-guide-getting-started)
- [BigQuery quickstarts](https://cloud.google.com/bigquery/docs/quickstarts)
- [Amazon Redshift getting started](https://docs.aws.amazon.com/redshift/latest/gsg/getting-started.html)
- Select only the vendor repeated by target jobs. Reuse the existing dimensional model and compare loading, partitioning/clustering or distribution, query plans and cost controls.

## Kafka / streaming

- Concepts first, only after a trigger: [*Streaming Systems*, Ch. 1–2](https://www.oreilly.com/library/view/streaming-systems/9781491983867/ch01.html) — bounded vs unbounded data, event time vs processing time, windows, triggers, and accumulation. Treat it as a conceptual reference, not a new book assignment.
- [Apache Kafka documentation](https://kafka.apache.org/documentation/)
- [Confluent Developer courses](https://developer.confluent.io/courses/)
- Minimum focus: records, brokers, topics, partitions, consumer groups, offsets and delivery semantics.

## Hadoop / Hive refresh

- [Apache Hadoop documentation](https://hadoop.apache.org/docs/current/)
- [Apache Hive documentation](https://hive.apache.org/)
- Refresh architecture and query behavior; skip MapReduce implementation depth unless explicitly required.

## BI exposure

- Use the official learning path for the tool named repeatedly in target roles.
- Build one decision-useful report over the flagship warehouse; avoid dashboard decoration.

## CI / infrastructure as code

- [GitHub Actions documentation](https://docs.github.com/en/actions)
- [Terraform tutorials](https://developer.hashicorp.com/terraform/tutorials) only if the trigger calls for IaC.

## Skip-for-now rule

No resource above is PRIMARY until its trigger is met. Record the job evidence, selected sections, exercise and project increment before studying.
