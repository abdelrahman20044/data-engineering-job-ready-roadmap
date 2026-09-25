# L01 · Advanced SQL Practice

| Tier | Time | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| 1 · SQL & Data Foundations | 14 hours | ●●●○○ | Existing SQL foundations | L02, L03 |

## What you will learn

Use SQL independently for analytical and data-quality work: reason about grain, NULLs and duplicate-producing joins; use CTEs and window functions; and validate results instead of trusting a query because it runs.

## Topics and learning resources

| Order | Topic | Primary resource | Arabic / alternative | Action |
|---:|---|---|---|---|
| 1 | Diagnostic | [PostgreSQL Exercises](https://pgexercises.com/) | — | Work for 90 minutes with hints and answers closed; record gaps only |
| 2 | Joins, cardinality, NULLs | [PostgreSQL tutorial: joins](https://www.postgresql.org/docs/current/tutorial-join.html) and [conditional expressions](https://www.postgresql.org/docs/current/functions-conditional.html) | [Mahara-Tech: Transact-SQL](https://maharatech.gov.eg/) — use only matching lessons | Write queries that expose and explain duplicate rows |
| 3 | Aggregation and windows | [PostgreSQL tutorial: window functions](https://www.postgresql.org/docs/current/tutorial-window.html) | [Modern SQL: window functions](https://modern-sql.com/feature/window-functions) | Solve ranking, running-total, lag/lead and framed-window tasks |
| 4 | CTEs and recursion | [PostgreSQL `WITH` queries](https://www.postgresql.org/docs/current/queries-with.html) | [Modern SQL](https://modern-sql.com/) | Refactor a multi-stage analysis and solve one recursive task |
| 5 | Interview transfer | [DataLemur SQL questions](https://datalemur.com/questions?category=SQL) | [StrataScratch](https://www.stratascratch.com/) | Solve medium questions without copying patterns |
| 6 | Validation SQL | Project data | — | Write count, uniqueness, null, accepted-value and referential checks |

## Practice

- Save the diagnostic results in `sql-diagnostic.md`: problem, first attempt, mistake, corrected rule.
- Complete at least 12 non-trivial problems independently, including 4 window-function problems.
- For one deliberately duplicated join, predict row counts before running it.
- Produce five business queries and five validation queries for the flagship.

## Project application

Start the [flagship project](../projects/flagship.md): choose the business process and explore the source data. Commit analytical and validation SQL with expected results and explanations for non-obvious logic.

## Interview check

Explain `WHERE` vs `HAVING`, `GROUP BY` vs window functions, `ROW_NUMBER` vs `RANK`, how NULL affects comparisons, why joins multiply rows, and how you validate a query result.

## Completion criteria

- [ ] Diagnostic gaps are documented and corrected.
- [ ] 12+ independent solutions are committed.
- [ ] Five business and five validation queries run against project data.
- [ ] You can explain each solution without notes.

## Next

Continue to [L02 · PostgreSQL & Performance Essentials](../02-postgresql-performance/README.md), then use L03 to turn the business process into a dimensional model.

Need an alternative or deeper reference? Open [`resources.md`](resources.md).
