# Data Engineering Book Guide

This guide turns the supplied library inventory into a **just-in-time reference**, not a second curriculum. The inventory contains 69 file entries and **68 distinct titles**: *Fundamentals of Data Engineering* appears twice under different filenames.

The active roadmap remains the authority. A book is assigned only where it can shorten the path from understanding to evidence:

> LEARN → PRACTISE → BUILD → DEBUG → EXPLAIN → PROVE → APPLY

## How to use this guide

- **READ NOW** — cover-to-cover reading is worth delaying the next practical step. There are deliberately no books in this class.
- **READ SELECTED CHAPTERS** — the named sections are part of the active path.
- **READ LATER** — valuable after the first-role core or when a level explicitly unlocks it.
- **REFERENCE ONLY** — consult for a concrete question; do not read linearly.
- **ALTERNATIVE** — overlaps a stronger assigned resource; use only if the assigned one does not work for you.
- **SKIP FOR CURRENT TARGET** — too specialized, vendor-specific, dated, or advanced for the first-role objective.

Exact page/chapter assignments below are made only for the five PDFs already inspected in the targeted Pass 2 audit. For the remaining inventory, mappings are at book level unless a public publisher table of contents was verified. Edition years marked `~` are publisher/catalog years for the inventory edition; they are useful for age checks, not bibliographic guarantees.

## Decision summary

| Decision | Meaning for this roadmap |
|---|---|
| READ NOW | **0** — no cover-to-cover requirement should block project work |
| READ SELECTED CHAPTERS | **5** — Kimball, Python ETL, Fundamentals of DE, Airflow, and Learning Spark |
| READ LATER | **15** — deeper architecture, performance, governance, and stack material after core evidence exists |
| REFERENCE ONLY | **21** — use to debug or answer a focused design question |
| ALTERNATIVE | **16** — a substitute, not an additional assignment |
| SKIP FOR CURRENT TARGET | **11** — preserve in the library, but do not schedule now |

## Best choices by learning objective

| Objective | Best choice for this roadmap | Why | Roadmap |
|---|---|---|---|
| DE lifecycle vocabulary | *Fundamentals of Data Engineering* | Vendor-neutral lifecycle and trade-off framing | L05–L06; architecture later |
| Relational design | *Grokking Relational Database Design* as reference | Focused and approachable; project schema supplies the practice | L02–L03 |
| Database internals | *Database System Concepts*, selected reference | Authoritative depth without forcing a 1,300-page detour | L02; later L11 |
| SQL practice | Exercises first; *Practical SQL* only as an alternative | The current need is independent problem-solving, not another beginner sequence | L01 |
| Dimensional modeling | *The Data Warehouse Toolkit*, selected chapters | Canonical grain/fact/dimension/SCD treatment | L03 |
| Python ETL | *Building ETL Pipelines with Python*, selected chapters | Directly maps to ingestion, idempotency, testing, and project code | L05–L06 |
| Orchestration | *Data Pipelines with Apache Airflow*, selected chapters | Best balance of concepts, implementation, testing, and operations | L08–L09 |
| Spark | *Learning Spark, 2nd ed.*, selected chapters | DataFrame-first mental model and practical optimization foundation | L10–L11 |
| Spark deep dive | *High Performance Spark, 2nd ed.* | Current performance treatment; unnecessary before a working Spark project | Later L11 |
| AWS implementation | *Data Engineering with AWS, 2nd ed.* as reference | Practical service patterns; official docs remain version truth | L12 |
| Kafka | *Kafka: The Definitive Guide, 2nd ed.* | Strongest broad reference if a job trigger appears | L13 |
| Lakehouse/table formats | *Apache Iceberg: The Definitive Guide* | Best format-level reference; not part of core | L13 |
| Snowflake | *Snowflake: The Definitive Guide* | Broad reference; choose a narrower project book only after a Snowflake trigger | L13 |
| dbt | *Analytics Engineering with SQL and dbt* | Best fit for modeling/testing workflow; official dbt Learn remains implementation primary | L13 |

## Key book-vs-book decisions

### SQL and relational databases

| Books | Relationship | Decision |
|---|---|---|
| *Practical SQL* vs *Grokking Relational Database Design* | Complementary: querying/analysis vs schema design | Do SQL exercises first. Use *Practical SQL* only for a query gap; use *Grokking* for a schema-design question. |
| *Grokking Relational Database Design* vs *Database Design and Modeling with PostgreSQL and MySQL* | True alternatives for practical relational design | Prefer *Grokking* for clarity and scope. Use the PostgreSQL/MySQL book only when vendor-specific implementation matters. |
| Both practical design books vs *Database System Concepts* | Practical introduction vs academic depth | Keep the textbook as reference for indexes, query processing, transactions, and recovery; do not read it sequentially. |
| *Oracle PL/SQL by Example* vs the roadmap's PostgreSQL path | Different vendor and learning goal | Skip unless a target role explicitly requires Oracle/PL/SQL. |

### Warehousing and modeling

| Books | Relationship | Decision |
|---|---|---|
| *The Data Warehouse Toolkit* vs *Architecting a Modern Data Warehouse for Large Enterprises* | Dimensional modeling foundation vs enterprise architecture | Kimball now, selected chapters. Enterprise architecture later, after one implemented warehouse. |
| *The Data Warehouse Toolkit* vs *Data Modeling with Snowflake* | Vendor-neutral foundation vs Snowflake implementation | Kimball first. Snowflake book only after a job-triggered Snowflake elective. |

### Python, ingestion, and ETL

| Books | Relationship | Decision |
|---|---|---|
| *Building ETL Pipelines with Python* vs *Data Engineering with Python* | Modern focused ETL project vs broad older tool tour | Assigned ETL book wins. The broader book is an alternative, not a second course. |
| *Building ETL Pipelines with Python* vs *Data Ingestion with Python Cookbook* | End-to-end ETL vs ingestion recipes/monitoring | Complementary only when an ingestion edge case appears; consult the cookbook, do not read both. |
| *Python for Data Analysis* vs *Python Polars: The Definitive Guide* | pandas analysis reference vs newer high-performance DataFrame specialist | Neither replaces engineering-focused Python. pandas is reference; Polars is job/project-triggered. |
| *Understanding ETL* vs the assigned ETL book | Conceptual overview vs implementation | Skip the overview unless you need a short reset; the roadmap already supplies both concepts and code. |

### Airflow

| Books | Relationship | Decision |
|---|---|---|
| *Data Pipelines with Apache Airflow, 2nd ed.* vs *Practical Guide to Apache Airflow 3* | Structured concepts/production patterns vs current-version implementation | Use selected chapters from the former; use the Airflow 3 book and official docs to translate APIs/version changes. |
| *Apache Airflow Best Practices* vs the two above | Additional operations advice | Reference later; it should not create a third Airflow learning path. |

### Spark and distributed processing

| Books | Relationship | Decision |
|---|---|---|
| *Learning Spark, 2nd ed.* vs *Spark in Action, 2nd ed.* | Concise DataFrame-first foundation vs longer multi-language project treatment | *Learning Spark* wins for L10. *Spark in Action* is an alternative. |
| *Learning Spark* vs *High Performance Spark, 2nd ed.* | Foundation vs optimization deep dive | Complementary and sequential: selected *Learning Spark* first; performance book later. |
| *Data Algorithms with Spark* vs both | Algorithm-recipe specialist | Reference only when solving a matching distributed algorithm; not entry-level curriculum. |
| *Hadoop: The Definitive Guide, 4th ed.* vs current Spark/object-store path | Legacy ecosystem implementation vs still-useful distributed concepts | Retain as historical/architecture reference; do not practise MapReduce APIs unless a job requires them. |

### Kafka and streaming

| Books | Relationship | Decision |
|---|---|---|
| *Kafka: The Definitive Guide* vs *Kafka in Action* | Broad authoritative reference vs guided implementation | Prefer the definitive guide as reference; use *Kafka in Action* if a trigger calls for a hands-on sequence. |
| *Kafka Connect* vs *Mastering Kafka Streams and ksqlDB* | Integration specialist vs processing specialist | Complementary but both job-triggered; select one according to the role. |
| Kafka books vs *Stream Processing with Apache Flink* | Platform-specific implementations of streaming concepts | Learn time/state/delivery semantics first; choose one implementation only after evidence demands it. |

### Lakehouse and vendor stacks

| Books | Relationship | Decision |
|---|---|---|
| *Apache Iceberg: The Definitive Guide* vs *Architecting an Apache Iceberg Lakehouse* | Format reference vs platform architecture | Use the definitive guide as reference; architecture book later if implementing Iceberg. |
| *Delta Lake: The Definitive Guide* vs *Delta Lake Up and Running* | Deep reference vs faster practical entry | Choose one after a Delta/Databricks trigger; start with *Up and Running* if speed matters. |
| *Engineering Lakehouses with Open Table Formats* vs format-specific books | Comparative breadth vs format depth | Use for format selection, not in addition to every Iceberg/Delta book. |
| Snowflake books | Heavy overlap across SQL, modeling, platform, DataOps, and advanced workloads | Start with official tutorials. Select **one** book aligned to the role; never read the cluster sequentially. |
| dbt books | Overlap across fundamentals and analytics-engineering workflow | Use dbt Learn first. Choose *Analytics Engineering with SQL and dbt* for concepts or *Unlocking dbt* for implementation—not both. |

## Complete categorized inventory

### 1. General data engineering and architecture

| Rank/level | Book | Edition/year | Best use | Roadmap | Decision | Reason |
|---|---|---|---|---|---|---|
| 1 · Foundational | *Fundamentals of Data Engineering* — Reis & Housley | 1e, 2022 | Lifecycle and trade-offs | L05–L06; later architecture | **READ SELECTED CHAPTERS** | Ch. 7 pp. 235–247, 250–257; Ch. 8 pp. 309–323 as reference. Duplicate file counted once. |
| 2 · Advanced | *Designing Data-Intensive Applications* — Kleppmann & Riccomini | 2e, 2026 | Reliability, storage, distributed systems | Later L09/L11/L13 | **READ LATER** | Excellent but intermediate–advanced; use after project failures make the abstractions concrete. |
| 3 · Reference | *97 Things Every Data Engineer Should Know* — Macey | 2021 | Short practitioner perspectives | Cross-level | **REFERENCE ONLY** | Useful breadth; essays do not form a coherent learning sequence. |
| 4 · Intermediate | *Data Engineering Design Patterns* — Konieczny | ~2024 | Solution patterns | L05/L09 later | **READ LATER** | Valuable after implementing one pipeline; premature patterns otherwise become vocabulary. |
| 5 · Intermediate | *Data Engineering Best Practices* — Schiller & Larochelle | ~2024 | Cloud-era trade-offs and cost | L12/later | **READ LATER** | Production context matters more after the first deployed pipeline. |
| 6 · Advanced | *Deciphering Data Architectures* — Serra | 2024 | Warehouse/lakehouse/mesh/fabric comparison | L13 | **REFERENCE ONLY** | Useful when choosing architecture; too broad for the active build. |
| 7 · Specialist | *Practical Data Engineering with Apache Projects* — Danushka | ~2024 | Cross-tool Apache project recipes | L13 | **SKIP FOR CURRENT TARGET** | Spark, Iceberg, Kafka, and Flink together would widen scope before evidence demands it. |
| 8 · Foundational | *Data Engineering for Beginners* — Nwokwu | Year not verified | General introduction | — | **ALTERNATIVE** | Redundant with the more rigorous existing roadmap and FoDE selections. |

### 2. SQL, relational databases, internals, and performance

| Rank/level | Book | Edition/year | Best use | Roadmap | Decision | Reason |
|---|---|---|---|---|---|---|
| 1 · Foundational | *Grokking Relational Database Design* — Hao & Tsikerdekis | 2025 | Relational design decisions | L02–L03 | **REFERENCE ONLY** | Clear, modern design aid; project schema and exercises remain primary. |
| 2 · Reference | *Database System Concepts* — Silberschatz et al. | 7e, 2019 | Indexes, optimization, transactions, recovery | L02; later L09/L11 | **REFERENCE ONLY** | Authoritative but far too large for sequential reading. |
| 3 · Foundational | *Practical SQL* — DeBarros | 2e, 2022 | PostgreSQL query examples and data analysis | L01 | **ALTERNATIVE** | Good book, but independent graded SQL practice better targets the current gap. |
| 4 · Intermediate | *Database Design and Modeling with PostgreSQL and MySQL* — Tezuysal & Ahmed | ~2024 | Vendor-specific implementation | L02–L03 | **ALTERNATIVE** | Use only if *Grokking* lacks an implementation detail. |
| 5 · Specialist | *Fuzzy Data Matching with SQL* — Lehmer | ~2025 | Entity matching and data-quality query patterns | L06/L13 | **REFERENCE ONLY** | Valuable for a matching/deduplication use case, not a core requirement. |
| 6 · Specialist | *Oracle PL/SQL by Example* — Rosenzweig & Rakhimov | 6e, ~2023 | Oracle procedural SQL | L13 | **SKIP FOR CURRENT TARGET** | PostgreSQL and portable SQL have higher current value; activate only for an Oracle-heavy job. |

### 3. Data warehousing and dimensional modeling

| Rank/level | Book | Edition/year | Best use | Roadmap | Decision | Reason |
|---|---|---|---|---|---|---|
| 1 · Core | *The Data Warehouse Toolkit* — Kimball & Ross | 3e, 2013 | Grain, facts, dimensions, SCDs | L03 | **READ SELECTED CHAPTERS** | Now: Ch. 1 pp. 7–22; Ch. 2 pp. 37–57; Ch. 3 pp. 70–79 and 98–104; Ch. 5 pp. 147–154. Later: Ch. 4 pp. 111–122; Ch. 6 pp. 167–199. |
| 2 · Advanced | *Architecting a Modern Data Warehouse for Large Enterprises* — Kumar et al. | ~2021 | Enterprise/multi-cloud architecture | L13/later | **READ LATER** | Architecture breadth is useful only after one small warehouse is real. |

### 4. Python, ingestion, ETL, and DataFrames

| Rank/level | Book | Edition/year | Best use | Roadmap | Decision | Reason |
|---|---|---|---|---|---|---|
| 1 · Core | *Building ETL Pipelines with Python* — Pandey & Schoof | 2023 | ETL implementation, tests, quality | L05–L06 | **READ SELECTED CHAPTERS** | L05: Ch. 4 pp. 47–52; Ch. 6 pp. 72–76. L06: Ch. 13 pp. 169–181; Ch. 14 pp. 185–195. |
| 2 · Intermediate | *Data Ingestion with Python Cookbook* — Esppenchutz | ~2023 | Ingestion, monitoring, error recipes | L05/L06 | **REFERENCE ONLY** | Consult for a concrete source/error pattern; avoid duplicating the assigned ETL path. |
| 3 · Foundational | *Data Engineering with Python* — Crickard | ~2020 | Broad Python pipeline tour | L04–L05 | **ALTERNATIVE** | Broader but older and less focused than the assigned resource/project. |
| 4 · Reference | *Python for Data Analysis* — McKinney | 3e, 2022 | pandas, file formats, data manipulation | L04–L05 | **REFERENCE ONLY** | Strong pandas reference; not a pipeline-engineering curriculum. |
| 5 · Specialist | *Python Polars: The Definitive Guide* — Janssens & Nieuwdorp | 2024 | Polars expressions and performance | L13 | **SKIP FOR CURRENT TARGET** | Learn only if a project/job selects Polars; pandas/PySpark coverage is currently stronger. |
| 6 · Foundational | *Understanding ETL* — Palmer | Year not verified | ETL overview | L05 | **ALTERNATIVE** | Redundant with FoDE, the assigned ETL chapters, and hands-on project work. |

### 5. Testing, governance, and observability

| Rank/level | Book | Edition/year | Best use | Roadmap | Decision | Reason |
|---|---|---|---|---|---|---|
| 1 · Intermediate | *Fundamentals of Data Observability* — Petrella | ~2024 | Reliability signals and incident thinking | L09/later | **READ LATER** | Useful once the flagship has measurable failures, logs, and checks. |
| 2 · Advanced | *Data Governance: The Definitive Guide* — Eryurek et al. | 2021 | Governance, metadata, privacy, stewardship | L13/later | **REFERENCE ONLY** | Important organizational context but not a pre-employment implementation priority. |

### 6. Airflow and orchestration

| Rank/level | Book | Edition/year | Best use | Roadmap | Decision | Reason |
|---|---|---|---|---|---|---|
| 1 · Core | *Data Pipelines with Apache Airflow: Orchestration for Data and AI* — de Ruiter et al. | 2e, ~2025–26 | DAGs, scheduling, testing, production patterns | L08–L09 | **READ SELECTED CHAPTERS** | L08: Ch. 1 §§1.1–1.3; Ch. 2 §§2.2–2.6; Ch. 3 §§3.4–3.7; Ch. 5 §§5.2–5.4. L09: Ch. 6 §§6.1, 6.4–6.6; Ch. 10 §§10.1, 10.4; Ch. 12 §§12.1–12.3; Ch. 13 §§13.2–13.6. |
| 2 · Current-version reference | *Practical Guide to Apache Airflow 3* — Fingerlin | ~2025–26 | Airflow 3 implementation | L08–L09 | **REFERENCE ONLY** | Use to translate version-specific APIs; official Airflow docs remain version truth. |
| 3 · Intermediate | *Apache Airflow Best Practices* — Intorf, Storey et al. | Year not verified | Operational practices | L09 | **READ LATER** | Additional depth after the assigned reliability work, not another first pass. |

### 7. Spark, distributed processing, Beam, and Hadoop

| Rank/level | Book | Edition/year | Best use | Roadmap | Decision | Reason |
|---|---|---|---|---|---|---|
| 1 · Core | *Learning Spark* — Damji et al. | 2e, 2020 | Structured APIs, DataFrames, Spark SQL, tuning | L10–L11 | **READ SELECTED CHAPTERS** | L10: Ch. 2 pp. 25–31; Ch. 3 pp. 47–68, 76–82; Ch. 4 pp. 94–100; Ch. 5 pp. 144–155. L11: Ch. 7 pp. 183–205. Verify APIs against current Spark docs. |
| 2 · Advanced | *High Performance Spark* — Karau, Polak & Warren | 2e, ~2026 | Current optimization deep dive | Later L11 | **READ LATER** | Best next book after the project produces real plans, shuffles, skew, and bottlenecks. |
| 3 · Intermediate | *Spark in Action* — Perrin | 2e, 2020 | Guided multi-language Spark projects | L10 | **ALTERNATIVE** | Longer than needed; use only if *Learning Spark* is too compressed. |
| 4 · Specialist | *Data Algorithms with Spark* — Parsian | ~2023 | Distributed algorithm recipes | L11/later | **REFERENCE ONLY** | Solve a matching problem; do not read as a course. |
| 5 · Specialist | *Building Big Data Pipelines with Apache Beam* — Lukavský | ~2022 | Unified batch/stream model | L13 | **SKIP FOR CURRENT TARGET** | Beam demand does not justify another processing model now. |
| 6 · Specialist | *Data Engineering with Scala and Spark* — Tome et al. | ~2022 | JVM/Scala Spark pipelines | L13 | **SKIP FOR CURRENT TARGET** | PySpark is the evidence-backed first interface; use only for a Scala job. |
| 7 · Specialist | *Functional Programming in Scala* — Pilquist et al. | 2e, 2023 | FP theory and Scala | L13/later | **SKIP FOR CURRENT TARGET** | High-quality but indirect for a Python-first junior DE target. |
| 8 · Historical/reference | *Hadoop: The Definitive Guide* — White | 4e, 2015 | HDFS/YARN/MapReduce architecture | L13 | **REFERENCE ONLY** | Preserve conceptual chapters; implementation APIs and operational details are dated. |
| 9 · Intermediate | *Data Engineering with Apache Spark, Delta Lake, and Lakehouse* — Kukreja | ~2021 | Spark plus Delta project | L13 | **ALTERNATIVE** | Use only after a Delta/Databricks trigger; it overlaps L10–L11 and the Delta books. |

### 8. Kafka and stream processing

| Rank/level | Book | Edition/year | Best use | Roadmap | Decision | Reason |
|---|---|---|---|---|---|---|
| 1 · Reference | *Kafka: The Definitive Guide* — Shapira et al. | 2e, 2022 | Producers, consumers, internals, operations | L13 | **REFERENCE ONLY** | Best broad Kafka reference if repeated job demand activates streaming. |
| 2 · Intermediate | *Kafka in Action* — Scott, Gamov & Klein | 2022 | Guided practical Kafka | L13 | **ALTERNATIVE** | Choose instead of—not after—the definitive guide when a hands-on path is preferred. |
| 3 · Specialist | *Kafka Connect* — Maison & Stanley | ~2022 | Connector pipelines and operations | L13 | **READ LATER** | Activate only for Connect-heavy integration roles. |
| 4 · Specialist | *Mastering Kafka Streams and ksqlDB* — Seymour | 2021 | Stream processing applications | L13 | **READ LATER** | Different goal from Kafka operations; only for a streams/ksqlDB role. |
| 5 · Advanced | *Kafka for Architects* — Gorshkova | ~2023 | Event-driven architecture | L13/later | **READ LATER** | Architecture depth should follow implementation experience. |
| 6 · Specialist/caution | *Stream Processing with Apache Flink* — Hueske & Kalavri | 2019 | Time, state, delivery semantics; older Flink APIs | L13 | **REFERENCE ONLY** | Ch. 1–3 concepts remain useful; implementation examples target an older Flink generation. |

### 9. Cloud platforms

| Rank/level | Book | Edition/year | Best use | Roadmap | Decision | Reason |
|---|---|---|---|---|---|---|
| 1 · Practical AWS | *Data Engineering with AWS* — Eagar | 2e, ~2024 | AWS pipeline implementation patterns | L12 | **REFERENCE ONLY** | Consult by service/problem; build from current AWS docs rather than read cover to cover. |
| 2 · Certification | *AWS Certified Data Engineer Associate Study Guide* — Mishra et al. | ~2024 | Exam coverage | L13/later | **READ LATER** | Certification is optional and must not replace deployed evidence. |
| 3 · Practical Azure | *Azure Data Engineering Cookbook* — Venkatesan & Osama | ~2022 | Recipe-based Azure implementation | L13 | **REFERENCE ONLY** | Use only after repeated Azure/ADF/Fabric demand. Verify renamed/retired services in Microsoft Learn. |
| 4 · Azure architecture | *Modern Data Architecture on Azure* — Lad | ~2022 | Azure solution design | L13/later | **READ LATER** | Architecture scope exceeds the first-role core. |
| 5 · Azure certification | *Azure Data Engineer Associate Certification Guide* | 2e, ~2022 | DP-203 preparation | L13 | **SKIP FOR CURRENT TARGET** | DP-203 was retired; use current Microsoft role-based material when Azure is triggered. |
| 6 · Azure certification | *MCA Azure Data Engineer Study Guide: DP-203* — Perkins | ~2021 | DP-203 preparation | L13 | **SKIP FOR CURRENT TARGET** | Retired-exam study guide; individual concepts may survive but the path is stale. |
| 7 · Azure fundamentals | *Microsoft Certified Azure Data Fundamentals: DP-900* — Switzer | ~2022 | Broad Azure data vocabulary | L13 | **ALTERNATIVE** | Too broad for implementation; use current Microsoft Learn if a role asks for Azure basics. |
| 8 · GCP | *Data Engineering with Google Cloud Platform* — Wijaya | ~2022 | GCP pipeline implementation | L13 | **ALTERNATIVE** | Choose only if target jobs repeatedly name GCP. Official docs remain version truth. |

### 10. Lakehouse, Databricks, and open table formats

| Rank/level | Book | Edition/year | Best use | Roadmap | Decision | Reason |
|---|---|---|---|---|---|---|
| 1 · Reference | *Apache Iceberg: The Definitive Guide* — Shiran, Hughes & Merced | 2024 | Iceberg architecture and operations | L13 | **REFERENCE ONLY** | Strong current format reference; not a core prerequisite. |
| 2 · Intermediate | *Delta Lake: The Definitive Guide* — Lee et al. | 2024 | Delta transaction log, operations, architecture | L13 | **REFERENCE ONLY** | Best deep Delta reference after a Databricks/Delta trigger. |
| 3 · Intermediate | *Delta Lake: Up and Running* — Haelen & Davis | ~2024 | Faster practical Delta entry | L13 | **ALTERNATIVE** | Prefer for rapid implementation; do not also read the definitive guide linearly. |
| 4 · Comparative | *Engineering Lakehouses with Open Table Formats* — Mazumdar & Govindarajan | ~2025 | Iceberg/Hudi/Delta comparison | L13/later | **READ LATER** | Useful when choosing formats, not before a lakehouse requirement exists. |
| 5 · Architecture | *Architecting an Apache Iceberg Lakehouse* — Merced | ~2024 | End-to-end Iceberg platform choices | L13/later | **READ LATER** | Complements the definitive guide only for an actual Iceberg design. |
| 6 · Architecture | *Practical Lakehouse Architecture* — Thalpati | ~2024 | Broad platform architecture | L13/later | **ALTERNATIVE** | Broad and overlapping; choose only if its platform mix matches the target role. |
| 7 · Databricks implementation | *Data Engineering with Databricks Cookbook* — Chadha | ~2023 | Databricks recipes | L13 | **REFERENCE ONLY** | Job-triggered and best used recipe-by-recipe. |
| 8 · Databricks application | *Building Modern Data Applications Using Databricks Lakehouse* — Girten | ~2024 | Databricks application patterns | L13 | **SKIP FOR CURRENT TARGET** | Specialized application scope beyond the current role target. |

### 11. Snowflake, dbt, and analytics engineering

| Rank/level | Book | Edition/year | Best use | Roadmap | Decision | Reason |
|---|---|---|---|---|---|---|
| 1 · dbt/analytics | *Analytics Engineering with SQL and dbt* — Machado & Russa | ~2023 | Modeling, testing, analytics-engineering workflow | L13 | **READ LATER** | Best conceptual dbt book after repeated dbt demand; do not duplicate L03 modeling. |
| 2 · dbt implementation | *Unlocking dbt* — Dorsey & Cyr | 2e, ~2025 | Practical dbt transformations/deployment | L13 | **ALTERNATIVE** | Choose instead of the analytics-engineering book when implementation speed is the goal. |
| 3 · dbt platform | *Data Engineering with dbt* — Zagni | ~2023 | Broader dbt-based platform | L13 | **ALTERNATIVE** | More platform breadth; unnecessary unless it fits the target architecture. |
| 4 · Snowflake reference | *Snowflake: The Definitive Guide* — Avila | ~2022 | Broad Snowflake platform reference | L13 | **REFERENCE ONLY** | Strong lookup source; official docs remain current version truth. |
| 5 · Snowflake project | *Snowflake Data Engineering* — Ferle | ~2023 | Practical Snowflake pipelines | L13 | **ALTERNATIVE** | Use for a Snowflake portfolio increment, not alongside every Snowflake book. |
| 6 · Snowflake warehouse | *Snowflake Data Warehouse Engineering* — Hander | Year not verified | Architecture, modeling, ELT, operations | L13 | **ALTERNATIVE** | Potentially good end-to-end fit, but overlaps the prior two heavily. |
| 7 · Snowflake modeling | *Data Modeling with Snowflake* — Gershkovich & Reis | ~2023 | Universal modeling implemented on Snowflake | L13 | **REFERENCE ONLY** | Useful after L03 if Snowflake is selected; not a replacement for Kimball foundations. |
| 8 · Snowflake SQL | *Learning Snowflake SQL and Scripting* — Beaulieu | ~2022 | Snowflake dialect and scripting | L13 | **REFERENCE ONLY** | Consult for dialect-specific gaps after portable SQL. |
| 9 · Snowflake operations | *Mastering Snowflake DataOps with DataOps.live* — Steelman | ~2024 | Vendor-tool-specific DataOps | L13/later | **SKIP FOR CURRENT TARGET** | Too specialized until a role names both Snowflake and this operating model/tool. |
| 10 · Advanced Snowflake | *Advanced Snowflake* — Ullah | ~2024–25 | Apps and ML workloads | L13/later | **SKIP FOR CURRENT TARGET** | Advanced platform/application scope does not improve first-role readiness now. |

## Just-in-time mapping to the 13 levels

| Level | Assigned reading | Optional lookup only | Explicitly not assigned |
|---|---|---|---|
| L01 — Advanced SQL | None; practise first | *Practical SQL* | Oracle PL/SQL; Snowflake SQL |
| L02 — PostgreSQL & Performance | None | *Grokking Relational Database Design*; targeted *Database System Concepts* sections | Full textbook reading |
| L03 — Dimensional Modeling | Verified Kimball selections above | Snowflake modeling only after L13 trigger | Enterprise architecture books |
| L04 — Python for DE | None; diagnostic and coding first | *Python for Data Analysis* | Generic beginner Python; Polars |
| L05 — APIs, ETL & Incremental Loads | Verified ETL Python and FoDE selections | Ingestion cookbook for a concrete problem | A second end-to-end ETL book |
| L06 — Testing & Data Quality | Verified ETL Python Ch. 13–14 | Observability later | Enterprise governance now |
| L07 — Git, Docker & Delivery | No book from this inventory | Official docs | General DataOps/cloud-architecture books |
| L08 — Airflow | Verified Airflow selections | Airflow 3 guide + official docs for version translation | Three parallel Airflow courses/books |
| L09 — Recovery & Reliability | Verified Airflow reliability selections | Observability and design patterns after failures exist | Senior operations breadth |
| L10 — PySpark & Parquet | Verified *Learning Spark* selections | *Spark in Action* only as alternative | Scala/Beam/Hadoop implementation tracks |
| L11 — Spark Performance | Verified *Learning Spark* Ch. 7 selection | *High Performance Spark, 2e* later | Algorithm cookbook cover-to-cover |
| L12 — Practical AWS | None; project + current docs | *Data Engineering with AWS, 2e* | Certification guide as prerequisite |
| L13 — Electives | One book at most after a documented trigger | Kafka/Iceberg/Delta/Snowflake/dbt/Azure/GCP references | Studying all stacks |

## Currency and caution notes

- The Kimball book is old by publication date but its modeling concepts remain useful; cloud implementation details elsewhere should not be inferred from it.
- *Learning Spark, 2nd ed.* targets Spark 3-era APIs. Its DataFrame/lazy-evaluation/partitioning concepts remain useful, while commands and defaults must be checked against current Apache Spark documentation.
- The 2015 Hadoop and 2019 Flink books are retained for architecture and stream-processing concepts, not current API instructions.
- Airflow 3 introduced breaking changes. The assigned Airflow book supplies durable concepts and patterns; the Airflow 3 guide and official documentation supply current syntax.
- DP-203-focused Azure books are not current certification paths. Preserve them only as historical concept references.
- Vendor books age faster than fundamentals. For AWS, Azure, GCP, Databricks, Snowflake, dbt, Kafka, Iceberg, and Delta, official documentation is the final source of version truth.

## Research basis

The ranking uses the supplied inventory, the five-file deep audit already completed, publisher tables of contents/catalog pages, author/publisher code repositories where available, official product documentation, and practitioner-fit checks against this roadmap's 54-job/42-early-career market dataset. Community sentiment was treated as a weak tie-breaker rather than technical proof.

Representative publisher references:

- [Fundamentals of Data Engineering — O'Reilly](https://www.oreilly.com/library/view/fundamentals-of-data/9781098108298/)
- [Designing Data-Intensive Applications, 2nd ed. — O'Reilly](https://www.oreilly.com/library/view/designing-data-intensive-applications/9781098119058/)
- [The Data Warehouse Toolkit — Kimball Group](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/books/data-warehouse-dw-toolkit/)
- [Database System Concepts, 7th ed. — official book site](https://www.db-book.com/)
- [Grokking Relational Database Design — Manning](https://www.manning.com/books/grokking-relational-database-design)
- [Practical SQL, 2nd ed. — official author site](https://practicalsql.com/)
- [Data Pipelines with Apache Airflow, 2nd ed. — Manning](https://www.manning.com/books/data-pipelines-with-apache-airflow-second-edition)
- [Learning Spark, 2nd ed. — O'Reilly](https://www.oreilly.com/library/view/learning-spark-2nd/9781492050032/)
- [High Performance Spark, 2nd ed. — O'Reilly](https://www.oreilly.com/library/view/high-performance-spark/9781098145842/)
- [Kafka: The Definitive Guide, 2nd ed. — O'Reilly](https://www.oreilly.com/library/view/kafka-the-definitive/9781492043072/)
- [Apache Iceberg: The Definitive Guide — O'Reilly](https://www.oreilly.com/library/view/apache-iceberg-the/9781098148614/)
- [Delta Lake: The Definitive Guide — O'Reilly](https://www.oreilly.com/library/view/delta-lake-the/9781098151935/)
- [Stream Processing with Apache Flink — O'Reilly](https://www.oreilly.com/library/view/stream-processing-with/9781491974285/)
