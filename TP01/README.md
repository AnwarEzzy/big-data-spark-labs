# TP01 — Apache Spark Core: RDD Fundamentals and Word Count

**Anwar Ezzirani — G4 — 5IIR Data Science & AI**

## Deliverables

- [Executed Jupyter notebook](TP1_RDD_Python.ipynb): Python and PySpark commands with saved execution outputs.
- [PDF report](Anwar_Ezzirani_Compte_Rendu_TP1_RDD_Python.pdf): a 21-page report with code, results, explanations, and screenshots.

The report and explanations are written in French. Both files are preserved from the original TP01 folder.

## Topics covered

- SparkSession, SparkContext, local execution, and Spark UI.
- Creating RDDs from Python collections and text files.
- Partitions, immutability, and lazy evaluation.
- Transformations: `map`, `filter`, `flatMap`, and `distinct`.
- Actions: `count`, `first`, `take`, `collect`, `reduce`, and numerical summaries.
- Word count with `reduceByKey` and top-word selection.
- Saving and reading distributed text outputs.

## Execution notes

The saved outputs identify Spark 4.0.0 with `local[4]`; notebook metadata identifies Python 3.13.5. The environment used JupyterLab in Docker.

All 29 non-empty code cells have execution counts, and the notebook contains no saved error outputs. One final code cell is empty. The PDF contains the execution screenshots.

The original answer to Q5.2 leaves the observed number of Spark jobs blank. The PDF explicitly identifies this value as still needing to be recorded from the original Spark UI session.

The saved results can be viewed without running Spark. Rerunning the notebook requires a compatible PySpark environment and adjustment of the `DATA` path if needed. The output directories used by `saveAsTextFile` must not already exist.
