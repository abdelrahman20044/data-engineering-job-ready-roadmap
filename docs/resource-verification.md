# Resource Verification

Last checked: **2026-09-25**.

Selection standard: topic coverage, technical accuracy, practical usefulness, fit for a non-beginner programmer, current relevance, provider credibility, and ability to produce inspectable evidence.

## Primary resource set

| Resource | Used for | Why selected | Limitation / use rule |
|---|---|---|---|
| [PostgreSQL Exercises](https://pgexercises.com/) | SQL diagnostic and practice | Interactive PostgreSQL problems from joins through aggregates, windows, dates, and recursive queries | Not a modeling course; solve without opening answers first |
| [PostgreSQL current docs](https://www.postgresql.org/docs/current/) | SQL/PostgreSQL reference | Current authoritative behavior and `EXPLAIN` reference | Read targeted sections, not the manual cover to cover |
| *The Data Warehouse Toolkit*, 3e | Modeling | Deep, decision-oriented treatment of grain, facts, dimensions, and SCDs | Older product examples; use concepts, not tool-specific implementation details |
| [Kimball dimensional techniques](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/kimball-techniques/dimensional-modeling-techniques/) | Modeling reference | Concise authoritative summaries that map directly to project decisions | Supports the audited book; does not replace hands-on schema work |
| Python/Requests/packaging official docs | Python pipeline mechanics | Current APIs for HTTP behavior, logging, packaging, and configuration | Targeted lookup, not a Python-from-zero course |
| [pytest docs](https://docs.pytest.org/en/stable/getting-started.html) | Testing | Direct path to assertions, fixtures, parametrization, and failure output | Start small; avoid plugin/tool sprawl |
| [Docker docs](https://docs.docker.com/get-started/) | Reproducibility | Maintained hands-on Docker/Compose guidance | Apply immediately to the flagship |
| [Astronomer Airflow 101](https://academy.astronomer.io/path/airflow-101) | First-pass Airflow learning | Focused path from Airflow practitioners | Account/access may be required; pair with official Airflow 3 docs |
| [Apache Airflow 3 docs](https://airflow.apache.org/docs/apache-airflow/stable/) | Current Airflow behavior | Authoritative source for concepts, backfills, and current interfaces | Older book syntax must be checked here |
| [Data Engineering Zoomcamp](https://github.com/DataTalksClub/data-engineering-zoomcamp) selected Spark material | Guided Spark practice | Real dataset, exercises, Parquet, partitions, and Spark UI | Do not take the entire course inside this roadmap |
| [Apache Spark docs](https://spark.apache.org/docs/latest/) | Current PySpark/Spark behavior | Authoritative DataFrame, data source, and performance reference | Use examples selectively; not a linear course |
| AWS Skill Builder's Data Engineering on AWS learning plan | Guided AWS context | Official role-focused material and labs | Dynamic pages may require sign-in; use only relevant modules, not certification prep |
| AWS service docs | S3/IAM/secrets/logging | Current and authoritative security/operations guidance | Implement a small architecture; avoid broad service tours |

## Reference-roadmap audit

On **2026-09-25**, the actual tier, level and resource pages in [Yahia Sherif's Data Engineering Roadmap 2026](https://github.com/Yahiasherif002/Data-Engineering-Roadmap-2026) were inspected as an information-architecture and resource-discovery reference. Reused design ideas are limited to tier tables, explicit prerequisites/unlocks, dominant topic-to-resource maps, separate deep-resource pages and evidence-based completion gates.

Selected resource leads reused after fit-checking include Learn Git Branching, Pro Git, GitHub Skills, Modern SQL, Use The Index Luke, PostgreSQL Exercises, Kimball techniques, Garage Education/Tech Vault topic explanations, Astronomer material, Data Engineering Zoomcamp's selected Spark exercises, Databricks/Spark references and AWS official training. Senior material such as Kubernetes, broad IaC, streaming platforms, governance stacks and deep database/Spark internals was not imported into the core path.

## Audited books used just in time

Exact assignments are copied from the completed PDF audit, not guessed from online tables of contents.

| Book | Classification | Assigned now |
|---|---|---|
| *The Data Warehouse Toolkit*, 3e | PRIMARY for L03 | Ch. 1 pp. 7–22; Ch. 2 pp. 37–57; Ch. 3 pp. 70–79 and 98–104; Ch. 5 pp. 147–154 |
| *Building ETL Pipelines with Python* | SUPPLEMENTARY for L05–L06 | Ch. 4 pp. 47–52; Ch. 6 pp. 72–76; Ch. 13 pp. 169–181; Ch. 14 pp. 185–195 |
| *Fundamentals of Data Engineering* | REFERENCE | Ch. 2 pp. 33–48 and 59–68; Ch. 7 pp. 235–247 and 250–257; Ch. 8 pp. 309–323 |
| *Data Pipelines with Apache Airflow*, 2e | PRIMARY for L08–L09 | Ch. 1 §§1.1–1.3; Ch. 2 §§2.2–2.6; Ch. 3 §§3.4–3.7; Ch. 5 §§5.2–5.4; Ch. 6 §§6.1, 6.4–6.6; Ch. 10 §§10.1, 10.4; Ch. 12 §§12.1–12.3; Ch. 13 §§13.2–13.6 |
| *Learning Spark*, 2e | SUPPLEMENTARY for L10–L11 | Ch. 2 pp. 25–31; Ch. 3 pp. 47–68 and 76–82; Ch. 4 pp. 94–100; Ch. 5 pp. 144–155; Ch. 7 pp. 183–205 |

## Resources intentionally demoted

- Long beginner SQL and Python video courses: use only for a diagnosed gap; they duplicate existing foundations.
- Tutorial warehouse repositories: architecture examples only. Do not clone a finished project and call it evidence.
- Complete Data Engineering Zoomcamp: selected labs only; otherwise it becomes a competing curriculum.
- Broad AWS certification material: Cloud Practitioner is already complete; project deployment is the objective.
- Great Expectations: optional reference after explicit data checks and pytest are understood.

## Unverified or intentionally omitted

No Arabic resource was promoted to universal PRIMARY. Garage Education, Tech Vault and Kube-ops topic material is listed as an alternative where the audited reference supplied a close topic match; stable lesson-level URLs and full currency were not independently established. Confirm the precise lesson before using it. The curriculum never fills an Arabic slot for symmetry.

AWS Skill Builder pages are dynamic and may require authentication. The official learning plan was discoverable, but stable deep links can change. AWS service documentation remains the durable fallback.
