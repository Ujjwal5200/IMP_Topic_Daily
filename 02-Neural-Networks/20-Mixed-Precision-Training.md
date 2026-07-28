# Mixed Precision Training

## Definition
Mixed precision training uses lower-precision numbers like FP16 or BF16 together with FP32 to speed up training and reduce memory usage while preserving model quality.

## Why It Is Useful
- Faster training on modern GPUs
- Lower memory consumption
- Larger batch sizes become possible
- Better hardware utilization

```mermaid
flowchart LR
A[Forward Pass in FP16/BF16] --> B[Loss Scaling]
B --> C[Backward Pass]
C --> D[FP32 Master Weights]
D --> E[Weight Update]
```

## Key Idea
Use lower precision where it is safe and use higher precision where numerical stability matters.

## Common Formats
| Format | Notes |
|---|---|
| FP32 | Full precision, stable, expensive |
| FP16 | Fast, memory-efficient, can underflow |
| BF16 | Better range than FP16, common on newer hardware |

## Loss Scaling
To avoid gradient underflow, the loss is multiplied by a scaling factor before backpropagation and then gradients are unscaled before the optimizer step.

## PyTorch Example
```python
scaler = torch.cuda.amp.GradScaler()

with torch.cuda.amp.autocast():
    pred = model(x)
    loss = criterion(pred, y)

scaler.scale(loss).backward()
scaler.step(optimizer)
scaler.update()
```

## Best Practices
- Use AMP when the hardware supports it.
- BF16 is often easier to use than FP16 on supported accelerators.
- Monitor for NaNs or divergence.
- Combine with gradient clipping when needed.

## Interview Questions
- What is mixed precision training?
- Why does it speed up training?
- FP16 vs BF16?
- What is loss scaling?