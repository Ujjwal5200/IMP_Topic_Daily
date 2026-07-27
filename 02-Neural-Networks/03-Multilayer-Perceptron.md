# Multilayer Perceptron (MLP)

## Definition
A Multilayer Perceptron (MLP) is a feedforward neural network consisting of an input layer, one or more hidden layers, and an output layer. Unlike a single perceptron, an MLP can learn complex non-linear relationships using activation functions and backpropagation.

## Why MLP?
- Solves non-linear problems
- Learns hierarchical feature representations
- Can solve XOR
- Foundation of deep learning

```mermaid
flowchart LR
I[Input Layer] --> H1[Hidden Layer 1]
H1 --> H2[Hidden Layer 2]
H2 --> O[Output Layer]
```

## Components
- Input Layer
- Hidden Layers
- Weights & Biases
- Activation Functions
- Output Layer

## Forward Propagation
1. Compute weighted sum.
2. Apply activation.
3. Pass output to next layer.
4. Produce final prediction.

## Matrix Form
Z = XW + b

A = f(Z)

## Advantages
- Learns complex patterns
- Supports multi-class classification
- Universal function approximator

## Limitations
- Computationally expensive
- Requires large datasets
- Can overfit without regularization

## Python Example
```python
from sklearn.neural_network import MLPClassifier

model = MLPClassifier(hidden_layer_sizes=(64,32), max_iter=500)
model.fit(X_train, y_train)
```

## Interview Questions
- Why are hidden layers needed?
- How is an MLP different from a perceptron?
- Why can MLP solve XOR?
- What is forward propagation?
