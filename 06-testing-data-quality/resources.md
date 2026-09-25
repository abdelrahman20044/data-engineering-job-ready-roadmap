# L06 Resources · Testing & Data Quality

## Recommended path

Use pytest documentation plus the audited ETL-book chapters, then write checks against the flagship. The project’s failure modes determine the test plan.

## Arabic / Egyptian

No Arabic resource is assigned as primary. Use an Arabic pytest explanation only for a specific blocker; verify APIs against current pytest documentation.

## English alternatives

- [pytest documentation](https://docs.pytest.org/en/stable/)
- [Great Expectations documentation](https://docs.greatexpectations.io/) — optional after explicit checks are understood.
- [dbt data tests](https://docs.getdbt.com/docs/build/data-tests) — reference only if dbt is later triggered.

## Audited book sections

- *Building ETL Pipelines with Python*, Ch. 13 pp. 169–181.
- *Building ETL Pipelines with Python*, Ch. 14 pp. 185–195.

## Practice / labs

- Parametrize transformations with null, duplicate, malformed and boundary records.
- Test a failed transaction leaves no partial warehouse state.
- Add accepted-value and referential-integrity checks in SQL.
- Record `input = accepted + rejected` for each run.

## Reference

- [Python logging cookbook](https://docs.python.org/3/howto/logging-cookbook.html)
- [Great Expectations concepts](https://docs.greatexpectations.io/docs/core/introduction/)

## Later / skip

- Later: Great Expectations, Soda, Monte Carlo and enterprise observability only if a job/project needs them.
- Skip creating a generic test framework; prove project behavior with the smallest useful suite.
- Do not mock PostgreSQL out of every test—the database contract matters.
