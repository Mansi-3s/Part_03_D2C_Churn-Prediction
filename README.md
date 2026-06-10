# Part 3 – Churn Prediction Model & Model Card

## Objective

The objective of this project is to build a machine learning model that predicts which customers are likely to churn within the next 60 days. The model is intended to support customer retention efforts by identifying at-risk customers before they become inactive.

## Business Problem

Customer churn directly impacts revenue and customer lifetime value. The goal of this project is to identify customers who are at risk of churning within the next 60 days so that retention actions can be taken before customers disengage.

## Project Structure

part3/
│
├── churn_model.ipynb
├── model.pkl
├── metrics.json
├── error_analysis.md
├── model_card.md
├── requirements.txt
└── README.md

---

## Repository Contents

| File              | Description                                                                                                                                 |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| churn_model.ipynb | Main notebook containing data preparation, model training, evaluation, threshold selection, feature interpretation, and model documentation |

| model.pkl         | Saved final model  artifact                                                                                                                  |
| metrics.json      | Evaluation metrics for the selected model                                                                                                   |
| error_analysis.md | Summary of false positive and false negative analysis                                                                                       |
| model_card.md     | Documentation describing model purpose, performance, limitations, and monitoring requirements                                               |
| requirements.txt  | Python package requirements                                                                                                                 |

---

## Dataset

This project uses the provided churn modeling dataset (or a feature table created from the raw customer data).

The target variable is:

* **churn** = 1 → Customer churned within the prediction window
* **churn** = 0 → Customer remained active

Features include customer behavioral, transactional, and engagement metrics such as:

* Recency
* Frequency
* Monetary Value (RFM)
* Customer tenure
* Support interaction features
* Additional engineered behavioral features

---

## Data Splitting Strategy

The data is separated into:

* Training Set
* Validation Set
* Test Set

This separation ensures that model selection and evaluation are performed on unseen data.

---

## Models Evaluated

The following models were trained and compared:

1. Logistic Regression (Baseline)
2. Random Forest
3. XGBoost
4. LightGBM

The best-performing model was selected based on validation and test performance.

---

## Evaluation Metrics

Model performance was evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC

Accuracy was not used as the sole evaluation metric because churn prediction is an imbalanced classification problem.

---

## Threshold Selection

The classification threshold was selected based on business considerations.

Missing a customer who is likely to churn (False Negative) is typically more costly than contacting a customer who ultimately remains active (False Positive). Therefore, threshold selection prioritized customer retention opportunities while maintaining reasonable precision.

---

## Error Analysis

Error analysis was performed using:

* False Positives
* False Negatives

Ten customer cases were manually reviewed and interpreted to understand model mistakes and identify opportunities for feature improvement.

---

## Feature Importance

Feature importance analysis was conducted to identify the primary drivers of churn predictions.

Key features include:

* Recency
* Frequency
* Monetary Value
* Customer Tenure

These features capture customer engagement, purchasing behavior, and relationship strength.

---

## Leakage Prevention

A snapshot-based modeling approach was used.

Only information available before the prediction window was used to create features.

No future customer behavior, purchases, or outcomes were included during feature generation.

---

## Model Documentation

A complete model card is included in `model_card.md`, covering:

* Intended use
* Data used
* Modeling approach
* Performance
* Limitations
* Ethical risks
* Monitoring requirements
* Appropriate and inappropriate use cases

---


##  Run Project

```bash

git clone https://github.com/Mansi-3s/Part_03-D2C-Churn-Prediction-Model.git
cd Part_03-D2C-Churn-Prediction-Model

## Install dependencies:


pip install -r requirements.txt
```

## Open:

```bash
jupyter notebook churn_model.ipynb
```

3. Run all notebook cells sequentially.

---

## Final Model Performance

The selected model achieved the best balance between identifying at-risk customers and minimizing unnecessary interventions.

Evaluation metrics included:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

Detailed metric values are available in `metrics.json`.

## Key Outcome

The final model successfully predicts customers at risk of churn and outperforms the baseline model using multiple classification metrics. The model provides actionable insights for customer retention and can support proactive intervention strategies.
