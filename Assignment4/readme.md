Assignment 4 – Survival Analysis

 Course: BINF-5507 Machine Learning & AI
 Student: Rajdeep Kaur
 Dataset: RADCURE_Clinical_v04_20241219.xlsx


Project Overview
This project uses survival analysis techniques to explore clinical outcomes from cancer patients. The goal is to determine how patient characteristics such as tumor stage, treatment modality, and age affect survival outcomes.

 Tools Used
- Python (Jupyter Notebook)
- lifelines (Kaplan-Meier, Cox Regression)
- scikit-learn (for Random Forest)
- pandas, matplotlib

 Data Preprocessing
- Cleaned column names.
- Converted "status" to binary: "alive" → 0, "dead" → 1
- Dropped missing values for analysis columns.

Kaplan-Meier Survival Analysis
- Generated Kaplan-Meier survival curves grouped by stage.
- Compared survival between Stage III and Stage IV using the log-rank test.

Cox Proportional Hazards Model
- Used covariates: age, stage, tx modality.
- Fitted model using lifelines.CoxPHFitter.
- Checked proportional hazards assumption.
- Evaluated using concordance index (C-index).

 Random Survival Forest (RSF)
- Trained RSF model using one-hot encoded features.
- Identified important predictors.
- Compared C-index of RSF with Cox model.