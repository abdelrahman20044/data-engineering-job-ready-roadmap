# L05 · API Ingestion, ETL & Incremental Loads

| Tier | Time | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| 2 · Build Reliable Pipelines | 24 hours | ●●●○○ | L03, L04 | L06, L08 |

## What you will learn

Build a rerunnable batch pipeline from a public API into raw, staging and warehouse layers. Make extraction bounded, transformations explicit and loading incremental rather than writing a one-off script.

## Topics and learning resources

| Order | Topic | Primary resource | Arabic / alternative | Action |
|---:|---|---|---|---|
| 1 | HTTP extraction | [Requests quickstart](https://requests.readthedocs.io/en/latest/user/quickstart/) | Garage Education ETL use-case material | Implement timeouts, pagination, status handling and bounded retries |
| 2 | Raw landing and contracts | Project API docs + *Fundamentals of Data Engineering*, Ch. 7 pp. 235–247 | — | Preserve raw input and document the expected schema |
| 3 | Transform and load | *Building ETL Pipelines with Python*, Ch. 4 pp. 47–52 and Ch. 6 pp. 72–76 | Garage Education / Seattle Data Guy selected lessons | Separate pure transforms from I/O and load transactionally |
| 4 | Incremental state | [PostgreSQL `INSERT`](https://www.postgresql.org/docs/current/sql-insert.html) | — | Use a watermark or source key plus upsert strategy |
| 5 | Idempotency and recovery | *Fundamentals of Data Engineering*, Ch. 7 pp. 250–257 | — | Rerun the same interval without duplicate effects |
| 6 | Reconciliation and drift | Project checks | — | Compare input/output/reject counts and quarantine invalid records |
| 7 | Secrets and configuration | [Twelve-Factor config](https://12factor.net/config) | — | Remove credentials and environment choices from code |

## Practice

- Extract multiple pages with explicit connect/read timeouts.
- Persist raw responses or records with run and interval metadata.
- Implement an incremental load and prove identical reruns do not duplicate rows.
- Inject an HTTP failure, malformed record and database failure; record expected behavior.
- Reconcile extracted, accepted, rejected and loaded counts.

## Project application

Implement the flagship path: `API → raw landing → validated staging → dimensional PostgreSQL warehouse`. Commit a run command, state strategy and rerun demonstration.

## Interview check

Explain ETL vs ELT, batch boundaries, full vs incremental loads, watermark limitations, idempotency, retries vs duplicates, upserts, schema drift and reconciliation.

## Completion criteria

- [ ] Extraction handles pagination, timeouts and non-success responses.
- [ ] Raw data is preserved before destructive transformation.
- [ ] Incremental state and rerun behavior are documented and tested manually.
- [ ] Counts reconcile and invalid rows have a visible policy.

## Next

Continue to [L06 · Testing & Data Quality](../06-testing-data-quality/README.md).

Books, alternatives and later patterns are in [`resources.md`](resources.md).
