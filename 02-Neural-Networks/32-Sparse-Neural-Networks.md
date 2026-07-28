# Sparse Neural Networks

## Definition
Sparse neural networks are models where many weights are zero or removed, so only a smaller subset of parameters is active during computation.

## Why Sparsity?
- Smaller memory footprint
- Potentially faster inference
- Lower compute and storage costs
- Useful for deployment and compression

```mermaid
flowchart LR
A[Dense Model] --> B[Prune or Mask Weights]
B --> C[Sparse Model]
C --> D[Less Compute / Memory]
```

## Types of Sparsity
| Type | Description |
|---|---|
| Unstructured Sparsity | Individual weights become zero |
| Structured Sparsity | Whole channels/heads/blocks removed |
| Dynamic Sparsity | Sparse pattern changes during training |

## Challenges
- Sparse patterns may not speed up on all hardware
- Training sparse models can be unstable
- Efficient sparse kernels are needed for real acceleration

## Best Practices
- Prefer structured sparsity for deployment speedups.
- Measure real latency on target hardware.
- Fine-tune after pruning or sparsification.

## Interview Questions
- What is a sparse neural network?
- Structured vs unstructured sparsity?
- Does sparsity always improve speed?
- Why is hardware support important?