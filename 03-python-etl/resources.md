# Curated Resources — Python ETL

## Primary path

- [Packaging Python Projects](https://packaging.python.org/tutorials/packaging-projects/) — project structure.
- [Requests Quickstart](https://requests.readthedocs.io/en/latest/user/quickstart/) and [advanced usage](https://requests.readthedocs.io/en/master/user/advanced/) — HTTP extraction.
- [Psycopg 3 basic usage](https://www.psycopg.org/psycopg3/docs/basic/usage.html) — PostgreSQL parameters/transactions.
- Project experiments — incremental load and idempotency are learned by rerunning and breaking the flagship, not by passive reading.

## Just-in-time books

- *Building ETL Pipelines with Python*: Ch. 4 pp. 47–52; Ch. 6 pp. 72–76.
- *Fundamentals of Data Engineering*: Ch. 2 pp. 33–48 and 59–68; Ch. 7 pp. 235–247 and 250–257; Ch. 8 pp. 309–323.

## Reference

- [Python documentation](https://docs.python.org/3/).
- [Python logging HOWTO](https://docs.python.org/3/howto/logging.html).
- [PostgreSQL transactions](https://www.postgresql.org/docs/current/tutorial-transactions.html).

## Skip for now

- Relearning Python from variables and loops.
- Async ingestion, multiprocessing, framework-heavy connectors, or microservices before the batch pipeline is correct and rerunnable.
- Copying row-by-row ETL examples from older material without evaluating batch loading and current library APIs.
