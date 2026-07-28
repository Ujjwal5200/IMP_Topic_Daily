# Pruning

## Definition
Pruning is the process of removing unnecessary weights, neurons, channels, or entire layers from a neural network to reduce model size and computation.

## Why Pruning?
- Smaller model size
- Faster inference
- Lower memory usage
- Useful for deployment on limited hardware

```mermaid
flowchart LR
A[Trained Model] --> B[Identify Low-Importance Weights]
B --> C[Remove / Zero Out]
C --> D[Smaller Sparse Model]
D --> E[Optional Fine-Tuning]
```

## Common Pruning Forms
| Type | Description |
|---|---|
| Unstructured Pruning | Remove individual weights |
| Structured Pruning | Remove channels, filters, or layers |
| Magnitude Pruning | Remove smallest weights |
| Dynamic Pruning | Prune during training or inference |

## What Usually Happens After Pruning
A pruned model often needs fine-tuning to recover performance.

## PyTorch Example
```python
import torch.nn.utils.prune as prune

prune.l1_unstructured(model.linear, name="weight", amount=0.3)
```

## Trade-offs
- Unstructured pruning gives high sparsity but may not speed up on all hardware.
- Structured pruning is easier to accelerate in real systems.
- Heavy pruning can hurt accuracy.

## Best Practices
- Prune after the model reaches good accuracy.
- Fine-tune after pruning.
- Prefer structured pruning for deployment speedups.
- Measure real hardware latency, not just parameter count.

## Interview Questions
- What is pruning?
- Structured vs unstructured pruning?
- Why fine-tune after pruning?
- Does sparse pruning always improve latency?