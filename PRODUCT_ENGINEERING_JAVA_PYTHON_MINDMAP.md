# Product Engineering Mind Map

## From Technologies to Solutions

---

# The Core Problem

Most roadmaps look like this:

```text
Java
↓
Spring
↓
Database
↓
Kafka
↓
Redis
↓
AI
```

The problem:

```text
I know what to learn,
but I don't know why I need it.
```

Real engineers think differently.

They think:

```text
Problem
↓
Feature
↓
Pain
↓
Concept
↓
Solution
↓
Trade-off
↓
Next Problem
```

The goal is not to memorize technologies.

The goal is to build a mental map connecting:

- Problems
- Solutions
- Design Decisions
- Trade-offs
- Product Requirements

When a problem occurs, the solution should naturally come to mind.

---

# Product-Centered Learning

One product.

```text
Mini Core Bank
```

One goal.

```text
Allow users to transfer money safely.
```

Every concept is added because the product demands it.

---

# Product Evolution Map

```text
Create Account
↓
Store Accounts
↓
Search Accounts
↓
Deposit / Withdraw
↓
Persist Data
↓
Transaction History
↓
Money Transfer
↓
Concurrency
↓
REST APIs
↓
Authentication
↓
Scaling
↓
Events
↓
Microservices
↓
Production Monitoring
↓
AI Features
```

---

# Stage 1: Create Accounts

## Feature

```text
Create Account
View Account
```

## User Story

```text
A customer opens a bank account.
```

## Concepts Required

```text
Class
Object
Constructor
Methods
Encapsulation
```

## Questions

```text
What is an Account?

What data belongs to it?

Who is allowed to modify balance?
```

## Mental Outcome

```text
Understanding why OOP exists.
```

---

# Stage 2: Store Multiple Accounts

## New Problem

```text
One account is not enough.

Need 1000 accounts.
```

## Concepts

```text
Collections
ArrayList
Generics
```

## Why

```text
Manage large amounts of data.
```

## Mental Outcome

```text
Understanding why collections exist.
```

---

# Stage 3: Search Accounts

## Problem

```text
Need to find account by ID.
```

## Pain

```text
ArrayList becomes slow.
```

## Concepts

```text
HashMap
hashCode()
equals()
```

## Goal

```text
Fast lookup.
```

## Mental Outcome

```text
Understanding when HashMap is required.
```

---

# Stage 4: Deposit and Withdraw

## Problem

```text
User enters invalid values.
```

Example:

```text
Deposit: -500
Withdraw: -100
```

## Concepts

```text
Validation
Business Rules
Exceptions
Custom Exceptions
```

## Why

```text
Protect business logic.
```

## Mental Outcome

```text
Exceptions exist to protect the system.
```

---

# Stage 5: Persistence

## Problem

```text
Application restart loses data.
```

## Disaster

```text
Customer balance disappears.
```

## Concepts

```text
File I/O
JDBC
PostgreSQL
```

## Why

```text
Memory is temporary.
```

## Mental Outcome

```text
Understanding why databases exist.
```

---

# Stage 6: Transaction History

## Feature

```text
View transactions.
```

## Requirement

```text
Audit trail.
```

## Concepts

```text
Tables
Relationships
Foreign Keys
Indexes
```

## Mental Outcome

```text
Understanding relational databases.
```

---

# Stage 7: Money Transfer

## Feature

```text
Transfer money.
```

## Problem

```text
Debit succeeds.

Credit fails.
```

## Disaster

```text
Money disappears.
```

## Concepts

```text
ACID
Transactions
@Transactional
```

## Why

```text
Money must never be lost.
```

## Mental Outcome

```text
Understanding why transactions exist.
```

---

# Stage 8: Concurrency

## Scenario

```text
Joint Account Balance = 1000

User A Withdraws 1000
User B Withdraws 1000

At the same moment.
```

## Disaster

```text
Negative balance.
```

## Concepts

```text
Threads
Race Conditions
Locks
Synchronization
```

## Mental Outcome

```text
Understanding concurrency problems.
```

---

# Stage 9: REST APIs

## Problem

```text
Application only works locally.
```

## Requirement

```text
Mobile App
Web App
External Integrations
```

## Concepts

```text
HTTP
REST
JSON
Spring Boot
Controllers
DTOs
```

## Mental Outcome

```text
Understanding why APIs exist.
```

---

# Stage 10: Authentication

## Problem

```text
Anyone can access accounts.
```

## Risk

```text
Unauthorized transfers.
```

## Concepts

```text
JWT
Spring Security
OAuth2
Roles
Permissions
```

## Mental Outcome

```text
Understanding security architecture.
```

---

# Stage 11: Scaling

## Problem

```text
10,000 users.
```

## Symptoms

```text
Slow queries.
Slow responses.
```

## Concepts

```text
Indexes
Pagination
Caching
Redis
Connection Pools
```

## Mental Outcome

```text
Understanding performance optimization.
```

---

# Stage 12: Events

## Requirement

```text
Transfer Completed
```

Multiple systems must react.

```text
Notify User
Generate Audit
Generate Report
Fraud Detection
```

## Concepts

```text
Kafka
Messaging
Events
Queues
```

## Mental Outcome

```text
Understanding event-driven systems.
```

---

# Stage 13: Microservices

## Problem

```text
Monolith becomes huge.
```

## Split Into

```text
Account Service
Transfer Service
Notification Service
Fraud Service
```

## Concepts

```text
Microservices
API Gateway
Service Discovery
gRPC
Distributed Systems
```

## Mental Outcome

```text
Understanding when microservices help.
```

---

# Stage 14: Production Engineering

## Problem

```text
Application crashes.
```

Questions:

```text
Where?
Why?
When?
```

## Concepts

```text
Logging
Metrics
Tracing
Prometheus
Grafana
OpenTelemetry
```

## Mental Outcome

```text
Understanding observability.
```

---

# Stage 15: AI Layer

## Problem

```text
Millions of transactions.

Fraud team overloaded.
```

## Feature

```text
Fraud Detection
Risk Scoring
Support Automation
```

## Concepts

```text
Machine Learning
Anomaly Detection
LLMs
RAG
Agents
```

## Mental Outcome

```text
AI should assist decision making.

AI should not replace business rules.
```

---

# Engineer's Problem-to-Solution Mental Map

Instead of memorizing technologies:

```text
HashMap
Kafka
Redis
JWT
RAG
```

Memorize problems:

---

## Search Is Slow

```text
Use HashMap
```

---

## Data Lost After Restart

```text
Use Database
```

---

## Money Lost During Transfer

```text
Use Transactions
```

---

## Duplicate Requests

```text
Use Idempotency
```

---

## Slow Queries

```text
Use Indexes
```

---

## Application Slow

```text
Use Cache
```

---

## Concurrent Updates

```text
Use Locks
```

---

## Need Audit Trail

```text
Use Events
```

---

## Multiple Services

```text
Use Kafka
```

---

## Unauthorized Access

```text
Use Security
```

---

## Need Real-Time Insights

```text
Use Observability
```

---

## Need Intelligence

```text
Use AI
```

---

# Robust Product Checklist

Every product should answer:

## Functionality

```text
Does it work?
```

---

## Reliability

```text
What happens when it fails?
```

---

## Security

```text
Can someone abuse it?
```

---

## Performance

```text
Can it handle growth?
```

---

## Observability

```text
Can I understand what is happening?
```

---

## Maintainability

```text
Can another engineer understand it?
```

---

## Recoverability

```text
Can damaged data be restored?
```

---

## Testability

```text
Can it be verified automatically?
```

---

# Repository Structure

```text
mini-core-bank/

README.md

ROADMAP.md

PRODUCT_ENGINEERING_MINDMAP.md

LEARNING.md

DECISIONS.md

MISTAKES.md

IDEAS.md

docs/

01-oop/
02-collections/
03-database/
04-transactions/
05-concurrency/
06-spring/
07-security/
08-kafka/
09-observability/
10-ai/
```

---

# Folder Template

Each concept folder contains:

```text
Problem
↓
Feature
↓
Failure
↓
Concept
↓
Implementation
↓
Trade-Off
↓
Next Problem
```

Example:

```text
Problem:
Search by Account ID

Feature:
Account Lookup

Failure:
Linear Search Too Slow

Concept:
HashMap

Implementation:
AccountRepository

Trade-Off:
More Memory Usage

Next Problem:
Concurrent Access
```

---

# Engineer's Final Operating Principle

Whenever you are stuck, do not ask:

```text
What technology should I learn?
```

Ask:

```text
What problem am I experiencing?
```

Then map it:

```text
Slow Search?
→ HashMap

Data Lost?
→ Database

Money Lost?
→ Transaction

Duplicate Request?
→ Idempotency

Slow Query?
→ Index

Many Users?
→ Concurrency

Need Audit?
→ Events

Need Security?
→ JWT

Need Intelligence?
→ AI
```

Technologies are answers.

Problems are the real syllabus.

---

# Final Formula

```text
Problem
↓
Feature
↓
Failure
↓
Concept
↓
Implementation
↓
Trade-Off
↓
Next Problem
```

Build products.

Observe failures.

Learn concepts.

Apply solutions.

Repeat for years.
