# AWS Serverless Patterns Lab

## Overview
This repository is a **focused lab for exploring and validating AWS serverless patterns** commonly used in production-grade, event-driven systems.

Rather than implementing a full application, this project isolates **individual architectural patterns** to clearly demonstrate their behavior, tradeoffs, and operational characteristics.

The patterns implemented here are inspired by real-world AWS reference architectures and community-vetted serverless examples.

---

## Purpose
The goal of this repository is to:
- experiment with **event-driven design patterns**
- understand failure modes and retry behavior
- validate observability and idempotency approaches
- document tradeoffs clearly

This repo complements larger system designs by serving as a **pattern validation space**.

---

## Patterns Covered

### Event Routing & Fan-Out
- EventBridge rules for selective routing
- SNS-based fan-out patterns
- Decoupling producers from consumers

### Asynchronous Processing
- SQS-based buffering and backpressure
- Retry behavior and visibility timeouts
- Dead-letter queue (DLQ) handling

### Idempotent Consumers
- Safe message reprocessing
- Duplicate event handling
- Idempotency key strategies

### Observability & Hygiene
- Structured logging
- Correlation IDs
- Metrics and alarms
- Error classification

---

## AWS Services Used
- **AWS Lambda** – serverless compute
- **Amazon EventBridge** – event routing and filtering
- **Amazon SQS** – asynchronous message queues
- **Amazon SNS** – event fan-out
- **Amazon CloudWatch** – logs, metrics, and alarms
- **AWS IAM** – least-privilege access control

---

## Repository Structure

Each pattern is:
- self-contained
- minimal
- intentionally scoped

---

## Infrastructure as Code
Infrastructure is defined using **Terraform**, following repeatable and modular practices.

This allows patterns to be:
- deployed independently
- tested in isolation
- destroyed safely

Community Terraform module conventions (e.g., terraform-aws-modules) are followed where appropriate.

---

## Observability
Each pattern includes:
- structured logs with correlation IDs
- basic CloudWatch metrics
- failure signals suitable for alerting

Observability is treated as a **first-class concern**, not an afterthought.

---

## Tradeoffs
This repository intentionally avoids:
- application-level business logic
- UI or frontend components
- complex authorization models

The focus is **architectural clarity**, not feature completeness.

---

## Why This Repository Exists
In real systems, architectural mistakes often come from misunderstood patterns rather than incorrect code.

This lab exists to:
- validate assumptions
- explore edge cases
- document behavior under failure
- build intuition for system design decisions

---

## References & Inspiration
This project draws inspiration from well-known AWS serverless resources, including:
- AWS Serverless Patterns
- Event-driven architecture examples
- Community-maintained EventBridge and Lambda best practices

Implementation details are original and scoped specifically for experimentation.

---

### Interview-ready summary
> “This repository is a focused lab where I explore and validate AWS serverless patterns—such as event routing, async processing, and idempotent consumers—before applying them to larger production systems.”
