error_report = """
# Error Analysis

## False Positives

Customers predicted to churn but remained active.

Implication:
Retention resources may be spent unnecessarily.

## False Negatives

Customers who churned but were not identified.

Implication:
Lost opportunity for intervention.

## Recommendations

- Add complaint data
- Add engagement metrics
- Add website activity
"""

with open("error_analysis.md", "w") as f:
    f.write(error_report)