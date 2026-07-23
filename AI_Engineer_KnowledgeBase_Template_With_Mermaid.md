# AI Engineer Knowledge Base Template

> Use this template for **every topic** you study. The goal is to
> understand concepts deeply enough to explain them confidently in an
> interview.

------------------------------------------------------------------------

# Topic: Activation Function

## 1. Definition

An activation function is a mathematical function applied to the output
of a neuron (`Wx + b`) to introduce **non-linearity**.

------------------------------------------------------------------------

## 2. Why is it Needed?

### Problem

Without activation functions:

-   Every layer performs only a linear transformation.
-   Multiple linear layers collapse into one linear equation.
-   Deep networks cannot learn complex relationships.

------------------------------------------------------------------------

## 3. Visual Flow

``` mermaid
flowchart LR
A[Input] --> B[Weighted Sum Wx+b]
B --> C[Activation Function]
C --> D[Next Layer]
```

------------------------------------------------------------------------

## 4. Why Without Activation Fails

``` mermaid
flowchart TD
A[Input]
A --> B[Linear Layer]
B --> C[Linear Layer]
C --> D[Linear Layer]
D --> E[Output]

F["Equivalent to ONE Linear Layer"] -.-> E
```

------------------------------------------------------------------------

## 5. How It Works

1.  Input enters neuron.
2.  Neuron computes `Wx+b`.
3.  Activation (ReLU/GELU/Sigmoid) is applied.
4.  Output goes to the next layer.

------------------------------------------------------------------------

## 6. Real Example

Image Classification

    Image
     ↓
    Edges
     ↓
    Shapes
     ↓
    Eyes
     ↓
    Face
     ↓
    Person

Without activation the network cannot learn this hierarchy.

------------------------------------------------------------------------

## 7. Common Activation Functions

  Function   Use                  Why
  ---------- -------------------- --------------------------
  ReLU       Hidden layers        Fast, simple
  GELU       Transformers         Smooth activation
  Sigmoid    Binary output        Probability
  Softmax    Multi-class output   Probability distribution

------------------------------------------------------------------------

## 8. Advantages

-   Enables deep learning
-   Learns non-linear patterns
-   Improves model capability

------------------------------------------------------------------------

## 9. Limitations

-   Wrong activation may slow training
-   Sigmoid/Tanh can suffer vanishing gradients

------------------------------------------------------------------------

## 10. Interview Answer (30 sec)

> Activation functions introduce non-linearity after each neuron.
> Without them, a deep neural network becomes mathematically equivalent
> to a single linear model and cannot learn complex patterns. Modern
> Transformer-based LLMs commonly use GELU in their feed-forward layers.

------------------------------------------------------------------------

## 11. Interview Follow-ups

-   Why ReLU?
-   Why GELU?
-   Why not Sigmoid everywhere?
-   Difference between activation and LayerNorm?

------------------------------------------------------------------------

# Template for Every Topic

Copy this structure for every concept.

``` text
1. Definition

2. Why needed?

3. Problem solved

4. Mermaid diagram

5. Step-by-step working

6. Real-world example

7. Advantages

8. Limitations

9. Alternatives

10. Interview answer (30 sec)

11. Detailed answer (2 min)

12. Follow-up questions

13. Common mistakes

14. Code (if applicable)

15. Revision (5 bullets)
```

# Mermaid Diagram Ideas

## Gradient Descent

``` mermaid
flowchart LR
Loss --> Gradient
Gradient --> UpdateWeights
UpdateWeights --> BetterModel
```

## RAG

``` mermaid
flowchart LR
User --> Query
Query --> Embed
Embed --> VectorDB
VectorDB --> RetrievedDocs
RetrievedDocs --> LLM
LLM --> Answer
```

## Transformer

``` mermaid
flowchart LR
Tokens --> Embedding
Embedding --> PositionalEncoding
PositionalEncoding --> SelfAttention
SelfAttention --> FeedForward
FeedForward --> Output
```

## AWS AI Service

``` mermaid
flowchart LR
User --> ALB
ALB --> FastAPI
FastAPI --> Redis
FastAPI --> PostgreSQL
FastAPI --> LLM
LLM --> Response
```

## Kubernetes

``` mermaid
flowchart LR
User --> Ingress
Ingress --> Service
Service --> Pods
Pods --> Database
```

## CI/CD

``` mermaid
flowchart LR
Developer --> GitHub
GitHub --> Jenkins
Jenkins --> Docker
Docker --> Kubernetes
```

# Sections to Create

-   01-ML-Fundamentals
-   02-Neural-Networks
-   03-Deep-Learning
-   04-Transformers
-   05-LLMs
-   06-RAG
-   07-AI-Agents
-   08-Embeddings
-   09-Vector-Databases
-   10-Prompt-Engineering
-   11-System-Design
-   12-AWS
-   13-Docker
-   14-Kubernetes
-   15-MLOps
-   16-Redis
-   17-PostgreSQL
-   18-Python
-   19-SQL
-   20-Behavioral Interviews
