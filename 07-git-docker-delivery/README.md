# L07 · Git, Docker & Reproducible Delivery

| Tier | Time | Difficulty | Prerequisites | Unlocks |
|---|---:|---|---|---|
| 2 · Build Reliable Pipelines | 12 hours | ●●○○○ | L04–L06 | L08, active application milestone |

## What you will learn

Package the pipeline so another person can review, run and recover it. Use Git deliberately, containerize only the required services, and automate one high-value verification step.

## Topics and learning resources

| Order | Topic | Primary resource | Arabic / alternative | Action |
|---:|---|---|---|---|
| 1 | Git diagnostic and recovery | [Learn Git Branching](https://learngitbranching.js.org/) | [Arabic Git/GitHub course](https://www.youtube.com/playlist?list=PLMTdZ61eBnypdpBVn2kb-2yizuEL7Phyj) — gap-only | Practise branches, rebase, reset/revert and conflict resolution |
| 2 | Reviewable history | [Pro Git: basics](https://git-scm.com/book/en/v2/Git-Basics-Undoing-Things), [branching/rebase](https://git-scm.com/book/en/v2/Git-Branching-Rebasing) + [commit guide](https://cbea.ms/git-commit/) | [GitHub Skills](https://skills.github.com/) | Clean `.gitignore`, secrets and commits; open a self-review PR |
| 3 | Images and Dockerfiles | [Docker Python guide](https://docs.docker.com/guides/python/) + [build best practices](https://docs.docker.com/build/building/best-practices/) | [Arabic Docker course](https://www.youtube.com/watch?v=PrusdhS2lmo) — watch only through Compose | Build a small non-secret image; explain build context, layers and cache |
| 4 | Compose, storage and networking | [Docker Compose quickstart](https://docs.docker.com/compose/gettingstarted/) + [startup order](https://docs.docker.com/compose/how-tos/startup-order/) | Same Arabic alternative | Start app + PostgreSQL with network, health check and persistent volume |
| 5 | Linux shell gap-only | [The Missing Semester: shell](https://missing.csail.mit.edu/2020/course-shell/) | — | Write repeatable inspect/run commands; no broad Linux course |
| 6 | Minimal CI | [GitHub Actions: Python](https://docs.github.com/en/actions/use-cases-and-examples/building-and-testing/building-and-testing-python) | — | Run formatting/lint only if used, plus tests on push/PR |

## Practice

- Recover a discarded-looking commit with `reflog` in a throwaway repo.
- Build the image twice and explain cache behavior.
- Compare a bind mount with a named volume and explain which project data should persist.
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
