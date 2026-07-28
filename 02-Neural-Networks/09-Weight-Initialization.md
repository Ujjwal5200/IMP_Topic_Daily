# Weight Initialization

## Definition
Weight initialization is the process of assigning initial values to a neural network's weights before training begins. Proper initialization helps gradients flow effectively and speeds up convergence.

## Why is it Important?
- Prevents vanishing and exploding gradients
- Speeds up convergence
- Improves training stability
- Helps deep networks learn efficiently

```mermaid
flowchart LR
A[Initialize Weights] --> B[Forward Pass]
B --> C[Loss]
C --> D[Backpropagation]
D --> E[Update Weights]
```

## Common Initialization Methods
| Method | Best For |
|--------|----------|
| Zero Initialization | Not recommended |
| Random Initialization | Simple networks |
| Xavier (Glorot) | Sigmoid/Tanh |
| He (Kaiming) | ReLU/GELU |
| Orthogonal | RNNs and deep models |

## Key Formulas
- Xavier: Var(W)=2/(fan_in+fan_out)
- He: Var(W)=2/fan_in

## PyTorch Example
```python
import torch.nn as nn
nn.init.xavier_uniform_(layer.weight)
n.init.kaiming_normal_(layer.weight)
```

## Best Practices
- Use He initialization with ReLU.
- Use Xavier with Sigmoid or Tanh.
- Never initialize all weights to zero.

## Interview Questions
- Why can't all weights be initialized to zero?
- Xavier vs He initialization?
- How does initialization affect convergence?
- Which initialization is best for ReLU?