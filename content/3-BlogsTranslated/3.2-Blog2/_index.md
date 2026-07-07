---
title: "Hybrid Multi-Tenant Architecture"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# Building a Hybrid Multi-Tenant Architecture for Stateful Services on AWS

This blog summarizes an AWS Architecture Blog case study about Amazon Ads' ad-serving system. The original model used one AWS account per tenant, which created high operational overhead and slow onboarding. The redesigned architecture uses a hybrid multi-tenant pattern to keep tenant isolation while reducing repeated infrastructure work.

## Main Architecture Idea

The case study introduces a 3-tier model:

* **Tier:** groups tenants with similar service-level or business requirements.
* **Cell:** isolates blast radius and scales tenant groups independently.
* **Infra Group:** shares infrastructure components where safe and cost-effective.

This model combines dedicated components for isolation with shared components for efficiency.

## AWS Services and Patterns

The design uses several AWS building blocks:

* Route 53 weighted routing to shift traffic safely.
* Application Load Balancer rules to route tenant traffic.
* Dedicated Amazon ECS clusters where isolation is required.
* AWS PrivateLink for shared private connectivity.
* Operational automation to reduce manual tenant onboarding effort.

## Key Value

The most important result is operational improvement. By moving away from the "one account per tenant" model, the team reduced tenant onboarding time from 52 days to 7 days while still preserving the isolation needed for stateful services.

## Lessons Learned

Multi-tenant architecture is not only about sharing resources. A practical design needs to balance isolation, cost, operations, deployment speed, and failure containment. Hybrid tenancy is often more realistic than choosing either fully siloed or fully shared infrastructure.
