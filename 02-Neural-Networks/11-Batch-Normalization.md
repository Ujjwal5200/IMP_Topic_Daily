# Batch Normalization

## Definition
Batch Normalization (BatchNorm) is a technique that normalizes the activations of each mini-batch during training, making neural networks train faster and more stably.

## Why Batch Normalization?
- Speeds up convergence
- Reduces internal covariate shift
- Stabilizes gradient flow
- Allows higher learning rates
- Acts as a mild regularizer

```mermaid
flowchart LR
A[Input] --> B[Linear Layer]
B --> C[Batch Normalization]
C --> D[Activation Function]
D --> E[Next Layer]
```

## BatchNorm Equation
x̂ = (x - μ) / √(σ² + ε)

y = γx̂ + β

Where:
- μ = batch mean
- σ² = batch variance
- ε = small constant
- γ = learnable scale
- β = learnable shift

## Training vs Inference
| Training | Inference |
|----------|-----------|
| Uses batch statistics | Uses running averages |

## PyTorch Example
```python
import torch.nn as nn

model = nn.Sequential(
    nn.Linear(128, 256),
    nn.BatchNorm1d(256),
    nn.ReLU()
)
```

## Best Practices
- Place BatchNorm before the activation function.
- Use mini-batches large enough for stable statistics.
- Switch to `model.eval()` during inference.

## Interview Questions
- Why is Batch Normalization used?
- What is internal covariate shift?
- Why are running statistics needed during inference?
- BatchNorm vs LayerNorm?