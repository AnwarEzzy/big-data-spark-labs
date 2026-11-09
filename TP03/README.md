# TP03 — Spark SQL and DataFrames

**Anwar Ezzirani — G4 — 5IIR Data Science & AI**

## Deliverables

- [Executed Jupyter notebook](TP3.ipynb): all 22 questions, code, saved results, explanations, and embedded Spark UI screenshots.
- [PDF report](Compte_rendu_TP3_Anwar_Ezzirani_G4.pdf): an export of the completed and executed notebook.
- [Assignment](TP_3SparkSQL_DataFrames.pdf): the original instructions supplied by Pr Fadwa FATHI.

The notebook and report are written in French. The initial work on parts 0–2 is retained and expanded; parts 3–6 complete the assignment.

## Topics covered

- SparkSession configuration and ANSI SQL conversion behavior.
- DataFrames created from Python lists, with inferred and explicit schemas.
- JSON and CSV readers, including the generic `format(...).load(...)` API.
- Projections, filters, conditional columns, aggregation, and sorting.
- SQL queries, local and global temporary views, and session isolation.
- Equivalent DataFrame and SQL execution plans.
- RDD-to-DataFrame conversions and access to `Row` fields.

## Main results

| Department | Employees | Average salary, rounded (MAD) | Maximum salary (MAD) |
| --- | ---: | ---: | ---: |
| Finance | 3 | 11,667 | 13,500 |
| Informatique | 3 | 13,833 | 16,500 |
| RH | 2 | 9,500 | 10,200 |

The dataset contains 8 employees, with total monthly salaries of 95,500 MAD and an overall average of 11,937.50 MAD. The three highest-paid employees are Youssef, Sara, and Anas.

## Execution and validation

The notebook runs on Apache Spark 4.0.0 in Docker with Python 3.13.5, Java 17, `local[*]`, and `spark.sql.shuffle.partitions = 4`. Its application name remains `TP1 - Spark SQL`, as requested in the TP03 assignment.

All 25 code cells are executed. Assertions check the results, including an independent Python reference for department statistics and salary ranking. The invalid ANSI cast and the inaccessible local view in a new session are intentional, caught exceptions.

The notebook embeds three genuine Spark UI screenshots: SQL executions, an aggregation execution plan, and stages. The saved notebook and PDF can be viewed without running Spark.

## Reproduce

Open `TP3.ipynb` in JupyterLab with PySpark 4.0.0 and Java 17, then run all cells from a fresh kernel. Input files are created automatically in the relative `data_tp1/` directory. Temporary views are created with replacement to allow repeated execution.

The embedded screenshots document the submitted execution. Generating new screenshots requires a browser connected to the current Spark UI. Local build scripts, temporary data, and execution evidence are excluded from Git; the submitted notebook contains the saved screenshots and outputs.
