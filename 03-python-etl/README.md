# Module 03 — Python ETL

## Why this matters

Python appeared in about 93% and ETL/ELT in about 86% of the early-career sample. The target is not generic Python fluency; it is a maintainable, rerunnable batch pipeline.

## Prerequisites

Modules 01–02, Python fundamentals, basic APIs, and a working PostgreSQL warehouse schema.

## Outcome

You can structure a Python project, call an API safely, land raw data, transform it explicitly, and load PostgreSQL incrementally without creating duplicates on rerun.

## Diagnostic gate

In 75 minutes, without a tutorial, write a small program that:

1. reads a JSON file;
2. validates required fields;
3. transforms records with functions;
4. writes a CSV/JSON result;
5. handles one expected error;
6. has a clear `main()` entry point.

If successful, skip beginner Python syntax. Repair only diagnosed gaps using the official [Python tutorial](https://docs.python.org/3/tutorial/).

## Topic path

### 1. Project structure, functions, types, and configuration

**Learn / reference**

- [Packaging Python Projects](https://packaging.python.org/tutorials/packaging-projects/) for `src/`, `pyproject.toml`, imports, and installable development.
- [Writing `pyproject.toml`](https://packaging.python.org/en/latest/guides/writing-pyproject-toml/).

**Read**

- *Fundamentals of Data Engineering*: Ch. 2 pp. 33–48 and 59–68 for lifecycle/context—not code recipes.

**Practice**

- Refactor the diagnostic into small typed functions with no hidden global configuration.

**Apply**

- Create the flagship Python package, `.env.example`, configuration boundary, CLI/entry point, and dependency definition. Never commit secrets.

### 2. Robust API extraction

**Learn**

- [Requests Quickstart](https://requests.readthedocs.io/en/latest/user/quickstart/) for parameters, JSON, errors, and explicit timeouts.
- [Requests advanced usage](https://requests.readthedocs.io/en/master/user/advanced/) for sessions and retry-aware adapters.

**Read**

- *Building ETL Pipelines with Python*: Ch. 4 pp. 47–52 and Ch. 6 pp. 72–76. Use the patterns conceptually; verify library APIs against current docs.

**Practice**

- Call a public API with parameters, pagination, a timeout, status checking, and a deliberate failure. Save one raw response exactly as received.

**Apply**

- Implement `extract.py` with bounded retries for transient failures, explicit timeouts, useful exceptions, and raw landing organized by extraction date/run.

### 3. Transformation boundaries and schema handling

**Learn / reference**

- [Python `datetime`](https://docs.python.org/3/library/datetime.html), [`decimal`](https://docs.python.org/3/library/decimal.html), and [`json`](https://docs.python.org/3/library/json.html) only as needed.

**Practice**

- Normalize timestamps/time zones, parse numeric values safely, define required/optional fields, and quarantine one malformed record.

**Apply**

- Keep pure transformation functions separate from network/database code. Produce staging-shaped records and document source-to-target mappings.

### 4. Incremental loading and idempotency

**Learn / read**

- *Fundamentals of Data Engineering*: Ch. 7 pp. 235–247 and 250–257; Ch. 8 pp. 309–323.
- PostgreSQL [transactions tutorial](https://www.postgresql.org/docs/current/tutorial-transactions.html) and [`INSERT ... ON CONFLICT`](https://www.postgresql.org/docs/current/sql-insert.html).

**Practice**

- On a toy table, compare append, delete-and-reload, and upsert for the same input interval. Run each twice and inspect counts/state.

**Apply**

- Choose an incremental boundary (watermark, source cursor, or time interval), persist state safely, load within transactions, and prove that rerunning the same interval is harmless.

### 5. Database loading and failure handling

**Learn / reference**

- [Psycopg 3 basic usage](https://www.psycopg.org/psycopg3/docs/basic/usage.html) for parameters, transactions, and context managers.
- [Python logging HOWTO](https://docs.python.org/3/howto/logging.html).

**Practice**

- Simulate a mid-load failure. Confirm the transaction rolls back and the next run succeeds.

**Apply**

- Log run ID/interval, source count, valid/rejected count, inserted/updated count, duration, and the failure point—without logging secrets or full sensitive payloads.

## Module practice

- [ ] Diagnostic passed or gaps repaired.
- [ ] Pagination and timeout demonstrated.
- [ ] Malformed record quarantined with a useful reason.
- [ ] Same interval run twice with stable target state.
- [ ] Database failure rolls back cleanly.

## Build

Flagship Phase 2, first half: a command-driven API → raw → staging → warehouse pipeline. Keep orchestration out; a local command should run one explicit interval.

## Interview check

Explain without notes:

1. ETL vs ELT in the context of your project.
2. Idempotency and how your pipeline achieves it.
3. Full refresh vs incremental load.
4. Timeout vs retry and which errors should not be retried.
5. Why transformation logic is separated from I/O.
6. What happens if loading fails halfway through.

## Evidence

Package structure, extraction/transform/load code, sample raw input, source-to-target mapping, rerun proof, logs, and small commits in the flagship project.

## Done when

A documented command runs a chosen interval end-to-end, a second run does not corrupt/duplicate data, and you can diagnose a failed run from logs.

## Next

[Module 04 — Testing, Data Quality & Delivery](../04-testing-quality-delivery/README.md)
