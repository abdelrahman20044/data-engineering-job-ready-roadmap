# L07 · Git, Docker & Reproducible Delivery

| Tier | Time | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| 2 · Build Reliable Pipelines | 12 hours | ●●○○○ | L04–L06 | L08, active application milestone |

## What you will learn

Package the pipeline so another person can review, run and recover it. Use Git deliberately, containerize only the required services, and automate one high-value verification step.

## Topics and learning resources

| Order | Topic | Primary resource | Arabic / alternative | Action |
|---:|---|---|---|---|
| 1 | Git diagnostic and recovery | [Learn Git Branching](https://learngitbranching.js.org/) | Kube-ops Git material | Practise branches, rebase, reset/revert and conflict resolution |
| 2 | Reviewable history | [Pro Git](https://git-scm.com/book/en/v2) selected chapters | — | Clean `.gitignore`, secrets and commit messages; open a self-review PR |
| 3 | Images and Dockerfiles | [Docker get started](https://docs.docker.com/get-started/) | TechWorld with Nana / Kube-ops Docker material | Build a small non-secret image with cached layers |
| 4 | Compose and service readiness | [Docker Compose how-tos](https://docs.docker.com/compose/) | Same Arabic alternative | Start app + PostgreSQL with health checks and persistent volume |
| 5 | Linux shell gap-only | [The Missing Semester: shell](https://missing.csail.mit.edu/2020/course-shell/) | — | Write repeatable inspect/run commands; no broad Linux course |
| 6 | Minimal CI | [GitHub Actions: Python](https://docs.github.com/en/actions/use-cases-and-examples/building-and-testing/building-and-testing-python) | — | Run formatting/lint only if used, plus tests on push/PR |

## Practice

- Recover a discarded-looking commit with `reflog` in a throwaway repo.
- Build the image twice and explain cache behavior.
- Prove `docker compose up` works from documented steps on a clean checkout.
- Break a health check or environment variable and improve the runbook.

## Project application

Add `Dockerfile`, `compose.yaml`, `.env.example`, health checks, persistent storage, clean setup commands and a small test workflow to the flagship.

## Interview check

Explain merge vs rebase, revert vs reset, image vs container, layers, bind mounts vs volumes, Compose readiness, environment secrets and what CI protects.

## Completion criteria

- [ ] Git history and repository ignore rules are reviewable.
- [ ] A clean checkout starts with documented commands.
- [ ] Tests run in CI.
- [ ] No credentials or generated data are committed.
- [ ] The [application milestone](../docs/application-milestone.md) is satisfied.

## Next

Begin a consistent application cadence, then continue to [L08 · Airflow & Orchestration](../08-airflow-orchestration/README.md).

Alternative learning paths are in [`resources.md`](resources.md).
