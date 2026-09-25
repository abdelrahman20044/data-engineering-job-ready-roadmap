# L03 · Dimensional Modeling & Warehousing

| Tier | Time | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| 1 · SQL & Data Foundations | 24 hours | ●●●○○ | L01 | L05, flagship warehouse |

## What you will learn

Translate a business process into a model with an explicit grain, useful facts and dimensions, defensible keys, and a deliberate history strategy. This is the decision point where the audited Kimball reading belongs.

## Topics and learning resources

| Order | Topic | Primary resource | Arabic / alternative | Action |
|---:|---|---|---|---|
| 1 | OLTP vs analytics | *The Data Warehouse Toolkit*, Ch. 1 pp. 7–22 | Tech Vault OLTP/OLAP explanation | Write why the project needs an analytical model |
| 2 | Four-step process and grain | Kimball Ch. 2 pp. 37–57 + [Kimball techniques](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/kimball-techniques/dimensional-modeling-techniques/) | Garage Education warehouse playlist | Declare the business process and grain before tables |
| 3 | Facts, dimensions and keys | Kimball Ch. 3 pp. 70–79 | Same Arabic alternative | Classify measures and choose surrogate/business keys |
| 4 | Star schema and reusable dimensions | Kimball Ch. 3 pp. 98–104 | [Data with Zach modeling material](https://www.youtube.com/@eczachly_) | Draw and critique the project star schema |
| 5 | SCD Type 1 and Type 2 | Kimball Ch. 5 pp. 147–154 | Kimball technique summaries | Implement one justified history policy |
| 6 | Physical warehouse | PostgreSQL DDL + L02 constraints | — | Build, seed and validate the model in PostgreSQL |

## Practice

- Write the business event in one sentence and the grain in one precise sentence.
- Make a source-to-target matrix: source fields → dimension/fact columns → transformation rule.
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
