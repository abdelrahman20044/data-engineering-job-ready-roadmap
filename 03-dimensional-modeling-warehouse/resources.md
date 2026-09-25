# L03 Resources · Dimensional Modeling & Warehousing

## Recommended path

Use *The Data Warehouse Toolkit*, 3e as the primary decision guide, but read only when the corresponding modeling decision is due.

### Read now

- Ch. 1 pp. 7–22
- Ch. 2 pp. 37–57
- Ch. 3 pp. 70–79 and 98–104
- Ch. 5 pp. 147–154

## Arabic / Egyptian

- Garage Education’s data-warehouse playlist — use the sections on warehouse architecture, dimensional modeling, facts/dimensions and SCDs as an Arabic conceptual alternative.
- Tech Vault OLTP vs OLAP material — use for the initial contrast, then return to the project decision.

## English alternatives

- [Kimball dimensional-modeling techniques](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/kimball-techniques/dimensional-modeling-techniques/) — concise authoritative reference.
- [Data with Zach](https://www.youtube.com/@eczachly_) — selected modeling discussions for another perspective; do not substitute a long playlist for building.
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
- Later: accumulating snapshots, bridges, advanced hierarchies and enterprise bus design.
- Skip outdated product-specific implementation advice; preserve the modeling principle and implement with current PostgreSQL.
- Do not invent junk/bridge/mini-dimensions merely to show vocabulary.
