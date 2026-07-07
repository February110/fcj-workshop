---
title: "Blogs Posted"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

# BLOGS POSTED

This section lists and introduces the blogs I have posted to [AWS Study Group](https://awsstudygroup.com/).

### [Blog 1 - Subdomain Takeover: When a Forgotten DNS Record Becomes an Attack Vector](3.1-Blog1/)

This blog covers the Subdomain Takeover attack technique, where a dangling DNS record left pointing at a deleted AWS resource such as S3, CloudFront, or Elastic Beanstalk can be reclaimed by an attacker. It explains how the attack happens and proposes an AWS-based detection approach using AWS Config and Lambda to compare Route 53 records with actual account resources, then alert through Security Hub and SNS.

### [Blog 2 - Building a Hybrid Multi-Tenant Architecture for Stateful Services on AWS](3.2-Blog2/)

This blog summarizes an AWS Architecture Blog case study on Amazon Ads' ad-serving system, which moved from a costly "one AWS account per tenant" model to a hybrid 3-tier Tier-Cell-Infra Group architecture using Route 53 weighted routing, per-tenant ALB rules, dedicated ECS clusters, and shared PrivateLink. The design helped reduce tenant onboarding time from 52 days to 7 days.

### [Blog 3 - Session Policies in Amazon EKS Pod Identity](3.3-Blog3/)

This blog introduces the session policies feature in Amazon EKS Pod Identity. The feature allows teams to narrow IAM permissions flexibly and precisely for each pod without creating many separate IAM roles, making it easier to apply least privilege in large-scale Kubernetes environments.
