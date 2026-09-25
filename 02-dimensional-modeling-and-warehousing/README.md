# Module 02 — Dimensional Modeling & Warehousing

## Why this matters

Warehousing appeared in about 74% and data modeling in about 64% of early-career descriptions. A junior engineer should be able to declare grain before drawing tables and defend what each fact row represents.

## Prerequisites

Module 01 and five written business questions for the flagship domain.

## Outcome

You can turn one business process into a PostgreSQL star schema, make a reasoned SCD choice, load representative data, query it correctly, and explain trade-offs.

## Topic path

### 1. Business process and grain

**Learn**

- [Kimball Group — grain](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/kimball-techniques/dimensional-modeling-techniques/grain/).

**Read**

- *The Data Warehouse Toolkit*, 3e: Ch. 1 pp. 7–22 and Ch. 2 pp. 37–57.

**Practice**

- Write three candidate grain statements in the form: “one row per …”. Reject any that mixes events or aggregation levels.

**Apply**

- Commit `docs/model.md` with the chosen business process, atomic grain, and the five questions it supports.

### 2. Facts, dimensions, and keys

**Learn**

- [Kimball dimensional modeling techniques](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/kimball-techniques/dimensional-modeling-techniques/), especially transaction facts, dimensions, and surrogate keys.

**Read**

- *The Data Warehouse Toolkit*, 3e: Ch. 3 pp. 70–79 and 98–104.

**Practice**

- Classify each candidate field as measure, degenerate dimension, dimension attribute, natural key, or warehouse key. Remove fields that violate the declared grain.

**Apply**

- Design one atomic fact table and the minimum useful dimensions. Create a diagram and PostgreSQL DDL with PK/FK/not-null constraints.

### 3. Slowly changing dimensions

**Learn**

- [Kimball Group — slowly changing dimension techniques](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/kimball-techniques/dimensional-modeling-techniques/).

**Read**

- *The Data Warehouse Toolkit*, 3e: Ch. 5 pp. 147–154.

**Practice**

- Given a customer attribute correction and an address change, decide between Type 1 and Type 2 and state the business consequence.

**Apply**

- Implement Type 1 unless historical attribute state materially changes a flagship question. If Type 2 is justified, add effective dates/current flag and tests for non-overlapping versions. Do not add SCD2 to look sophisticated.

### 4. Warehouse SQL quality and performance reasoning

**Learn / reference**

- [PostgreSQL `EXPLAIN`](https://www.postgresql.org/docs/current/using-explain.html).
- [PostgreSQL indexes introduction](https://www.postgresql.org/docs/current/indexes-intro.html).

**Practice**

- Run `EXPLAIN (ANALYZE, BUFFERS)` on one representative query before and after one defensible index. Record what changed and what did not.

**Apply**

- Add duplicate, orphan, null, and row-count validation queries. Add an index only when its query/access pattern justifies it.

## Module practice

- Model a second, unfamiliar business process on paper in 45 minutes.
- Review the model from the fact row outward: can every dimension join at the same grain?
- Load a small seed dataset containing a late correction and demonstrate the chosen change-handling rule.

## Build

Flagship Phase 1 deliverable:

- `docs/model.md`: business process, grain, assumptions, facts/dimensions, SCD decision.
- Star-schema diagram.
- Versioned DDL/migration files and seed data.
- Five analytical queries tied to the original questions.
- Validation SQL and one documented `EXPLAIN` experiment.

## Interview check

Explain without notes:

1. Why grain is declared before facts and dimensions.
2. Natural vs surrogate keys.
3. Transaction, periodic snapshot, and accumulating snapshot facts.
4. SCD Type 1 vs Type 2 and when not to use Type 2.
5. Why a star schema is denormalized and what trade-off that creates.
6. What `EXPLAIN ANALYZE` actually measured in your project.

## Evidence

Design decisions, DDL, diagram, seed/load script, query results, validation queries, and performance note in the flagship repository.

## Done when

Another engineer can infer exactly what one fact row means, run the schema and queries, and understand each key/SCD decision. You can defend the model without opening Kimball.

## Next

[Module 03 — Python ETL](../03-python-etl/README.md)
