# Model Card

## Model Name
Customer Churn Prediction Model

## Intended Use
Identify customers likely to churn within the next 60 days.

## Users
Retention team
CRM team
Marketing team

## Data
Customer transactions
Customer demographics
Support interactions

## Target
Churn within next 60 days

## Models Evaluated
- Logistic Regression
- XGBoost

## Final Model
Logistic Regression

## Performance

Accuracy: 0.8036
Precision: 0.8000
Recall: 0.8095
F1: 0.8047
ROC-AUC: 0.8887

## Threshold
Chosen using validation F1 optimization.

## Limitations

- Does not capture competitor activity.
- Does not include website engagement.
- Performance may drift over time.

## Ethical Considerations

- Avoid discriminatory targeting.
- Use predictions to assist decisions, not automate customer treatment.

## Monitoring

Monitor:

- Precision
- Recall
- ROC-AUC
- Churn rate
- Feature drift
