# Evaluation Metrics

## Definition
Evaluation metrics measure how well a machine learning model performs on unseen data. Choosing the correct metric depends on the problem type, business objective, and dataset characteristics.

## Why Evaluation Metrics Matter
- Compare models objectively
- Detect overfitting and underfitting
- Optimize business outcomes
- Monitor production performance

```mermaid
flowchart LR
A[Predictions] --> B[Compare with Ground Truth]
B --> C[Compute Metrics]
C --> D[Model Evaluation]
D --> E[Model Selection]
```

## Regression Metrics
- MAE
- MSE
- RMSE
- RMSLE
- R² Score
- Adjusted R²

## Classification Metrics
- Accuracy
- Precision
- Recall
- F1 Score
- Specificity
- ROC-AUC
- PR-AUC
- Log Loss
- Matthews Correlation Coefficient (MCC)

## Confusion Matrix
- True Positive
- False Positive
- True Negative
- False Negative

## Choosing the Right Metric
- Balanced classes → Accuracy
- Imbalanced classes → Precision, Recall, F1, PR-AUC
- Regression → MAE or RMSE depending on penalty for large errors

## Python Example
```python
from sklearn.metrics import accuracy_score, f1_score

acc = accuracy_score(y_true, y_pred)
f1 = f1_score(y_true, y_pred)
```

## Best Practices
- Never rely on a single metric.
- Use cross-validation.
- Consider business impact when selecting metrics.
- Monitor metrics after deployment.

## Interview Questions
- Accuracy vs Precision vs Recall?
- When is F1 Score preferred?
- ROC-AUC vs PR-AUC?
- When should MAE be preferred over RMSE?
