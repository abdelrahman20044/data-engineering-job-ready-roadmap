# Module 01 — SQL & PostgreSQL

## Why this matters

SQL appeared in about 98% of the early-career market sample. The goal is not syntax completion; it is independent problem solving, correct handling of grain/cardinality/nulls, and SQL another engineer can review.

## Prerequisites

Existing SQL fundamentals: filtering, joins, grouping, subqueries, and basic window functions. If the diagnostic shows a gap, repair only that gap.

## Outcome

You can translate a business question into correct PostgreSQL, validate the result, identify duplicate-producing joins, and explain the query without notes.

## Step 1 — 90-minute diagnostic

Use [PostgreSQL Exercises](https://pgexercises.com/) with hints/answers closed. Create `sql-diagnostic.md` and record the problem, elapsed time, result, and diagnosed gap.

1. Two multi-table joins: one inner, one outer.
2. Two aggregation problems using `GROUP BY`, `HAVING`, conditional aggregation, or distinct counts.
3. Two window problems: ranking and a running/rolling calculation.
4. One date/time problem.
5. One problem requiring a CTE or subquery.
6. One data-quality query that finds duplicates or missing relationships.

**Pass gate:** at least 8/10 correct without copying; all results checked for grain and duplicate multiplication. If you pass, skip beginner SQL lessons. If you miss a category, use the map below and solve three new problems in that category.

## Topic path

### 1. Join cardinality and null behavior

**Learn / review**

- [PostgreSQL tutorial — joins between tables](https://www.postgresql.org/docs/current/tutorial-join.html).
- Use SQLBolt lessons 6–7 only if the diagnostic exposes a basic join gap: [multi-table queries](https://sqlbolt.com/lesson/6) and [outer joins](https://sqlbolt.com/lesson/7).

**Practice**

- Solve three [PostgreSQL Exercises joins/subqueries](https://pgexercises.com/questions/joins/) without answers.
- For each result, write the expected row grain before running the query.

**Apply**

- In the flagship, write a query that deliberately demonstrates and then fixes a one-to-many join multiplication bug.

### 2. Aggregation and analytical windows

**Learn / review**

- [PostgreSQL window-functions tutorial](https://www.postgresql.org/docs/current/tutorial-window.html).
- [PostgreSQL Exercises — aggregates](https://pgexercises.com/questions/aggregates/) for worked practice.

**Practice**

- Solve rank/top-N, running total, lag/lead comparison, and rolling-average problems.
- Then solve four medium SQL interview problems from [DataLemur's SQL set](https://datalemur.com/questions?category=SQL).

**Apply**

- Add two business queries to the flagship: one period-over-period metric and one top-N-within-group metric.

### 3. CTEs, subqueries, set logic, and readable decomposition

**Learn / review**

- [PostgreSQL `WITH` queries](https://www.postgresql.org/docs/current/queries-with.html).

**Practice**

- Rewrite one nested query as named CTE steps, then state whether clarity improved.
- Solve one `EXISTS`/`NOT EXISTS` problem and one `UNION`/`INTERSECT`/`EXCEPT` problem.

**Apply**

- Use CTE names that express business steps in a flagship transformation query. Avoid a CTE for every line.

### 4. Data validation SQL

**Learn / review**

- Review PostgreSQL constraints: [data definition — constraints](https://www.postgresql.org/docs/current/ddl-constraints.html).

**Practice**

- Write checks for uniqueness, required values, accepted ranges, referential integrity, and unexpected row-count changes.

**Apply**

- Save validation SQL under `sql/quality/` and make each check return zero failing rows or an explicit metric.

## Module practice

- [ ] Diagnostic completed honestly.
- [ ] At least 12 non-trivial problems solved independently across joins, aggregates, windows, dates, and set/subquery logic.
- [ ] Three incorrect first attempts documented with the cause and corrected reasoning.
- [ ] Queries formatted, named clearly, and committed in small logical commits.

## Build

Do not finalize the flagship schema yet. Select the project domain/API and write five analytical questions the eventual warehouse must answer. These questions become constraints for Module 02.

## Interview check

Explain without notes:

1. `WHERE` vs `HAVING`.
2. `ROW_NUMBER`, `RANK`, and `DENSE_RANK`.
3. Window functions vs `GROUP BY`.
4. Why a correct-looking join can inflate measures.
5. `NOT EXISTS` vs `NOT IN` when nulls are present.
6. How you would test whether a SQL result is trustworthy.

## Evidence

- Diagnostic record, independent solutions, failure notes, and five business questions.
- No copied solution is counted as evidence.

## Done when

You pass the diagnostic or repair every failed category, can solve unfamiliar medium SQL problems without tutorials, and can explain correctness checks for each flagship query.

## Next

[Module 02 — Dimensional Modeling & Warehousing](../02-dimensional-modeling-and-warehousing/README.md)
