# Survival Analysis – Customer Churn and CLV Estimation

## Overview

This project analyzes customer churn behavior and estimates Customer Lifetime Value (CLV) using survival analysis techniques. The analysis was performed as part of a homework assignment for the "Survival Analysis" course.

## Dataset

The dataset includes customer-level data with attributes such as tenure, churn status, gender, income, and service usage.

## Methodology

- The dataset was cleaned and preprocessed, including binary encoding and one-hot encoding for categorical variables.
- Several survival models were tested:
  - LogNormal AFT
  - Generalized Gamma
  - Weibull
- The LogNormal AFT and Generalized Gamma models exhibited numerical instability or produced unrealistic survival estimates.
- The final model selected was the **WeibullFitter**, which provided stable and interpretable survival curves.

## Key Findings

- The overall survival function showed a steady decline in retention, with a survival probability of approximately 60% at 72 months.
- Gender-based survival analysis indicated slightly higher retention for female customers.
- CLV estimation revealed:
  - Female CLV: $2,762.91
  - Male CLV: $2,757.21
- Female customers represent a marginally more valuable segment for retention strategies.

## Setup Instructions

This project requires Python 3.9+ and `lifelines` with AFT model support.

It is recommended to create a virtual environment:

```bash
python3 -m venv venv-clv
source venv-clv/bin/activate
pip install -r requirements.txt
```

## Tools

- Python
- **lifelines**
- **pandas**
- **matplotlib**

## Deliverables

- Jupyter Notebook with code, analysis, and visualizations.
- **requirements.txt** for environment reproducibility.

## Author - **Albert Simonyan**