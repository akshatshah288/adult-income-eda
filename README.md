# Adult Income: Cleaning, EDA and Feature Engineering

Author: Akshat Shah

This project cleans the Kaggle Adult Income dataset, explores income patterns with six charts, and creates five candidate predictors for future modeling.

## Contents
- `Adult_Income_Cleaning_EDA.ipynb`: notebook with code, explanations, executed outputs, charts and findings.
- `data/adult.csv`: original, unchanged Kaggle CSV.
- `outputs/adult_cleaned_features.csv`: derived data with missing categories handled, exact duplicates removed, diagnostic flags and engineered features.
- `outputs/charts/`: six PNG charts.
- `outputs/five_key_insights.md`: five findings.
- `outputs/cleaning_audit.csv`, `outputs/missing_values_before.csv`, `outputs/outlier_report.csv`: audit tables.
- `SUBMISSION_GUIDE.md`: Kaggle, GitHub and Colab instructions.
- `requirements.txt`: packages for a local Jupyter environment.

## Run
For Kaggle, import the notebook and attach `wenruliu/adult-income-dataset`. For Colab, upload the notebook and `adult.csv` through the Files sidebar. For local Jupyter, keep this folder structure and run:

```bash
python -m pip install -r requirements.txt
jupyter notebook Adult_Income_Cleaning_EDA.ipynb
```

Run all cells from the top. The original CSV is not overwritten; generated files go into `outputs/`. Saved notebook outputs are included, so the analysis can also be read without running it.

## Cleaning decisions
Convert `?` to missing values, remove 52 exact duplicate rows, and fill missing categorical predictors with `Unknown`. The final sample has 48,790 rows. No rows violate the specified numeric plausibility checks. Plausible statistical extremes are retained, flagged where useful, and capital variables are log-transformed in separate columns.

## Features
`age_group`, `works_overtime`, `capital_net`, `capital_gain_log`, and `capital_loss_log`. The target encoding `income_gt_50k` is not a predictor. IQR flags for age and hours are diagnostics and must be recomputed using training-only cutoffs before modeling.

## Findings
- Data quality: 52 duplicate rows were removed, leaving 48,790 records. Before deduplication, workclass, occupation and native country had 2,799, 2,809 and 857 missing values; these predictor values were retained as Unknown.

- Income is imbalanced: 76.1% earn <=50K and 23.9% earn >50K. A future model should be evaluated with precision, recall and F1 as well as accuracy.

- Education is associated with income: 41.3% of bachelor's graduates earn >50K, compared with 15.9% of high-school graduates. Education code has a correlation of 0.33 with the high-income indicator; this is an association, not proof of causation.

- The >50K group works an average of 45.5 hours weekly, versus 38.8 hours for the <=50K group. Their medians are 40 and 40 hours, respectively, so the distributions still overlap.

- Capital gain is zero for 91.7% of records. The >50K rate is 61.7% with positive gains and 20.5% with zero gains. Log features reduce the long tail; positive gains should not automatically be deleted as outliers.

## Scope
The source reflects 1994 Census data. Statistics are unweighted sample associations, not present-day population estimates or causal effects. This assignment performs EDA and feature engineering, without fitting a predictive model.

## Data attribution
- Kaggle: https://www.kaggle.com/datasets/wenruliu/adult-income-dataset
- Becker, B. & Kohavi, R. (1996). Adult. UCI Machine Learning Repository. https://doi.org/10.24432/C5XW20
- UCI source and license: https://archive.ics.uci.edu/dataset/2/adult ; CC BY 4.0 https://creativecommons.org/licenses/by/4.0/
- The original CSV is redistributed with attribution. The derived CSV contains the transformations documented in the notebook.
