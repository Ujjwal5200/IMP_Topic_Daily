# Neural Architecture Search (NAS)

## Definition
Neural Architecture Search is an automated method for finding better neural network architectures by searching over a space of candidate designs.

## Why NAS?
- Reduces manual architecture trial-and-error
- Can discover efficient models automatically
- Useful when you need strong accuracy under compute constraints

```mermaid
flowchart LR
A[Search Space] --> B[Search Strategy]
B --> C[Candidate Architectures]
C --> D[Evaluate Performance]
D --> E[Best Architecture]
```

## Main Parts of NAS
- Search space: what architectures are allowed
- Search strategy: how candidates are explored
- Evaluation strategy: how candidates are scored

## Common Search Methods
| Method | Idea |
|---|---|
| Random Search | Sample architectures randomly |
| Evolutionary Search | Mutate and select architectures |
| Reinforcement Learning | Use reward to guide search |
| Gradient-Based NAS | Make search differentiable |

## Trade-offs
- NAS can be expensive to run.
- Better architectures may still be hard to deploy.
- The search cost can outweigh the benefit for small projects.

## Best Practices
- Define a small, meaningful search space.
- Use proxy evaluation to reduce cost.
- Validate the final architecture carefully.
- Compare against a strong manual baseline.

## Interview Questions
- What is Neural Architecture Search?
- What are search space, strategy, and evaluation?
- Why is NAS expensive?
- When would you avoid NAS?