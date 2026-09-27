# L03 · Dimensional Modeling & Warehousing

| Tier | Time | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| 1 · SQL & Data Foundations | 24 hours | ●●●○○ | L01 | L05, flagship warehouse |

## What you will learn

Translate a business process into a model with an explicit grain, useful facts and dimensions, defensible keys, and a deliberate history strategy. This is the decision point where the audited Kimball reading belongs.

## Diagnostic gate · 45 minutes

Before studying, take one small operational dataset and, without references, declare the business process and grain, identify the fact and dimensions, choose natural/surrogate keys, classify the measures, and state whether one dimension needs SCD Type 1 or 2. Then test the proposed grain against five sample rows.

- If every choice is coherent and you can defend it, skip introductory explanations and move directly to the selected Kimball sections plus the flagship model.
- If the grain changes while you answer, facts mix levels of detail, or history behavior is vague, study only those exposed gaps before retrying with a different process.

## Topics and learning resources

| Order | Topic | Primary resource | Arabic / alternative | Action |
|---:|---|---|---|---|
| 1 | OLTP vs analytics | *The Data Warehouse Toolkit*, Ch. 1 pp. 7–22 | [Tech Vault: OLTP vs OLAP](https://www.youtube.com/watch?v=LU8pfUrdXWE) | Write why the project needs an analytical model |
| 2 | Four-step process and grain | Kimball Ch. 2 pp. 37–57 + [Kimball techniques](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/kimball-techniques/dimensional-modeling-techniques/) | [Garage Education: DWH Modelling](https://www.youtube.com/playlist?list=PLxNoJq6k39G_Ffv8Na1oRbob0sVHfFc_T) | Declare the business process and grain before tables |
| 3 | Facts, measures and fact-table types | Kimball Ch. 3 pp. 70–79 + [Kimball technique summary](https://www.kimballgroup.com/wp-content/uploads/2013/08/2013.09-Kimball-Dimensional-Modeling-Techniques11.pdf) | Same Arabic alternative | Classify measures and choose transactional, periodic-snapshot or accumulating-snapshot facts |
| 4 | Dimensions and keys | Kimball Ch. 3 pp. 98–104 + technique summary | Same Arabic alternative | Choose natural/surrogate keys and justify date, conformed, role-playing and degenerate dimensions |
| 5 | Star schema and SCD Type 1/2 | Kimball Ch. 5 pp. 147–154 | Kimball technique summary | Draw the schema and implement one justified history policy |
| 6 | Physical warehouse | PostgreSQL DDL + L02 constraints | — | Build, seed and validate the model in PostgreSQL |

## Practice

- Write the business event in one sentence and the grain in one precise sentence.
- Make a source-to-target matrix: source fields → dimension/fact columns → transformation rule.
- Classify each measure as additive, semi-additive or non-additive and choose the fact-table type before writing DDL.
- Test the model with five business questions before implementing it.
- Implement at least one SCD Type 2 change only if the chosen dimension genuinely needs history.

## Project application

Create `docs/model.md`, a star-schema diagram, versioned DDL, seed data and five business queries in the [flagship](../projects/flagship.md). Record alternatives considered and why they were rejected.

## Interview check

Explain grain, fact vs dimension, additive/semi-additive/non-additive measures, surrogate keys, star vs snowflake, fact-table types, and SCD 1 vs 2 using your own model.

## Completion criteria

- [ ] Business process and grain are explicit.
- [ ] Facts, dimensions, keys and history decisions are justified.
- [ ] PostgreSQL DDL and seed data work from a clean database.
- [ ] Five business questions are answered without violating grain.

## Next

Continue to [L04 · Python for Data Engineering](../04-python-for-data-engineering/README.md), then L05 will load this model.

Exact book pages, alternatives and later topics are in [`resources.md`](resources.md).
