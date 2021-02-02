# Benchmarking Performance of Hyperparameter Tuning for Tree-based Algorithms

The goal of this project is to tune hyperparameters for Ensemble based Learning methods and to compare the performance of Python’s scikit-learn library with PySpark’s ML Library.

## Evaluated Systems
1. Local machine: The local machine used is a 2020 MacBook Pro with 16GB RAM, Quad-core and 512GB SSD.
2. Databricks : A Standard Edition Databricks account was used to test the performance of Apache Spark’s PySpark library. Performance was captured by varying the number of worker nodes.

## Problem Statement
Through analysis, the following questions are answered:

*Part 1: On Local Machine*

  - How does Python vs PySpark perform for basic data loading using data stored locally?
  - How does Python vs PySpark perform for data imputation tasks?
  - How does the performance of Python vary as we tune hyperparameters using a Grid Search and Random Search for a Random Forest Model and a Gradient Boosted Tree Model?
  - How does performance of PySpark vary as we tune hyperparameters using Cross Validation and Train Validation techniques for a Random Forest Model and a Gradient Boosted Tree Model?
  - How does the performance of Python vs PySpark vary with change in the size of the
dataset?

*Part 2: On Databricks*

  - How does PySpark perform for basic data loading with data stored on an S3 bucket?
- How does PySpark perform for data imputation tasks?
- How does PySpark perform as we vary hyperparameters using Cross Validation and Train Validation techniques for a Random Forest Model and Gradient Boosted Model?
- How does PySpark perform for the conditions listed above when we vary the number of worker nodes from 2 vs 4 vs 8?

## Methodology

### Dataset:
The dataset used is the [US College Scorecard](https://collegescorecard.ed.gov/) data that was released by the US Department of Education. College Scorecard provides a publicly available data set consisting of approximately 2000 metrics for 7805 degree-granting institutions. These metrics include demographic data, test scores, family income data, data about the percentages of students in each major, financial aid information, debt and debt repayment values, earnings of alumni  everal years after graduation, and more.

The goal of this project was to build a model that would accurately predict the earnings of a college's graduates after ten years based on the specific features.
To perform this regression task, the response variable used is: **mn_earn_wne_p10: Median earnings of students working and not enrolled 10 years
after entry.**
