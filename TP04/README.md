# TP04 — E-commerce Sales Analysis with Spark SQL

**Anwar Ezzirani — G4 — 5IIR Data Science & AI**

## Deliverables

- [Executed Jupyter notebook](TP4_Anwar_Ezzirani_G4.ipynb): all 29 questions, code, results, explanations, screenshots, and charts.
- [PDF report](Compte_rendu_TP4_Anwar_Ezzirani_G4.pdf): export of the completed and executed notebook.
- [Final CSV report](Rapport_CA_TP4_Anwar_Ezzirani_G4.csv): revenue by category and month, with a header and 36 data rows.
- [Assignment](TP4_SparkSQL_Analyse_Ventes.docx): the original instructions and reproducible data generator.

The notebook and report are written in French.

## Topics covered

- Explicit schemas, data quality audits, and safe ANSI-mode conversions.
- Duplicate removal, missing values, text normalization, and price imputation.
- SQL and DataFrame joins, revenue aggregation, and customer segmentation.
- Window functions: category rankings, cumulative revenue, and monthly variations.
- Catalyst predicate pushdown, broadcast joins, and measured cache performance.
- Partitioned Parquet, partition pruning, and a single-file CSV export.

## Key results

| Metric | Result |
| --- | ---: |
| Raw order rows | 3,040 |
| Exact duplicate rows | 40 |
| Clean orders | 2,949 |
| Delivered orders contributing to revenue | 2,089 |
| Total delivered revenue | 1,215,123.00 MAD |
| Imputed price for Casque | 149.00 MAD |
| Customers without a clean order | 6 |
| Best month | January 2025 — 118,017.00 MAD |

Only delivered orders contribute to revenue. Prices and amounts use decimal types. Customer segmentation groups by customer ID to preserve distinct customers with the same name; it includes customers with delivered sales.

## Execution and validation

Environment: Apache Spark 4.0.0, Python 3.13.5, Java 17, Docker, `local[*]`, and 8 SQL shuffle partitions. The container exposes four processors. The application name `TP2 - Ventes` and directories `data_tp2` and `out_tp2` follow the TP04 assignment.

The notebook contains 31 executed code cells. Assertions compare Spark results with an independent Python implementation reading the original CSV and JSON files. Validation covers cleaning, revenue totals, cities, categories, months, products, customer segments, window calculations, and the exported CSV.

Four genuine Spark UI screenshots document SQL executions, a broadcast join, stages, and materialized sales in Storage. Cache measurements contain three runs before caching and three runs after materialization; they describe this small execution and are not a general performance benchmark.

## Reproduce

Open the notebook in a fresh PySpark 4.0.0 kernel with Java 17 and run every cell. The assignment's original generator creates the input files using seed 42. Parquet and CSV outputs under `out_tp2/` are written in overwrite mode. The standalone CSV deliverable is copied directly from Spark's single output CSV file.

The saved notebook and PDF include all outputs and screenshots and can be read without running Spark. Regenerating Spark UI screenshots requires a browser connected to the active application. Local build scripts, temporary files, generated data, and intermediate Parquet outputs are excluded from Git.
