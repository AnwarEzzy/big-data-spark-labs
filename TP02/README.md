# TP02 — Apache Spark Core: RDDs and Sales Analysis

**Anwar Ezzirani — G4 — 5IIR Data Science & AI**

## Deliverables

- [Executed Jupyter notebook](TP2_Anwar_Ezzirani_G4.ipynb): all exercises, code, outputs, explanations, and embedded screenshots.
- [PDF report](Compte_rendu_TP2_Anwar_Ezzirani_G4.pdf): an 18-page export of the executed notebook, including results, charts, and actual Spark UI screenshots.

The report and explanations are written in French.

## Topics covered

- Data loading, cleaning with `flatMap`, and caching.
- Key-value aggregations, sorting, and shuffle comparison.
- Inner and outer joins, and `cogroup`.
- Set operations, Cartesian products, and `zip`.
- Partitioning and saving results.
- Business analysis of sales by product, city, and month.

## Execution

The notebook was executed with Apache Spark 4.0.0, Python 3.13.5, and Java 17.0.16 in Docker, using `local[4]`.
All 27 code cells completed successfully. The two intentional `zip` errors required by the assignment are caught and explained.

The notebook creates its input dataset from the data supplied in the assignment. Its saved outputs and images can be viewed without running Spark. To rerun it, use a Python kernel with PySpark 4.0.0 and Java 17. The embedded screenshots document the submitted execution; generating new Spark UI screenshots requires a separate browser capture step.

## Key results

| Metric | Result |
| --- | ---: |
| Valid sales | 19 |
| Rejected records | 3 |
| Total revenue | 173,750 MAD |
| Best-selling product by quantity | Souris — 65 units |
| City with the highest average sale amount | Marrakech — 16,200 MAD |
| January 2025 revenue | 129,200 MAD |
| February 2025 revenue | 44,550 MAD |
