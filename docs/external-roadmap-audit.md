# External Roadmap and Practitioner Audit

**Audit date:** 2026-09-27  
**Decision authority:** this repository's 54-job market sample, including 42 early-career descriptions.  
**Purpose:** use external sources to improve explanation, exercises, resources, and decision rules—without replacing the market-driven 13-level scope.

## Sources reviewed

| Source | What was inspected | Strongest contribution | Main limitation for this roadmap |
|---|---|---|---|
| [Ahmed Shaaban — Data Engineering Mentorship](https://github.com/ahmedshaaban1999/Data_Engineering_Mentorship) | Level plan, deliverables, projects, and resource lists | Concrete SQL/problem-solving deliverables and project-first expectations | Front-loads HDFS and Kafka; broad resource lists and DSA volume exceed this target |
| [Data With Baraa — 2026 Roadmap](https://candle-gosling-511.notion.site/Data-Engineering-Roadmap-2026-Data-With-Baraa-2e534b251f128086b4cef556b8712103) plus [public explanation](https://www.blog.datawithbaraa.com/p/how-to-become-data-engineer-in-2026) | Public roadmap structure, entry-to-senior phases, linked Databricks project | Separates job-entry skills from post-hire growth; practise, build a portfolio, apply before 100% | Treats Databricks as a central pre-hire platform and gives certification more weight than this market sample supports |
| [IEEE Man CSC 2025 — General Roadmap](https://github.com/Welloz03/Data-Engineering-Roadmap-IEEEManCSC-2025/blob/main/General%20Roadmap.md) | General stages, weekly version, links, practice suggestions | Clear beginner/intermediate/advanced staging; continued SQL practice | Generic breadth; mixes NoSQL, Snowflake, dbt, BI, vector databases, and AI without target-job triggers |
| [Yahia Sherif — Data Engineering Roadmap 2026](https://github.com/Yahiasherif002/Data-Engineering-Roadmap-2026) | 30-level hierarchy, exit criteria, dependency mapping, bilingual resources, audits | Excellent information architecture, evidence-based completion, and resource-type separation | Approximately 1,600 hours and senior-scope breadth; not suitable as an entry-role curriculum |
| [DataCamp — Associate Data Engineer in SQL](https://www.datacamp.com/tracks/associate-data-engineer-in-sql) | Track outline and project/practice model | Bounded interactive SQL, database design, and warehousing practice | Browser exercises do not replace independent PostgreSQL/project evidence; Snowflake emphasis is platform-specific |
| [DataCamp — Data Engineer in Python](https://www.datacamp.com/tracks/data-engineer-in-python) | Track outline and prerequisites | Useful alternative practice for APIs, ETL, Airflow, Git, and projects | Paid, broad, and risks becoming a second curriculum |
| [DataCamp — Professional Data Engineer in Python](https://www.datacamp.com/tracks/professional-data-engineer) | Advanced track topics | Shows testing, Docker, shell, PySpark, and dbt as later engineering breadth | NoSQL/dbt and professional-level scope should not be pulled into the core automatically |
| Supplied roadmap image | Core/concepts/stack/stand-out/AI grouping | Clearly separates transferable concepts from selectable stacks | A single creator's opinion; overpromotes CI/CD, Kafka, Terraform, and AI relative to this early-career sample |
| `dataa.txt` practitioner discussion | All 678 lines / roughly 33,000 words | Real interview, production, regional-stack, and learning-order experience | Anecdotal and internally inconsistent; company-, era-, and speaker-specific claims require verification |

## Cross-source consensus

| Topic | Existing market evidence | Cross-source signal | Decision |
|---|---:|---|---|
| SQL | 98% of early-career sample | Universal core; interview practice repeatedly emphasized | Keep L01 first and exercise-driven |
| Python | 93% | Universal implementation language; project code matters more than generic syntax study | Keep diagnostic-first L04 and practical L05 |
| ETL/ELT and pipelines | 86% | Concepts transfer across vendors; rerun/recovery behavior matters | Keep L05 central; add one focused idempotency reading |
| Warehousing | 74% | Learn the analytical purpose before collecting tools | Keep L03 before pipeline orchestration |
| Data modeling | 64% | Grain/facts/dimensions appear in interviews and real work | Preserve verified Kimball selections and project schema evidence |
| Cloud | 62% | Learn one platform through deployment; services are analogous but details differ | Keep one practical AWS implementation in L12; other providers triggered in L13 |
| Testing/data quality | 45% | Practitioners distinguish quality from cleaning and expect explicit validation | Keep L06 before the application milestone |
| Spark/PySpark | 36% | Valuable distributed-processing step, not a prerequisite for every application | Keep L10–L11 after the first application milestone |
| Airflow | 29% | Practical orchestration and recovery skills; business logic should remain testable outside DAGs | Keep L08–L09 after the batch pipeline exists |
| Git | Supporting evidence | Effectively mandatory engineering hygiene across sources | Keep L07; already used from the start |
| Docker | Supporting evidence | Useful proof of reproducibility, even when not named in every JD | Keep bounded L07 scope; do not add Kubernetes |

## Where sources disagree

| Question | Positions found | Resolution for this roadmap |
|---|---|---|
| When should candidates apply? | Finish a broad stack/certification first vs apply once foundations and one project exist | Apply selectively now; active cadence after L07. Interviews feed a bounded gap list. |
| Should Databricks be core? | Data With Baraa makes it central; other sources treat the stack as selectable | Keep it L13. Spark concepts are core enough for L10; Databricks requires repeated target-job evidence. |
| How much Hadoop? | Some practitioners call it obsolete; regional roadmaps retain a full ecosystem | Keep HDFS/YARN/MapReduce concepts as prior foundation/reference; no deep implementation before a matching role. |
| How much Kafka? | Several diagrams make it a stand-out/core-adjacent skill; others treat it as production specialization | Keep streaming concepts and Kafka as job-triggered L13. Do not delay applications. |
| Certification value | Some speakers/roadmaps recommend it strongly; others prioritize projects and experience | Optional. A certification never substitutes for working project evidence. |
| Read first or build first? | Book/course-first and project-first camps both appear | Use a short concept → targeted practice → project increment loop. No cover-to-cover gate. |
| On-prem before cloud? | Some speakers say on-prem fundamentals are essential; others learned directly in cloud | Learn the transferable storage/compute/network/security model; implement locally, then deploy one pipeline. |
| Kimball depth | Canonical foundation vs not universal/modern enough | Use selected grain/fact/dimension/SCD chapters and implement them; do not treat Kimball as the only architecture. |
| DataOps meaning | Operations/support role vs DevOps-style automation for data | Treat the label as ambiguous. Inspect responsibilities rather than learning a branded syllabus. |

## Topic comparison across sources

Legend: `Core` = pre-first-role focus, `Later` = valuable after foundation, `Stack` = employer/technology dependent, `Broad` = source includes more than this roadmap needs.

| Topic | This roadmap | Ahmed | Baraa | IEEE | Yahia | DataCamp | Transcript | Image |
|---|---|---|---|---|---|---|---|---|
| SQL | Core | Core | Core | Core | Core | Core | Core | Core |
| Python | Core | Core + DSA | Core | Core | Core | Core | Core | Core |
| Database design/internals | Core, bounded | Partial | Concepts | Core | Deep | SQL track | Strong core | Implicit |
| DWH/modeling | Core | Core | Concepts | Intermediate | Core | SQL track | Strong core | Core concept |
| ETL/incremental loads | Core | Projects | Core concept | Intermediate | Core | Core | Strong core | Core concept |
| Testing/data quality | Core | Partial | Partial | Partial | Deep | Professional | Important | Core concept |
| Git/Docker | Core supporting | Core | Git core | Later | Core | Professional | Git mandatory; Docker useful | Git core; Docker stand-out |
| Airflow/reliability | Later core | Resource list | Stack | Advanced | Core | Python track | Important after pipeline | One stack branch |
| Spark | Later core | Four-week block | Central via Databricks | Advanced | Core | Professional | Important after foundation | One stack branch |
| Cloud | One practical provider | Limited | Platform choice | Azure-heavy | Multi-cloud breadth | Platform examples | Provider depends on company | AWS/Azure branches |
| Kafka/streaming | Job-triggered | Three-week block | After job | Advanced | Full level | Limited | Stack-dependent | Stand-out |
| Hadoop | Concepts/reference | Core block | Not central | Advanced | Full level | Minimal | Disputed/legacy | Absent |
| dbt/Snowflake | Job-triggered | Limited | Platform choice | Intermediate | Full breadth | Professional/SQL | Company-dependent | One stack branch |
| Kubernetes/Terraform | Not core | Limited | Later | Docker/K8s | Full level | Limited | Advanced/ops | Terraform stand-out |
| Governance/MDM | Later/reference | Limited | Senior | Intermediate | Full level | Limited | Important but seniorer | Absent |
| AI pipelines/RAG/agents | Not added | Absent | After job | AI/vector breadth | Advanced breadth | Absent | Not foundational | Later stand-out |

## Practitioner Discussion — `dataa.txt`

### Evidence labels

- **A — Corroborated principle:** agrees with the job sample and multiple external sources.
- **B — Useful practitioner opinion:** actionable, but not directly measured by the sample.
- **C — Stack/company specific:** valid in its context; not general curriculum.
- **D — Possibly outdated:** technology or hiring context may have moved.
- **E — Debatable:** reasonable people in the transcript disagreed or the claim overreaches.

### Foundational / mandatory

| Insight | Label | Curriculum consequence |
|---|---|---|
| A roadmap is a map, not a checklist; no engineer uses every listed tool | A | Preserve the 13-level core and trigger electives from jobs |
| Strong SQL matters disproportionately in work and interviews | A | Keep L01 first and continue SQL practice throughout |
| Understand relational databases, keys, normalization, indexes, and query behavior before vendor tools | A | Keep L02 before cloud warehouses and tool-specific databases |
| Learn DWH/modeling before blindly constructing pipelines | A | Keep L03 before L05/L08 |
| Python should be used to build and debug, not merely studied | A | Keep diagnostic-first L04 and immediate project integration |
| ETL/pipeline concepts transfer even when tools differ | A | Teach pagination, state, idempotency, transactions, and failure handling explicitly |
| Git is effectively mandatory | A | Preserve continuous Git use and L07 delivery evidence |
| Start with a simple project and add a tool only when the project needs it | A | Preserve one evolving flagship plus one distinct Spark project |

### Important after foundation

| Insight | Label | Curriculum consequence |
|---|---|---|
| Distributed-systems reasoning matters more than memorizing Hadoop commands | A/B | Teach partitions, shuffles, failures, and delivery semantics through Spark; keep Hadoop implementation optional |
| Airflow should orchestrate testable tasks rather than contain all business logic | A/B | Preserve modular Python pipeline before DAG work |
| Data quality is not synonymous with cleaning | A | L06 requires constraints, freshness/completeness/uniqueness checks, quarantine, and failure policy |
| Cost and performance become real engineering constraints in cloud/production | A/B | Include bounded cost/performance reasoning in L11–L12, not a FinOps curriculum |
| Basic shell, Linux, Docker, and reproducibility remove common operational friction | A/B | Keep supporting scope in L07; no Kubernetes expansion |

### Stack-dependent

| Insight | Label | Treatment |
|---|---|---|
| Azure, AWS, and GCP expose analogous capabilities but employers standardize on different ecosystems | B/C | Learn AWS practically because of existing background; translate concepts when a job triggers another cloud |
| Informatica appears in some Saudi/Gulf enterprise environments | C/D | Monitor job evidence; do not add to core without repeated current demand |
| DAMA/governance knowledge can matter in Gulf organizations | C | Preserve as later/reference; not an entry-level implementation gate |
| Kafka depth depends on whether the team owns streaming infrastructure | C | L13 trigger only |
| Hadoop clusters remain in some banks/telecoms while greenfield systems often use object storage/managed compute | C/D | Retain architecture vocabulary; skip deep MapReduce work unless required |

### Interview-relevant

| Insight | Label | Curriculum consequence |
|---|---|---|
| Junior candidates are often tested on SQL problem solving and a concrete business-modeling use case | A/B | SQL diagnostic/problems plus grain/facts/dimensions explanation remain completion evidence |
| A candidate can apply with strong foundations before completing every tool | A/B | Selective applications now; steady cadence after L07 |
| Failed interviews reveal the next bounded learning gap | B | Add an interview-gap feedback rule to the application milestone |
| Senior interviews emphasize trade-offs, failures, and system stories more than definitions | B | Project READMEs and interview checks require decisions and failure/recovery explanations |

### Production / seniorer concerns

| Insight | Label | Treatment |
|---|---|---|
| Lineage, impact analysis, governance, MDM, reference data, security/masking, and broad observability matter in mature organizations | A/B | Awareness and later/reference material; do not inflate entry curriculum |
| Operations, on-call ownership, capacity/cost optimization, and organization-wide platform design grow after joining | B/C | L09–L12 supply an introduction; deeper study waits for role context |
| Job titles such as DataOps/MLOps are ambiguous | A/B | Inspect actual responsibilities, not the label |

### Optional / specialized

- Deep Kafka administration, Kafka Streams/ksqlDB, and Flink.
- MDM implementations and formal governance frameworks.
- Vendor-specific ETL suites such as Informatica unless target jobs repeat them.
- Deep Hadoop administration/MapReduce APIs.
- Multiple cloud providers, lakehouse formats, and managed warehouses at once.

### Outdated or needs caution

| Claim heard | Classification | Corrected decision |
|---|---|---|
| “Hadoop is obsolete” | D/E — overbroad | HDFS/YARN/MapReduce concepts still explain distributed storage/compute and survive in some estates; deep implementation is not core. |
| “Spark is the future” | E — subjective | Spark has meaningful early-career demand (36%) but is not required before the application milestone. |
| One provider is categorically “worst” for ETL | C/E | Provider choice depends on employer stack, region, contracts, managed services, and workload. |
| Certifications are mandatory | C/E | They can help in particular markets; project evidence and fundamentals remain the default priority. |
| Long overtime/grinding is necessary for the first decade | E | Rejected as career advice; deliberate practice and sustained delivery are the objective. |

### Preserved disagreements

- **DataOps:** some speakers meant production support/operations; others meant automated testing, deployment, and observability for data. The roadmap uses the latter practices without depending on the title.
- **Certification:** speakers disagreed on whether credentials materially affect hiring. The roadmap makes them optional and job-triggered.
- **On-prem before cloud:** one camp viewed on-prem experience as essential; another successfully learned cloud-first. The roadmap teaches transferable concepts locally, then one cloud deployment.
- **Reading vs building:** speakers varied from book-first to project-first. The roadmap uses short, just-in-time reading immediately followed by an artifact.
- **Kimball depth:** some favored extensive study; others learned modeling mainly through use cases. The roadmap assigns selected canonical sections and requires a real schema/explanation.
- **Remote vs office learning:** opinions reflected personal mentoring experiences, not a universal rule, so no curriculum change was made.

## Resource candidates: accepted

Only two new content links were accepted; both serve a distinct purpose and neither creates a new course.

| Resource | Type/purpose | Placement | Why accepted |
|---|---|---|---|
| [Functional Data Engineering — Maxime Beauchemin](https://maximebeauchemin.medium.com/functional-data-engineering-a-modern-paradigm-for-batch-data-processing-2327ec32c42a) | Concept reading: immutable inputs, deterministic/idempotent batch tasks, reproducibility | L05 reference, immediately before the rerun experiment | Directly strengthens an existing exit criterion and the flagship's incremental-load design |
| [Streaming Systems, Ch. 1–2 / Streaming 101 concepts](https://www.oreilly.com/library/view/streaming-systems/9781491983867/ch01.html) | Concept reference: bounded/unbounded data, event vs processing time, windowing/triggers | L13 Kafka/streaming, only after a trigger | Supplies transferable concepts before a vendor API; explicitly not active curriculum |

One process rule was also accepted: record interview gaps and patch only repeated or high-impact gaps without pausing the application cadence.

## Resource candidates considered but rejected

| Candidate | Source | Reason not imported |
|---|---|---|
| SQLZoo, SQLBolt, Mode, HackerRank, LeetCode SQL duplicates | Ahmed/IEEE/Yahia | Existing PostgreSQL Exercises + DataLemur path is sufficient; extra platforms increase switching cost |
| Four-week general Python/DSA plan | Ahmed | Backend experience makes generic syntax/DSA repetition low value; the roadmap uses a diagnostic |
| Full HDFS block before Spark | Ahmed/Yahia | Concepts already exist; no repeated early-career evidence justifies implementation depth |
| Three-week Kafka block | Ahmed | Kafka remains an elective in the market dataset |
| Databricks bootcamp as the main portfolio | Data With Baraa | Strong project, but it would replace rather than improve the current vendor-neutral flagship and prematurely select a platform |
| DataCamp tracks as required curriculum | DataCamp | Useful interactive alternatives, but paid breadth and browser exercises duplicate the active path |
| Full dbt/Snowflake/NoSQL sequence | IEEE/DataCamp/Yahia | Job-triggered tools; would inflate the core |
| Vector database, RAG, AI agents/pipelines | IEEE/image/Baraa later phases | Not supported as first-role priorities by the current early-career dataset |
| Kubernetes and Terraform level | Yahia/image | Terraform stays trigger-only; Kubernetes is not needed for current project evidence |
| Full distributed-systems/system-design level | Yahia | Valuable later; DDIA and targeted concepts are enough before the first role |
| Multiple Arabic/English alternatives per topic | Several roadmaps | Existing repo already follows one primary + meaningful alternative + official reference; more would increase decision fatigue |
| Old Airflow video playlists as primary | Ahmed/IEEE | Airflow 3 has breaking changes; audited book + current official docs are safer |

## Actual roadmap changes from this audit

1. Added *Functional Data Engineering* to L05 as a single focused concept reading tied to the existing idempotency/rerun lab.
2. Added *Streaming Systems* Ch. 1–2 as a **trigger-only** conceptual reference in L13, before Kafka vendor material.
3. Added an interview-gap feedback rule to the application milestone: record the question, classify the gap, patch repeated/high-impact fundamentals, and continue applying.
4. Added this audit and the full [book guide](book-guide.md) to make future decisions traceable.

No level order, hours, project architecture, application milestone, or market-derived priority was changed.

## Topics intentionally not added

- Kubernetes, full Terraform/IaC, platform engineering, or multi-cloud breadth.
- AI pipelines, RAG, vector databases, or agents.
- Deep Hadoop/MapReduce/Hive implementation.
- Mandatory Kafka/Flink/Beam streaming.
- Mandatory Databricks, Snowflake, dbt, Fabric, ADF, or a second cloud.
- Formal governance/MDM certification paths.
- A certification track.
- Another portfolio project or another large resource catalog.

## Decision rule for future imports

A resource enters an active level only when it improves a current learning objective better than the existing primary, fills a verified gap, or enables a required artifact. Otherwise it belongs in reference material—or nowhere. A roadmap idea enters the curriculum only when repeated market evidence or project failure supports it.
