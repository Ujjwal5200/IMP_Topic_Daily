# Feature Engineering

## Definition
Feature Engineering is the process of creating, transforming, selecting, and improving input features so that machine learning models can learn patterns more effectively. Well-engineered features often improve model performance more than changing algorithms.

## Why is it Important?
- Improves model accuracy.
- Reduces overfitting.
- Makes patterns easier to learn.
- Speeds up training.
- Helps simpler models perform better.

## Workflow
```mermaid
flowchart LR
A[Raw Data] --> B[Data Cleaning]
B --> C[Feature Creation]
C --> D[Feature Transformation]
D --> E[Feature Selection]
E --> F[Train ML Model]
```

## Common Techniques
- Feature creation
- Polynomial features
- Log transformation
- Binning
- One-Hot Encoding
- Label Encoding
- Date & time feature extraction
- Interaction features
- Domain-specific features

## Production Pipeline
1. Collect raw data.
2. Clean missing values.
3. Encode categorical variables.
4. Scale numerical features.
5. Save transformations.
6. Apply identical pipeline during inference.

## Best Practices
- Avoid data leakage.
- Keep transformations consistent.
- Automate preprocessing pipelines.
- Validate feature importance.

## Python Example
```python
from sklearn.preprocessing import PolynomialFeatures
poly = PolynomialFeatures(degree=2)
X_new = poly.fit_transform(X)
```

## Interview Questions
- What is Feature Engineering?
- Why is it important?
- Difference between Feature Engineering and Feature Selection?
- Give real-world examples of engineered features.
