# L04 · Python for Data Engineering

| Tier | Time | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| 2 · Build Reliable Pipelines | 14 hours | ●●○○○ | Existing programming experience | L05, L06 |

## What you will learn

Turn existing Python knowledge into maintainable pipeline code. Skip beginner syntax and focus on structure, interfaces, errors, configuration, logging and database transactions.

## Topics and learning resources

| Order | Topic | Primary resource | Arabic / alternative | Action |
|---:|---|---|---|---|
| 1 | Gap diagnostic | [Exercism Python track](https://exercism.org/tracks/python) | Corey Schafer gap-only videos | Solve 3–5 exercises; list language gaps, not all topics |
| 2 | Project structure and environments | [Python Packaging User Guide](https://packaging.python.org/en/latest/tutorials/packaging-projects/) | Kiwilytics Python material if a specific explanation is needed | Create `pyproject.toml`, package layout and reproducible commands |
| 3 | Iteration and resource safety | [Python functional HOWTO](https://docs.python.org/3/howto/functional.html) and [`contextlib`](https://docs.python.org/3/library/contextlib.html) | — | Stream records and close files/connections safely |
| 4 | Configuration and interfaces | [`argparse`](https://docs.python.org/3/library/argparse.html), [`dataclasses`](https://docs.python.org/3/library/dataclasses.html) | — | Add CLI parameters and environment-based configuration |
| 5 | Errors and logging | [Python logging HOWTO](https://docs.python.org/3/howto/logging.html) | Corey Schafer targeted videos | Replace prints/silent failures with useful exceptions and logs |
| 6 | PostgreSQL connectivity | [Psycopg basic usage](https://www.psycopg.org/psycopg3/docs/basic/usage.html) | — | Use parameterized SQL and explicit transaction boundaries |

## Practice

- Refactor one small script into importable functions plus a thin CLI.
- Add type hints to public interfaces and focused docstrings where decisions are non-obvious.
- Process a file through a generator rather than loading everything at once.
- Demonstrate a database transaction that rolls back cleanly on failure.

## Project application

Create the flagship package skeleton, configuration loader, CLI, structured logging and database connection layer. Do not build ETL behavior until L05.

## Interview check

Explain modules vs packages, iterators vs lists, context managers, exception boundaries, dependency/environment reproducibility, parameterized queries and transaction scope.

## Completion criteria

- [ ] Package installs and commands run from a clean environment.
- [ ] Configuration and secrets are separated from code.
- [ ] Logs and exceptions identify the failing operation.
- [ ] Database access is parameterized and transactional.

## Next

Continue to [L05 · API Ingestion, ETL & Incremental Loads](../05-etl-api-incremental-loads/README.md).

Gap-only alternatives and references are in [`resources.md`](resources.md).
