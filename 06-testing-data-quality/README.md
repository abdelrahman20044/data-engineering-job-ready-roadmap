# L06 · Testing & Data Quality

| Tier | Time | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| 2 · Build Reliable Pipelines | 16 hours | ●●●○○ | L05 | L07, application milestone |

## What you will learn

Prove pipeline behavior with focused unit/integration tests, explicit data checks, useful run metadata and controlled failure experiments. Learn the checks before adopting a large quality framework.

## Topics and learning resources

| Order | Topic | Primary resource | Arabic / alternative | Action |
|---:|---|---|---|---|
| 1 | pytest essentials | [pytest getting started](https://docs.pytest.org/en/stable/getting-started.html) | — | Test a pure transformation with clear assertions |
| 2 | Fixtures and parametrization | [pytest fixtures](https://docs.pytest.org/en/stable/how-to/fixtures.html) and [parametrize](https://docs.pytest.org/en/stable/how-to/parametrize.html) | — | Cover valid, boundary and invalid records |
| 3 | Test boundaries | *Building ETL Pipelines with Python*, Ch. 13 pp. 169–181 | — | Separate unit, integration and external-contract tests |
| 4 | Data-quality dimensions and rules | Same book, Ch. 14 pp. 185–195 | Selected Great Expectations concepts only | Map completeness, validity, uniqueness, consistency, timeliness and accuracy risks to concrete checks |
| 5 | Contract and integration checks | Project schema + PostgreSQL | — | Verify schema, database constraints, atomic loads and same-interval idempotency at real boundaries |
| 6 | Observability basics | Python logging + project run metadata | — | Log run ID, interval, counts, duration and failure point |
| 7 | Failure recovery | Project experiments | — | Inject failures and prove cleanup/restart behavior |

## Practice

- Test transformation functions on tiny readable fixtures.
- Run an integration test against an isolated PostgreSQL instance/schema.
- Add at least five critical checks covering multiple quality dimensions and make one fail deliberately.
- Save a short failure/recovery note with relevant log excerpts.

## Project application

Add `tests/`, `sql/quality/`, rejected-record handling and run metadata to the flagship. Evidence must include passing tests and one controlled failure.

## Interview check

Explain unit vs integration vs contract tests, fixture scope, what to mock, six quality dimensions, why row counts are insufficient, fail-fast vs quarantine and how you test idempotency.

## Completion criteria

- [ ] Critical transforms have unit tests.
- [ ] One real database boundary is tested.
- [ ] Core schema/content/relationship checks exist.
- [ ] Failure and recovery behavior are demonstrated.

## Next

Continue to [L07 · Git, Docker & Reproducible Delivery](../07-git-docker-delivery/README.md).

Alternatives and framework boundaries are in [`resources.md`](resources.md).
