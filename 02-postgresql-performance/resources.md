# L02 Resources · PostgreSQL & Performance

## Recommended path

1. PostgreSQL constraint and transaction documentation.
2. [Use The Index, Luke!](https://use-the-index-luke.com/) for the index mental model.
3. PostgreSQL `EXPLAIN` documentation applied to one project query.

## Arabic / Egyptian

- Tech Vault database-storage and database-design lessons, when available in the referenced roadmap: useful conceptual clarification before reading a real plan.
- If an Arabic explanation conflicts with current PostgreSQL output, trust the current PostgreSQL documentation and measured plan.

## English alternatives

- [CMU 15-445/645 Database Systems](https://15445.courses.cs.cmu.edu/) — selected lectures on storage, indexes and query execution; deeper than required.
- [PostgreSQL Indexes](https://www.postgresql.org/docs/current/indexes.html) — authoritative but best used by question, not linearly.

## Practice / labs

- Use `generate_series` to create enough local data for a visible plan difference.
- Compare no index, single-column index and one defensible composite index.
- Change selectivity and observe when the planner changes scan strategy.

## Reference

- [`EXPLAIN`](https://www.postgresql.org/docs/current/sql-explain.html)
- [Planner statistics](https://www.postgresql.org/docs/current/planner-stats.html)
- [Routine vacuuming](https://www.postgresql.org/docs/current/routine-vacuuming.html)

## Later / skip

- Later: buffer internals, MVCC implementation detail, advanced locks and production server tuning.
- Skip: memorizing configuration knobs, speculative indexes, and DBA certification material.
