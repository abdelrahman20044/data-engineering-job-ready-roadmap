# L11 Resources · Spark Performance

## Recommended path

Use *Learning Spark* Ch. 7 for the first mental model, then the current Spark tuning guide and one measured project experiment.

## Arabic / Egyptian

- Garage Education selected lessons on partitions, shuffles and optimization.
- Use the Arabic lesson to build intuition, then verify the plan and UI yourself.

## English alternatives

- Data Engineering Zoomcamp’s Spark UI/performance material.
- Databricks performance talks on join strategies and Adaptive Query Execution—select by problem.
- [The Internals of Spark SQL](https://books.japila.pl/spark-sql-internals/) by Jacek Laskowski — deep reference, not the learning path.

## Audited book sections

- *Learning Spark*, 2e: Ch. 7 pp. 183–205.

## Practice / labs

- Broadcast vs shuffled join on a small dimension.
- Too many tiny partitions vs fewer meaningful partitions.
- Cache a reused result, then remove the cache and compare.
- Add a skewed key only if you can explain the experiment.

## Reference

- [Spark SQL performance tuning](https://spark.apache.org/docs/latest/sql-performance-tuning.html)
- [Spark web UI](https://spark.apache.org/docs/latest/web-ui.html)
- [PySpark `explain`](https://spark.apache.org/docs/latest/api/python/reference/pyspark.sql/api/pyspark.sql.DataFrame.explain.html)

## Later / skip

- Later: AQE internals, custom partitioners, memory management internals and cluster sizing.
- Skip lists of tuning knobs without a measured bottleneck.
