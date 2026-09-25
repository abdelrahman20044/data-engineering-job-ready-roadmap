# L02 · PostgreSQL & Performance Essentials

| Tier | Time | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| 1 · SQL & Data Foundations | 10 hours | ●●●○○ | L01 | L03, L11 |

## What you will learn

Design trustworthy PostgreSQL tables and use evidence—not folklore—to improve a slow query. The objective is basic performance reasoning, not database administration.

## Topics and learning resources

| Order | Topic | Primary resource | Arabic / alternative | Action |
|---:|---|---|---|---|
| 1 | Keys, constraints, data types | [PostgreSQL DDL constraints](https://www.postgresql.org/docs/current/ddl-constraints.html) | Tech Vault database-design material | Strengthen project DDL so invalid states are rejected |
| 2 | Index mental model | [Use The Index, Luke!](https://use-the-index-luke.com/) | Tech Vault database-storage material | Predict whether an index can help before creating it |
| 3 | Plans and scans | [Using `EXPLAIN`](https://www.postgresql.org/docs/current/using-explain.html) | [CMU 15-445](https://15445.courses.cs.cmu.edu/) for a deeper explanation | Compare sequential/index scans and join strategies |
| 4 | Statistics and maintenance | [Planner statistics](https://www.postgresql.org/docs/current/planner-stats.html) | — | Explain estimates and recognize stale/inadequate statistics |
| 5 | Transactions | [PostgreSQL transactions tutorial](https://www.postgresql.org/docs/current/tutorial-transactions.html) | — | Make one load atomic and safely retryable |

## Practice

- Add primary, foreign, unique, check and not-null constraints where the data contract justifies them.
- Capture `EXPLAIN (ANALYZE, BUFFERS)` before and after one justified index/query change.
- Write a short conclusion separating measured improvement from assumptions.
- Demonstrate commit and rollback on a small load.

## Project application

Improve the flagship warehouse DDL and save one performance note with the query, plan excerpts, measured timings, index choice and trade-off.

## Interview check

Explain composite-index order, sequential vs index scans, estimated vs actual rows, why an index can hurt writes, and what a transaction protects during a load.

## Completion criteria

- [ ] Constraints enforce the project’s key invariants.
- [ ] One before/after plan experiment is committed.
- [ ] The chosen index has a workload-based justification.
- [ ] You can explain the result without claiming universal speedups.

## Next

Continue to [L03 · Dimensional Modeling & Warehousing](../03-dimensional-modeling-warehouse/README.md).

Need more depth? Open [`resources.md`](resources.md).
