# Curriculum Decisions

Internal rationale. The root README stays learner-facing and intentionally omits this detail.

## Evidence base

The current Notion market sample contains about 54 distinct Data Engineering job descriptions, including about 42 early-career descriptions. Approximate early-career frequencies used for prioritization are SQL 98%, Python 93%, ETL/ELT 86%, warehousing 74%, modeling 64%, cloud 62%, testing/data quality 45%, Spark 36%, and Airflow 29%.

This repository changes **how** the curriculum is executed, not those evidence-backed priorities.

## Why eight modules

Eight modules preserve one obvious path without fragmenting every tool into a separate course. SQL and modeling remain separate because each has its own diagnostic/build gate. Testing, data quality, Git, Docker, and Linux are combined into a professional-delivery module because their value is demonstrated together in a reproducible pipeline.

## Why Airflow precedes Spark

The flagship already creates a real batch pipeline that needs scheduling, retries, backfills, and monitoring. Airflow therefore extends existing work naturally. Spark uses a separate scale-appropriate dataset and comes later because it appears in a smaller share of early-career postings and is not required to make the first pipeline professional.

## Why AWS is the first cloud

Abdelrahman already has AWS Cloud Practitioner foundations. Practical AWS can therefore focus on deployment evidence rather than repeating generic cloud theory. Azure/ADF/Fabric/Databricks vocabulary remains an elective because it matters regionally, but switching the first cloud would add delay unless several target jobs repeatedly demand it.

## Why Kafka and advanced Hadoop are electives

Streaming and Hadoop ecosystem depth are specialized and often associated with larger-scale or more experienced roles. Existing Hadoop fundamentals are retained for interview context. Neither should delay SQL, Python ETL, testing, orchestration, or a deployable project.

## Project consolidation

Four overlapping small projects were consolidated into:

1. One flagship API-to-Warehouse platform that evolves through SQL/modeling, Python ETL, quality/delivery, Airflow, and AWS.
2. One separate Spark project where distributed execution, Parquet, partitions, shuffles, and performance experiments are authentic.

This reduces repeated scaffolding and makes progress visible as engineering maturity rather than tool accumulation.

## Resource decisions

- PostgreSQL Exercises and targeted interview problems replace a full beginner SQL course; the learner already has substantial SQL exposure.
- Kimball is assigned only where a modeling decision is made. Reading is never completion evidence.
- DataTalksClub material is used selectively for Docker/Spark/project patterns, not as a second full curriculum.
- Official documentation is a reference for current behavior. Structured courses/books are primary only where they improve first-pass learning.
- Great Expectations is optional after handwritten checks and pytest; adopting a framework before understanding the checks would hide fundamentals.
- No Arabic resource is included merely for symmetry. An Arabic alternative must cover the exact topic well enough to replace or clarify the primary resource.

## Re-evaluation rule

Do not reorder this path for isolated postings. Re-evaluate when roughly 15–20 meaningful new job descriptions accumulate after the existing baseline, or earlier only when a strong repeated shift appears.
