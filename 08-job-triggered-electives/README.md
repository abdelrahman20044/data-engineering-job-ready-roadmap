# Module 08 — Job-Triggered Electives

## Why this matters

Regional postings sometimes cluster around dbt, Microsoft data services, Databricks, Kafka, BI, or legacy Hadoop ecosystems. These skills can improve a specific application, but none is universal enough to delay the core portfolio or active applications.

## Prerequisites

Modules 01–04 and an active application pipeline. Complete later core modules in parallel unless a high-priority role creates an immediate elective trigger.

## Outcome

You close one repeated target-job gap with small, inspectable evidence and can explain why the technology belongs in an architecture—without starting a second generic curriculum.

## Rule

This is not a final mandatory phase. Choose **one** elective only when:

1. it is repeated across at least three realistic active target roles, **or**
2. a high-priority opportunity explicitly requires it and the gap is learnable before interview, **or**
3. the flagship/Spark project has a real requirement that the tool solves.

An isolated posting does not reorder the roadmap. Update the Notion Roadmap Decision Log only for a material decision.

## Elective map

| Elective | Trigger | Minimum useful outcome | Do not do yet |
|---|---|---|---|
| dbt | Repeated analytics-engineering/warehouse transformation roles | Build tested models, sources, documentation, and incremental logic on an existing warehouse | Certifications, packages/macros depth |
| Azure / ADF / Fabric / Databricks | Several high-priority Egypt/Gulf roles repeat the same Microsoft stack | Translate the flagship architecture and implement one small pipeline/lab in the demanded service | Learn the entire Microsoft data platform |
| Kafka / streaming | Repeated target roles truly require streaming, not just “nice to have” | Explain broker/topic/partition/consumer group/offsets and build one small reliable producer-consumer pipeline | Complex event-driven platform, exactly-once marketing claims |
| BI exposure | Roles expect Power BI/Tableau collaboration | Build one thin dashboard on the warehouse and explain metric grain/definitions | Become a dashboard specialist |
| Hadoop/Hive refresher | Interview/role repeats the ecosystem | Explain HDFS/YARN/MapReduce/Hive roles and contrast them with Spark/cloud systems | Cluster administration or another Hadoop project |
| CI/CD | Project/application values automated checks | Run formatting/tests on pull requests and document release/deploy gate | Platform engineering depth |
| Terraform | Repeated cloud roles require IaC after a working manual deployment | Recreate the small AWS architecture reproducibly with safe state/secrets handling | Multi-environment enterprise modules |

## Curated starting points

### dbt

- **Learn:** [dbt Learn](https://learn.getdbt.com/) fundamentals relevant to models, tests, sources, documentation, and incremental models.
- **Reference:** [dbt documentation](https://docs.getdbt.com/).
- **Practice/apply:** model one layer of the existing flagship warehouse; do not create a third project.
- **Evidence:** lineage/docs screenshot, tests, model SQL, incremental rerun, and a written explanation of dbt's role vs Airflow.

### Microsoft data stack

- **Learn:** select the exact [Microsoft Learn](https://learn.microsoft.com/training/) path matching repeated job wording—ADF, Fabric, Azure Databricks, or Synapse. Do not take all four.
- **Practice/apply:** recreate one ingestion/transformation path with a tiny dataset and map each component to the flagship equivalent.
- **Evidence:** pipeline/configuration, run output, architecture comparison, and cost/cleanup note.

### Kafka

- **Learn:** [Apache Kafka documentation](https://kafka.apache.org/documentation/) for authoritative concepts; use [Confluent Developer tutorials](https://developer.confluent.io/tutorials/) for a guided lab.
- **Practice/apply:** producer → topic → consumer with keys, partitions, offsets, retries, and duplicate-awareness.
- **Evidence:** code, local Compose setup, failure/replay demonstration, and explanation of at-least-once implications.

### BI

- **Learn:** official Microsoft Learn Power BI content or Tableau training only for the tool named repeatedly in target roles.
- **Practice/apply:** connect to the flagship warehouse, create three decision-oriented metrics, and document their grain.
- **Evidence:** thin dashboard and metric definitions—not visual decoration.

### Hadoop/Hive refresher

- **Review:** existing notes plus [Apache Hadoop documentation](https://hadoop.apache.org/docs/current/) and [Apache Hive documentation](https://hive.apache.org/).
- **Practice:** draw the write/read execution path and compare MapReduce, Spark, and cloud object storage.
- **Evidence:** interview explanation. No new project by default.

## Interview check

For the selected elective, explain:

1. Which repeated market signal triggered it.
2. What problem the technology solves.
3. Where it fits in the existing architecture.
4. What trade-off/cost it introduces.
5. What you built that proves more than vocabulary.

## Done when

The specific target-job gap is closed with inspectable evidence. Stop there; return attention to applications, interviews, and strengthening existing projects.

## Next

Use the Notion Career OS to choose current applications and the next evidence gap. Do not automatically select another elective.
