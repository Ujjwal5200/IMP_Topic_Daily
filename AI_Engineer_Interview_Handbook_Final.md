# AI Engineer Interview Handbook (Master Revision)

## Purpose

This handbook is designed for daily revision before AI Engineer
interviews. Every topic should be studied using the same framework so
you remember concepts, not definitions.

## Universal Study Template

For every topic answer:

1.  Definition
2.  Why is it needed?
3.  Problem it solves
4.  How it works
5.  Mermaid diagram
6.  Real-world example
7.  Advantages
8.  Limitations
9.  Alternatives
10. 30-second interview answer
11. 2-minute detailed answer
12. Common follow-up questions
13. Common mistakes
14. Code example (if relevant)
15. Revision bullets (5 lines)

------------------------------------------------------------------------

# Interview Thinking Pattern

Whenever asked a question:

-   What is it?
-   Why was it invented?
-   How does it work?
-   Where is it used?
-   What are its trade-offs?
-   Give one production example.

------------------------------------------------------------------------

# Example Topic

## Activation Function

### Definition

A function applied after `Wx+b` that introduces non-linearity.

### Why?

Without it, deep neural networks collapse into a single linear
transformation.

### Mermaid

``` mermaid
flowchart LR
Input-->Neuron["Wx+b"]-->Activation-->NextLayer
```

### Example

Image → Edges → Shapes → Face → Person

### 30-sec Interview

Activation functions introduce non-linearity after each neuron. Without
them, even a deep neural network behaves like one linear model. Modern
Transformers typically use GELU in feed-forward layers.

### Follow-ups

-   Why GELU?
-   Why ReLU?
-   Why not Sigmoid?
-   Difference from LayerNorm?

------------------------------------------------------------------------

# ML Evaluation

## Classification

-   Accuracy
-   Precision
-   Recall
-   F1 Score
-   ROC-AUC
-   Confusion Matrix

### Interview Tip

Accuracy alone is not enough for imbalanced datasets.

## Regression

-   MAE
-   MSE
-   RMSE
-   R²

------------------------------------------------------------------------

# LLM Evaluation

Remember: **LLMs are not evaluated using only accuracy.**

## Generation Quality

-   Answer Correctness
-   Relevance
-   Faithfulness
-   Hallucination Rate

## Retrieval (RAG)

-   Context Precision
-   Context Recall
-   Retrieval Precision
-   Retrieval Recall

## Production Metrics

-   Latency
-   Throughput
-   Token Usage
-   Cost per request
-   User Satisfaction
-   Error Rate

### Mermaid

``` mermaid
flowchart LR
User-->Retriever-->VectorDB-->Context-->LLM-->Answer
```

### 30-sec Interview

For RAG systems I evaluate retrieval and generation separately.
Retrieval uses Context Precision and Recall. Generation is evaluated
using correctness, faithfulness, hallucination rate, latency, token
usage and user feedback.

### Follow-ups

-   What is hallucination?
-   What is faithfulness?
-   What is RAGAS?
-   What is DeepEval?
-   How would you compare two prompts?

------------------------------------------------------------------------

# AI System Design Checklist

For every design answer:

1.  Requirements
2.  High-Level Architecture
3.  Components
4.  Database
5.  APIs
6.  Caching
7.  Security
8.  Scalability
9.  Monitoring
10. Failure handling
11. Trade-offs

------------------------------------------------------------------------

# Mermaid Templates

## RAG

``` mermaid
flowchart LR
Query-->Embedding-->VectorDB-->Retriever-->LLM-->Response
```

## Kubernetes

``` mermaid
flowchart LR
Ingress-->Service-->Pods-->Database
```

## AWS

``` mermaid
flowchart LR
User-->ALB-->FastAPI-->Redis
FastAPI-->PostgreSQL
FastAPI-->LLM
```

## CI/CD

``` mermaid
flowchart LR
Developer-->GitHub-->Jenkins-->Docker-->Kubernetes
```

------------------------------------------------------------------------

# Master Topic Checklist

## ML

-   AI vs ML vs DL
-   Supervised / Unsupervised / RL
-   Classification vs Regression
-   Bias-Variance
-   Overfitting
-   Cross Validation
-   Metrics
-   Feature Engineering

## Neural Networks

-   Neuron
-   Weights
-   Bias
-   Activation
-   Loss
-   Optimizer
-   Gradient Descent
-   Backpropagation
-   Learning Rate
-   Epoch
-   Batch Size

## Deep Learning

-   CNN
-   RNN
-   LSTM
-   GRU
-   Transformer

## LLMs

-   Attention
-   QKV
-   Tokenization
-   Embeddings
-   Context Window
-   Temperature
-   Top-k
-   Top-p
-   Fine-tuning
-   LoRA
-   QLoRA
-   Quantization
-   RLHF

## RAG

-   Chunking
-   Embeddings
-   Vector DB
-   Retriever
-   Reranker
-   Hybrid Search
-   Metadata Filtering

## AI Agents

-   Tool Calling
-   Function Calling
-   MCP
-   Memory
-   Planning

## AWS

-   EC2
-   S3
-   IAM
-   VPC
-   ECS
-   EKS
-   Lambda
-   CloudWatch

## Docker & Kubernetes

-   Images
-   Containers
-   Dockerfile
-   Pods
-   Deployments
-   Services
-   Ingress
-   ConfigMap
-   Secret
-   HPA

## Python

-   OOP
-   Async
-   Decorators
-   Generators
-   Threading vs Multiprocessing

## SQL

-   Joins
-   Indexes
-   ACID
-   Transactions
-   Window Functions
-   CTE

------------------------------------------------------------------------

# Random Questions to Practice

-   Explain activation functions.
-   Explain backpropagation.
-   Why use Adam over SGD?
-   Explain embeddings.
-   Explain attention.
-   Explain Transformer.
-   Explain RAG.
-   Difference between RAG and fine-tuning.
-   How do you evaluate an ML model?
-   How do you evaluate an LLM?
-   How do you reduce hallucinations?
-   How do you reduce LLM cost?
-   Design a chatbot.
-   Design a document Q&A system.
-   Explain your project end-to-end.
-   What would you improve in your architecture?
-   Why this database?
-   Why Redis?
-   Why Docker?
-   Why Kubernetes?
-   Explain your CI/CD pipeline.

------------------------------------------------------------------------

# Daily Routine (45--60 min)

1.  Review yesterday (10 min)
2.  Learn one topic using the template (20 min)
3.  Explain it aloud without notes (15 min)
4.  Answer 3 random interview questions (10 min)

**Rule:** Never memorize definitions only. Always remember: - What? -
Why? - How? - Where? - Trade-offs? - Real example?
