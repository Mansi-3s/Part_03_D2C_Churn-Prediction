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
XGBoost

## Performance

Accuracy:
Precision:
Recall:
F1:
ROC-AUC:

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