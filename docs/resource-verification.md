# Resource Verification

Last checked: **2026-09-26**.

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

## 13-level coverage audit · 2026-09-26

The audit preserved all levels and their order. It compared each level's learning outcomes, topic decomposition, practice, project increment, interview check and exit criteria against the existing 54-JD/42-early-career evidence base. It also inspected the corresponding level/resource pages in the reference roadmap before accepting individual resource leads.

| Level | Coverage correction | Resource correction |
|---|---|---|
| L01 · SQL | Added top-N-per-group and latest-record/deduplication as recurring analytical patterns; moved gaps-and-islands/sessionization later | Linked the exact Mahara course and exact PostgreSQL Exercises sections; added bounded SQL 50 alternative |
| L02 · PostgreSQL | Kept the scope at constraints, indexes, plans, estimates and transactions—not DBA tuning | Replaced vague Tech Vault labels with Use The Index, Luke and one named visual index explanation |
| L03 · Modeling | Added fact-table types, additivity, key choices, date/conformed/role-playing/degenerate dimensions | Linked the exact Garage DWH playlist, Tech Vault OLTP/OLAP lesson and Kimball technique PDF |
| L04 · Python | Added file/data interfaces and typed public boundaries without restarting programming basics | Linked the exact Mahara/Elzero gap-only options and targeted standard-library pages |
| L05 · ETL | Added rate-limit handling, batching, overlap-window/late-arrival behavior and visible drift policy | Removed the broad Seattle Data Guy recommendation; linked Requests timeouts and the discovered Garage playlist |
| L06 · Quality | Named six quality dimensions; added contract, database-boundary, atomicity and idempotency checks | Added pytest's good-practices page; kept quality frameworks later |
| L07 · Delivery | Added build context/layers/cache, volume vs bind mount, networking, health/readiness and explicit Compose behavior | Linked exact Pro Git chapters, Docker Python/best-practice/Compose pages and a bounded Arabic Docker course |
| L08 · Airflow | Added current TaskFlow, connection/variable handling, local Docker execution and CLI validation | Replaced broad Airflow/course references with stable official pages; retained Astronomer as optional structured support |
| L09 · Reliability | Added trigger rules/failure propagation alongside retries, idempotency, backfills, XComs and sensors | Linked the exact official trigger-rule, XCom, sensor and callback pages |
| L10 · PySpark | Added null/date handling and deterministic DataFrame/schema testing | Linked current Spark SQL, Parquet and Testing PySpark pages plus exact Arabic/Parquet alternatives |
| L11 · Spark performance | Made exchanges, small files, formatted plans and evidence limits explicit | Replaced broad “Spark docs” references with tuning, join-strategy, `explain` and UI pages |
| L12 · AWS | Defined one deployable default: S3 + EC2 Docker workload + private RDS PostgreSQL + CloudWatch, with a documented low-cost fallback | Replaced service-tour placeholders with direct S3, IAM role, VPC/RDS, EC2, CloudWatch and cost pages |
| L13 · Electives | Added a managed-warehouse trigger; preserved all elective gates | Replaced the stale/broad ADF training link and added vendor-specific warehouse starting points |

The only material time change is L12, from **24 to 30 hours**, because a secure network boundary, EC2/RDS deployment, centralized logs and teardown evidence cannot credibly fit the earlier placeholder scope. Other additions replace or clarify existing study time rather than expand the curriculum.

## Reference-roadmap audit

On **2026-09-25**, the actual tier, level and resource pages in [Yahia Sherif's Data Engineering Roadmap 2026](https://github.com/Yahiasherif002/Data-Engineering-Roadmap-2026) were inspected as an information-architecture and resource-discovery reference. Reused design ideas are limited to tier tables, explicit prerequisites/unlocks, dominant topic-to-resource maps, separate deep-resource pages and evidence-based completion gates.

Selected resource leads reused after fit-checking include Learn Git Branching, Pro Git, GitHub Skills, Modern SQL, Use The Index Luke, PostgreSQL Exercises, Kimball techniques, the exact Garage DWH/Spark playlists, focused Tech Vault OLTP/OLAP and Parquet explanations, Astronomer material, Data Engineering Zoomcamp's selected Spark exercises and official Spark/AWS references. Senior material such as Kubernetes, broad IaC, streaming platforms, governance stacks and deep database/Spark internals was not imported into the core path.

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

## Manual uncertainty and dynamic resources

- No Arabic resource was promoted to universal PRIMARY. The exact Mahara Transact-SQL page, Garage DWH playlist and Tech Vault OLTP/OLAP/Parquet pages were inspected. The Garage ETL and Spark playlist URLs were extracted from the live reference repository, but individual video titles/order still require a manual check before study; they remain alternatives, not dependencies.
- Astronomer Academy and AWS Skill Builder are dynamic and may require an account. Official Airflow/AWS service documentation is the durable fallback and owns current behavior.
- YouTube availability, subtitles and playlist order can change without a stable version. The level README still works if every optional video disappears.
- Microsoft renamed and repositioned parts of its data-integration stack. The old broad ADF training URL was replaced with the current ADF product introduction plus current Fabric training; only a job-triggered elective should choose between them.
- Automated bulk URL checking was not treated as proof of instructional quality. Primary technical references were resolved to official documentation; dynamic/sign-in resources remain explicitly optional.
