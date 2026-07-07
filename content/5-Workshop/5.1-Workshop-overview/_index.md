---
title : "Introduction"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.1. </b> "
---

#### What is PeriodIQ?

PeriodIQ is a serverless application that generates a personalized 4-week gym workout plan for a user based on their fitness level, body weight, training goal, and Personal Records, using a rule-based engine (Volume Filter -> Conflict Resolution -> Progression Builder). The full architecture (16 AWS services across 8 layers) is described in the [Proposal](../../2-proposal/) section.

#### How the team split the work

| Section | Role | AWS Services |
|---|---|---|
| Lê Hoài Huân | Auth & User Profile | Amazon Cognito, AWS WAF, Amazon CloudFront |
| **Trần Anh Tài (me)** | **Rule Engine & Workout Generation** | **Lambda (API Handler + Rule Engine), Amazon S3** |
| Lê Hữu Duy Hoàng | Progress & Async Notification | Amazon SQS, Lambda Worker, Amazon SNS |
| Chương Tử Luân | Admin Panel & Data | Lambda Admin API, Amazon DynamoDB, API Gateway |
| Phạm Văn Sỹ | CI/CD & Monitoring | AWS CodePipeline, AWS CodeBuild, CloudFormation/SAM, Amazon CloudWatch |

#### Scope of this workshop

This workshop documents the full team architecture and then focuses on **my own role, Trần Anh Tài - Rule Engine & Workout Generation**. My section verifies the workout generation path from the frontend to API Gateway, Lambda Rule Engine, DynamoDB, and CloudWatch. Other sections summarize the supporting roles owned by the remaining team members.

> **Project Note:** the live PeriodIQ deployment is kept running for final evaluation, so no shared production resource is deleted in this report.
