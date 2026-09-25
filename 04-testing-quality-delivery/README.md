# Module 04 — Testing, Data Quality & Reproducible Delivery

## Why this matters

Testing/data quality appeared in about 45% of early-career postings, while Git, Docker, Linux, and operational discipline recur as supporting engineering skills. Together they turn a script into credible portfolio evidence.

## Prerequisites

Module 03 pipeline runs locally for one interval.

## Outcome

You can test transformation/load behavior, enforce critical data expectations, debug failures, and start the complete local platform reproducibly with Docker Compose.

## Topic path

### 1. Unit and integration tests with pytest

**Learn**

- [pytest Get Started](https://docs.pytest.org/en/stable/getting-started.html): assertions, discovery, fixtures, and failure output.
- [Parametrization](https://docs.pytest.org/en/stable/how-to/parametrize.html).

**Read**

- *Building ETL Pipelines with Python*: Ch. 13 pp. 169–181.

**Practice**

- Test a pure transform with normal, boundary, null, and malformed inputs.
- Use one database fixture for a load/idempotency integration test.

**Apply**

- Add fast unit tests for transformations and focused integration tests for transactions/upserts. Do not mock the logic being tested.

### 2. Data-quality contracts

**Learn / reference**

- [Great Expectations — data-quality use cases](https://docs.greatexpectations.io/docs/reference/learn/data_quality_use_cases/dq_use_cases_lp/) for schema, uniqueness, integrity, freshness, volume, and distribution concepts.

**Practice**

- Express critical expectations first as plain SQL/Python checks: schema, not-null, uniqueness, accepted values/ranges, referential integrity, freshness, and plausible volume.

**Apply**

- Fail the pipeline on contract-breaking conditions; report warnings separately for non-blocking anomalies. Great Expectations itself is optional after the fundamentals are visible.

### 3. Debugging and observability

**Learn / reference**

- [Python logging HOWTO](https://docs.python.org/3/howto/logging.html).
- [Missing Semester — debugging and profiling](https://missing.csail.mit.edu/2020/debugging-profiling/) selectively for logs/debugging workflow.

**Practice**

- Inject a bad API response, database outage, and schema drift. For each, record signal → diagnosis → fix → prevention.

**Apply**

- Produce structured-enough logs with run/interval identifiers and counts. Add a concise `docs/runbook.md` for the three failure classes.

### 4. Docker and Docker Compose

**Learn**

- [Docker Get Started](https://docs.docker.com/get-started/) for image/container fundamentals.
- [Docker Compose Quickstart](https://docs.docker.com/compose/gettingstarted/) for services, health checks, volumes, logs, and debugging.

**Read**

- *Building ETL Pipelines with Python*: Ch. 14 pp. 185–195. Verify commands/configuration against current Docker docs.

**Practice**

- Containerize a minimal CLI, then connect it to PostgreSQL via Compose. Rebuild from a clean checkout.

**Apply**

- `docker compose up` must start PostgreSQL and the required local services; health checks prevent race-condition startup; data persistence and teardown are documented.

### 5. Git and Linux operating basics

**Diagnostic**

- Can you branch, make focused commits, inspect a diff/log, resolve a small conflict, use environment variables, pipes/redirection, permissions, processes, and log inspection? If yes, skip lessons and apply them.

**Gap resources**

- [Missing Semester — version control](https://missing.csail.mit.edu/2020/version-control/).
- [Missing Semester — shell tools and scripting](https://missing.csail.mit.edu/2020/shell-tools/).

**Apply**

- Use small meaningful commits; provide `.env.example`; add a `Makefile` or documented commands only if it reduces real repetition; never include secrets/generated data accidentally.

## Module practice

- [ ] One test fails for the intended reason before the fix.
- [ ] Unit, integration, and data-quality concerns are distinguished.
- [ ] The same interval can run twice inside the reproducible environment.
- [ ] A clean checkout starts from documented commands.
- [ ] Three injected failures are diagnosed through evidence, not guesswork.

## Build

Flagship Phase 2, professionalization: tests, quality gates, logs, Docker Compose, `.env.example`, README setup/commands, and a small failure runbook.

## Interview check

Explain without notes:

1. Unit vs integration vs data-quality tests.
2. What should fail the pipeline vs create a warning.
3. Fixture vs mock and where each appears in your tests.
4. Image vs container; volume vs bind mount.
5. Why a Compose health check matters.
6. How you diagnosed one real project failure.

## Evidence

Passing test output, deliberate failing case, quality checks, logs, `compose.yaml`, Dockerfile, clean-start instructions, and failure runbook.

## Done when

Another engineer can clone the flagship, start it from the README, run tests and one pipeline interval, observe useful logs, and reproduce a controlled failure.

## Application milestone

This is the main **active-application gate**. If Modules 01–04 have inspectable evidence, begin a consistent weekly application cadence while continuing the roadmap. See [`docs/application-milestone.md`](../docs/application-milestone.md).

## Next

[Module 05 — Airflow](../05-airflow/README.md)
