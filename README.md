# Sampling and Sampling Error

## Project Overview

This project explains sampling, sampling methods, and different types of
errors that can occur when using a sample to understand a population. It
also uses Python to compare Simple Random Sampling and Stratified
Sampling and to study how sample size affects sampling error.

## Topics Covered

### 1. Sampling

Sampling is the process of collecting data from a representative subset
of a population instead of studying every individual.

### 2. Probability Sampling

-   **Simple Random Sampling:** Every individual has an equal chance of
    being selected.
-   **Stratified Random Sampling:** The population is divided into
    groups (strata), and individuals are randomly selected from those
    groups.
-   **Systematic Random Sampling:** Individuals are selected at regular
    intervals.
-   **Cluster Sampling:** The population is divided into clusters, and a
    subset of clusters is randomly selected.

**Advantages of probability sampling:** - Helps reduce sample bias. -
Represents different population characteristics. - Helps produce
accurate sample representations.

### 3. Non-Probability Sampling

The notebook also introduces non-probability sampling, where individuals
do not have an equal chance of selection.

### 4. Types of Errors in Sampling

-   **Sampling Error:** The difference between a sample estimate and the
    actual population value.
-   **Coverage Error:** Happens when some groups in the population are
    not properly represented.
-   **Nonresponse Error:** Happens when selected people do not respond
    to the survey.
-   **Measurement Error:** Happens when the measurement method or tool
    does not measure the correct value.

## Python Implementation

The notebook uses a synthetic population of 10,000 individuals. It
creates two groups (`low` and `high`) and generates income values using
NumPy.

It then: 1. Calculates the population mean. 2. Draws a Simple Random
Sample of 100 individuals. 3. Draws a proportional Stratified Sample
based on the two groups. 4. Calculates and compares the sample means and
their absolute errors against the population mean. 5. Repeats random
sampling for different sample sizes and plots the mean absolute sampling
error.

## Sampling Error vs Sample Size

The notebook tests these sample sizes:

`5, 10, 20, 50, 100, 200, 500, 1000`

For each sample size, it performs 500 repetitions and plots the mean
absolute sampling error. The notebook introduces the relationship that
expected absolute sampling error decreases as sample size increases,
approximately following `σ / √n`.

## Machine Learning / AI Connection

The notebook connects sampling concepts to machine learning:

-   **Train / Validation / Test Split:** The test set is a sample used
    to estimate model performance on unseen data.
-   **Stratified Split:**
    `sklearn.model_selection.train_test_split(stratify=y)` can preserve
    class proportions across data splits.
-   **Imbalanced Learning:** Over-sampling and under-sampling are used
    to address class imbalance.
-   **Data Leakage:** The notebook discusses how an unrepresentative
    test set can affect evaluation of future data.

## Libraries Used

-   Python
-   NumPy
-   Pandas
-   Matplotlib

## How to Run

1.  Download or clone this repository.
2.  Open the notebook file in Jupyter Notebook, JupyterLab, or Google
    Colab.
3.  Run the notebook cells in order.
4.  Review the printed comparisons and the sampling-error graph.

Install the required libraries with:

``` bash
pip install numpy pandas matplotlib
```

## Repository Structure

``` text
Sampling-and-Sampling-Error/
├── README.md
└── sampling_and_sampling_error.ipynb
```

## Conclusion

This project demonstrates sampling methods and sampling errors through
Python examples. It compares Simple Random Sampling with Stratified
Sampling and visualizes how sampling error changes with sample size.
