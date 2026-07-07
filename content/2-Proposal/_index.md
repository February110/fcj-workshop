---
title: "Proposal"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# PERIODIQ - SERVERLESS PERIODIZATION ENGINE

## A Science-Based, Automated Workout Plan Generator on AWS Serverless

### 1. Executive Summary

PeriodIQ is a serverless web platform that acts as an automatic personal trainer. A user enters training information such as body weight, fitness level, training goal, available days per week, Personal Records, limitations, and equipment. The system then generates a personalized 4-week workout plan with concrete exercise targets, sets, reps, RPE, rest time, and target weights.

The project is built by a 5-person team using AWS serverless services. My responsibility is **Trần Anh Tài - Rule Engine & Workout Generation**, covering the workout generation API flow, Lambda Rule Engine logic, Workout Plan UI behavior, generated `WorkoutPlan` output, and verification through DynamoDB and CloudWatch logs.

Live project URL: <https://d1di1pzmfypszp.cloudfront.net>

### 2. Problem Statement

**What's the problem?** Most gym users rely on static workout templates from the internet, books, or coaches. These plans usually do not account for individual fitness level, current strength, recovery capacity, available training days, physical limitations, or recent fatigue. As a result, users may under-train with no progression or over-train with excessive high-CNS sessions, increasing the risk of injury and burnout.

**The solution** PeriodIQ automates evidence-based periodization through a 3-step Rule Engine:

1. **Volume Filter** - controls weekly training volume based on goal, fitness level, and days per week.
2. **Conflict Resolution** - prevents unsafe combinations such as too many high-CNS exercises or limitation conflicts.
3. **Progression Builder** - builds a 4-week structure: Week 1 base volume, Week 2 volume overload, Week 3 peak intensity, and Week 4 deload.

Users can generate and view a plan from the web interface. The plan is saved in DynamoDB and displayed back to the user with weekly progression, day split, exercise list, set/rep targets, target RPE, rest time, and target weight.

**Benefits and value**

* Personalized, science-based programming without needing a human coach for every update.
* Safer progression through volume control, conflict rules, and a deload week.
* A real serverless team project using authentication, API, compute, data, async messaging, monitoring, and CI/CD.
* Low idle cost because the system is designed around pay-per-use AWS services.

### 3. Solution Architecture

The system is deployed in AWS region `ap-southeast-1` and organized into multiple layers: Edge/Frontend, Auth, API, Core Engine, Data, Async/Messaging, Monitoring, and CI/CD.

![PeriodIQ AWS Serverless Architecture](../images/2-Proposal/aws_architecture.png)

**Main request flow - Generate Workout Plan**

1. The user accesses the React/Vite web app through CloudFront.
2. CloudFront serves the static frontend from S3 and routes API requests to API Gateway.
3. API Gateway receives authenticated requests and forwards the generation request to the backend Lambda path.
4. The API Handler validates the request and calls the Rule Engine logic.
5. The Rule Engine reads user input and relevant profile data, then runs Volume Filter, Conflict Resolution, and Progression Builder.
6. The generated 4-week plan is saved to DynamoDB as a `WorkoutPlan` item.
7. The API returns the result to the frontend so the user can view the plan immediately.
8. CloudWatch records Lambda execution logs and API behavior for verification.
9. After generation, an asynchronous message can continue the notification/progress flow without blocking the main response.

### AWS Services Used

| # | Service | Layer | Role |
| --- | --- | --- | --- |
| 1 | AWS WAF | Edge/Security | Helps protect public entry points from common web attacks |
| 2 | Amazon CloudFront | Edge | CDN for the React/Vite frontend and routing layer for the public site |
| 3 | Amazon S3 | Frontend | Hosts static frontend build files |
| 4 | Amazon Cognito | Auth | User authentication and JWT issuance |
| 5 | Amazon API Gateway | API | Receives API requests and routes them to Lambda |
| 6 | AWS Lambda - API Handler | Core Engine | Handles user-facing backend requests |
| 7 | AWS Lambda - Rule Engine | Core Engine | Generates the personalized 4-week workout plan |
| 8 | AWS Lambda - Admin API | Core Engine | Supports admin data operations |
| 9 | Amazon DynamoDB | Data | Stores user profile, rules, templates, progress, and generated plans |
| 10 | Amazon SQS | Async | Queues asynchronous work after the main request |
| 11 | AWS Lambda - Worker | Async | Processes queued messages |
| 12 | Amazon SNS / Amazon SES | Notification | Sends notifications and workout-plan related emails |
| 13 | Amazon CloudWatch | Monitoring | Logs, metrics, and alarms |
| 14 | AWS CodePipeline | CI/CD | Orchestrates deployment pipeline |
| 15 | AWS CodeBuild | CI/CD | Builds and tests backend/frontend code |
| 16 | AWS CloudFormation / SAM | IaC | Defines and deploys infrastructure |

### Component Design

* **Edge & Frontend:** React 19 + Vite SPA hosted on S3 and served through CloudFront.
* **Auth:** Cognito handles user sign-in and issues JWTs used by backend APIs.
* **API:** API Gateway exposes HTTP routes such as `POST /api/workoutplans/generate`.
* **Core Engine:** Lambda-backed backend path runs the API Handler and Rule Engine logic.
* **Data:** DynamoDB stores master data, user profiles, records, tracking data, rule definitions, and generated `WorkoutPlan` items.
* **Async/Messaging:** SQS decouples follow-up work such as notification or progress-related processing.
* **Monitoring:** CloudWatch logs and metrics help verify execution and troubleshoot issues.
* **CI/CD:** CodePipeline, CodeBuild, and CloudFormation/SAM support repeatable deployment.

### 4. Technical Implementation

**Team structure** - the project was split among 5 members:

* Lê Hoài Huân - Auth & User Profile: Cognito, WAF, CloudFront.
* **Trần Anh Tài - Rule Engine & Workout Generation:** Lambda API Handler, Lambda Rule Engine, S3-hosted Workout Plan UI.
* Lê Hữu Duy Hoàng - Progress & Async Notification: SQS, Lambda Worker, SNS/SES.
* Chương Tử Luân - Admin Panel & Data: DynamoDB, Lambda Admin API, API Gateway.
* Phạm Văn Sỹ - CI/CD & Monitoring: CodePipeline, CodeBuild, CloudFormation/SAM, CloudWatch.

**My implementation focus**

* Define the Workout Plan input contract: goal, fitness level, days/week, start date, current 1RM, limitations, and equipment.
* Implement or refine `POST /api/workoutplans/generate`.
* Implement Rule Engine stages: Volume Filter, Conflict Resolution, and Progression Builder.
* Store generated plans in DynamoDB with nested `Weeks` output.
* Verify the user-facing product flow: generate plan, view My Plans, open detail, and inspect weekly progression.
* Confirm execution through CloudWatch logs and DynamoDB records.

**Tech stack**

* Backend: .NET, ASP.NET Core Web API, Lambda hosting, Clean Architecture, DynamoDB SDK.
* Frontend: React, Vite, Tailwind CSS, Axios, React Router.
* Cloud: AWS Lambda, API Gateway, DynamoDB, S3, CloudFront, Cognito, SQS, CloudWatch, CodePipeline, CodeBuild, CloudFormation/SAM.

### 5. Timeline & Milestones

* **Weeks 1-5:** Learn AWS foundation services through labs: account setup, IAM, VPC, EC2, S3, DynamoDB, CloudWatch, and security basics.
* **Week 6:** Map serverless backend learning to the PeriodIQ Rule Engine request path.
* **Week 7:** Define authenticated Workout Plan frontend flow and API input requirements.
* **Week 8:** Design Rule Engine logic and DynamoDB `WorkoutPlan.Weeks` output.
* **Week 9:** Start implementing the Rule Engine and workout generation endpoint.
* **Week 10:** Complete the user-facing Workout Plan flow and validate generated output.
* **Week 11:** Verify AWS resources, DynamoDB records, and CloudWatch logs.
* **Week 12:** Finalize demo, workshop pages, report content, and shared-resource notes.

### 6. Budget Estimation

PeriodIQ uses a mostly serverless, pay-per-use architecture. For a small-scale capstone deployment with low request volume, the main cost drivers are:

* **AWS Lambda:** billed per request and execution duration; low traffic is usually very inexpensive.
* **Amazon DynamoDB:** on-demand billing scales with actual reads/writes instead of fixed provisioned capacity.
* **Amazon API Gateway:** billed per API request.
* **Amazon CloudFront + S3:** low cost for a small SPA and low traffic volume.
* **Amazon SQS / SNS / SES:** low message volume, with generous free-tier coverage for small usage.
* **CodePipeline / CodeBuild:** cost depends on active pipelines and build minutes.

No fixed AWS Pricing Calculator estimate is included because the actual cost depends on final user traffic and deployment usage. The architecture was chosen to keep idle cost low and marginal cost near zero at small scale.

### 7. Risk Assessment

* **Rule miscalculation leading to unsafe plans** - mitigated by Volume Filter, Conflict Resolution rules, test scenarios, and final review of generated output.
* **Broken frontend/backend integration** - mitigated by testing the full product flow from CloudFront frontend to API Gateway, Lambda, DynamoDB, and back to the UI.
* **Authentication or API authorization issues** - mitigated by using Cognito JWTs and checking authenticated request behavior.
* **DynamoDB schema mismatch** - mitigated by defining the `WorkoutPlan` output structure early and verifying actual records in DynamoDB.
* **Lambda/runtime errors** - mitigated through CloudWatch logs, API response checks, and repeated generation tests.
* **Deployment drift or stale frontend build** - mitigated through CI/CD verification and CloudFront deployment checks.

### 8. Expected Outcomes

* A working, publicly deployed serverless application for generating personalized 4-week workout plans.
* A completed Rule Engine feature that transforms user training input into structured weekly plans.
* A clear user flow: log in, open Workout Plan, generate a plan, view plan list, and inspect plan details.
* Verified AWS evidence from Lambda, API Gateway, S3/CloudFront, DynamoDB, CloudWatch, and SQS.
* A reusable learning outcome for future serverless .NET and React applications on AWS.

Live result: <https://d1di1pzmfypszp.cloudfront.net>
