# stroke-risk-analysis-dashboard
Exploring stroke-related data with Python, statistical analysis, logistic regression, and Power BI to understand patterns and factors associated with recorded stroke outcomes..
# Stroke Risk Analysis & Interactive Dashboard

## Overview

This project presents an analysis of stroke‑related observational data with Python and Microsoft Power BI.

The project combines exploratory data analysis, data quality assessment, statistical hypothesis testing interpretable logistic regression, ROC‑AUC evaluation and interactive data visualization.

The objective is to investigate patterns and associations between clinical and lifestyle variables and recorded stroke outcomes and to clearly distinguish statistical association from causality.

---

## Objectives

- Explore the structure and quality of the dataset

- Identify values and potential outliers

- Analyze demographic, clinical and lifestyle variables

- Compare variables across recorded stroke outcomes

- Apply statistical hypothesis tests

- Build an interpretable logistic regression model

- Evaluate model discrimination using ROC‑AUC

- Develop an interactive Power BI dashboard

- Communicate analytical findings through visual storytelling

---

## Dataset

The dataset contains 5,110 observations. Includes variables such as:

- Age

- Gender

- Hypertension

- Heart disease

- Average glucose level

- BMI

- Work type

- Residence type

- Smoking status

- Stroke outcome

The target variable is `stroke` where:

- `0` = no recorded stroke

- `1` = recorded stroke

---

## Data Preparation

The analysis included:

- Dataset structure and descriptive statistics

- Duplicate‑value checks

- Missing‑value analysis

- BMI missing‑value investigation

- BMI imputation

- IQR‑based outlier identification

- Creation of age groups

- Preparation of an analysis‑ready dataset for Power BI

Potential outliers were investigated instead of automatically removed because statistical outlier status does not necessarily show an incorrect observation.

---

## Exploratory Data Analysis

The analysis examined:

- Age distribution

- BMI distribution

- Average glucose level

- Hypertension

- Heart disease

- Smoking status

- Gender

- Work type

- Residence type

Group‑level comparisons were performed to investigate differences in recorded stroke proportions.

---

## Statistical Analysis

The project uses tests that are appropriate to each variable type.

### Mann–Whitney U Test

Used to compare distributions between stroke outcome groups, including:

- Age

- Average glucose level

### Chi‑Square Test of Independence

Used to investigate associations between categorical variables and recorded stroke outcome including:

- Hypertension

- Heart disease

- Smoking status

- Gender

- Work type

- Residence type

Statistical significance was interpreted using a 0.05 significance level.

---

## Multivariate Logistic Regression

A logistic regression model was developed using:

- Age

- BMI

- Average glucose level

- Hypertension

- Heart disease

- Gender

- Residence type

- Smoking status

The model was used to examine associations with recorded stroke outcomes while accounting for variables simultaneously.

### Model interpretation

Odds ratios and 95 percent confidence intervals were calculated to make the model coefficients easier to interpret.

The variables showing significant associations in the final model included:

- Age

- Average glucose level

- Hypertension

The results are interpreted as statistical associations within the dataset and should not be interpreted as causal effects.

---

## Model Evaluation

The logistic regression model was evaluated using a held‑out test set.

### Test ROC‑AUC

**ROC‑AUC = 0.838**

The ROC curve was above the random‑classifier reference line indicating useful discriminatory ability on the held‑out test data.

---

## Power BI Dashboard

An interactive Power BI dashboard was developed to communicate the analysis through:

- Stroke‑rate KPIs

- Age‑group analysis

- Hypertension comparison

- Heart‑disease comparison

- Glucose distribution

- Smoking‑status analysis

- demographic filters

The dashboard complements the Python analysis by providing an interactive visual exploration layer.

---

## Key Analytical Observations

The analysis identified significant differences or associations involving several variables, including age, average glucose level, hypertension, heart disease, smoking status and work type in bivariate analyses.

However some relationships changed after accounting for variables simultaneously.

For example heart disease showed a significant bivariate association, with recorded stroke outcome while its

I noticed that the association was not statistically significant, in the multivariate regression model.

I see that this shows the importance of considering variables rather than relying only on individual comparisons.

---

## Tools & Technologies

- Python

- Pandas

- NumPy

- Matplotlib

- Seaborn

- SciPy

- Statsmodels

- Scikit-learn

- Google Colab

- Microsoft Power BI

- Git / GitHub

---

## Project Structure

```text

stroke-risk-analysis-dashboard/

│

├── data/

├── notebooks/

├── powerbi/

├── visualizations/

├── README.md

└── requirements.txt
Limitations

This is a dataset where statistical associations found in the analysis do not prove that one factor causes another.

The dataset has a class imbalance meaning there are fewer recorded stroke cases compared to non-stroke cases.

Because of this the logistic regression results should be seen as showing associations, within this dataset. They should not be treated as a clinical prediction system.
Author

Manasvi Sharma

B.Tech Data Science

GitHub: [https://github.com/manasvishara0804/]
```
