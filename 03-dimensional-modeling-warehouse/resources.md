# L03 Resources · Dimensional Modeling & Warehousing

## Recommended path

Use *The Data Warehouse Toolkit*, 3e as the primary decision guide, but read only when the corresponding modeling decision is due.

### Read now

- Ch. 1 pp. 7–22
- Ch. 2 pp. 37–57
- Ch. 3 pp. 70–79 and 98–104
- Ch. 5 pp. 147–154

## Arabic / Egyptian

- [Garage Education: DWH Modelling](https://www.youtube.com/playlist?list=PLxNoJq6k39G_Ffv8Na1oRbob0sVHfFc_T) — select the lessons on grain, facts/dimensions, star schemas and SCDs; do not watch unrelated material linearly.
- [Tech Vault: OLTP vs OLAP](https://www.youtube.com/watch?v=LU8pfUrdXWE) — use for the initial contrast, then return to the project decision.

## English alternatives

- [Kimball dimensional-modeling techniques](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/kimball-techniques/dimensional-modeling-techniques/) — concise authoritative reference.
- [Kimball dimensional-modeling techniques summary (PDF)](https://www.kimballgroup.com/wp-content/uploads/2013/08/2013.09-Kimball-Dimensional-Modeling-Techniques11.pdf) — direct quick reference for fact-table types, dimensional patterns and SCDs.
- *Fundamentals of Data Engineering*, Ch. 2 pp. 33–48 and 59–68 — architecture/lifecycle reference, not a modeling textbook.

## Practice

- Model the same business process at two grains and explain which questions each permits.
- Classify at least five measures by additivity.
- Simulate one attribute correction (Type 1) and one historical change (Type 2).
- Run orphan, duplicate-natural-key and overlapping-effective-date checks.

## Reference

- [Kimball Group techniques](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/kimball-techniques/)
- [PostgreSQL constraints](https://www.postgresql.org/docs/current/ddl-constraints.html)

## Later / skip

- Read later only if the project needs them: Ch. 4 pp. 111–122 and Ch. 6 pp. 167–199.
- Later: bridges, multi-valued dimensions, advanced hierarchies and enterprise bus design. Accumulating snapshots are understood conceptually now but implemented only if the project process has milestones.
- Skip outdated product-specific implementation advice; preserve the modeling principle and implement with current PostgreSQL.
- Do not invent junk/bridge/mini-dimensions merely to show vocabulary.
