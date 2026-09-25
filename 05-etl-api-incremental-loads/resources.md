# L05 Resources · ETL, APIs & Incremental Loads

## Recommended path

1. Requests and source API documentation for extraction behavior.
2. The audited *Building ETL Pipelines with Python* sections for implementation patterns.
3. PostgreSQL documentation plus a project-specific idempotency experiment.

## Arabic / Egyptian

- Garage Education ETL/data-warehouse use-case material — useful for an Arabic end-to-end explanation; adapt the pattern rather than copying its domain.

## English alternatives

- Seattle Data Guy’s selected ETL/pipeline videos — supplementary architecture discussion.
- [Data Engineering Zoomcamp](https://github.com/DataTalksClub/data-engineering-zoomcamp) — reuse a narrowly relevant ingestion/workflow lab only; do not take it as a second curriculum.
- *Fundamentals of Data Engineering*: Ch. 7 pp. 235–247 and 250–257; Ch. 8 pp. 309–323 as reference.

## Audited book sections

- *Building ETL Pipelines with Python*: Ch. 4 pp. 47–52 and Ch. 6 pp. 72–76 now.
- The same book’s Ch. 13–14 belong to L06, not this level.

## Practice / labs

- Use a public API with pagination and stable identifiers.
- Rerun the same window twice and compare table checksums/counts.
- Move one malformed item to a quarantine artifact with a reason.
- Restart after a simulated mid-load failure.

## Reference

- [Requests documentation](https://requests.readthedocs.io/)
- [Psycopg transactions](https://www.psycopg.org/psycopg3/docs/basic/transactions.html)
- [PostgreSQL `INSERT … ON CONFLICT`](https://www.postgresql.org/docs/current/sql-insert.html)

## Later / skip

- Later: CDC/Debezium when a target role or project genuinely needs change streams.
- Later: dbt when repeated target-job demand triggers L13.
- Skip microservice/event-bus architecture for this batch project.
