---
title: "Week 11 Worklog"
date: 2024-01-01
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:

* Verify the AWS resources behind my PeriodIQ Rule Engine role.
* Confirm that the live request path works on AWS from frontend to API Gateway, Lambda, DynamoDB, SQS, and CloudWatch.
* Collect real screenshots and CLI/log evidence for the workshop report.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Verify Lambda function `periodiq-rule-engine-dev`: trigger, runtime, description, and recent deployment timestamp | 29/06/2026 | 29/06/2026 | AWS Console screenshot - Lambda |
| 3 | - Verify API Gateway route `ANY /api/workoutplans/generate` and confirm it points to the Rule Engine Lambda path | 30/06/2026 | 30/06/2026 | AWS Console screenshot - API Gateway |
| 4 | - Verify S3 frontend bucket `periodiq-frontend-dev-345798130457` contains the deployed React/Vite build files | 01/07/2026 | 01/07/2026 | AWS Console screenshot - S3 deployment<br><https://d1di1pzmfypszp.cloudfront.net> |
| 5 | - Verify generated `WorkoutPlan` items in DynamoDB, especially the nested `Weeks` output created by the Rule Engine | 02/07/2026 | 02/07/2026 | DynamoDB table screenshots |
| 6 | - Generate a plan and inspect CloudWatch logs for `POST /api/workoutplans/generate`, HTTP 200, Lambda START/END/REPORT, and SQS message after generation | 03/07/2026 | 03/07/2026 | CloudWatch log evidence and SQS evidence |


### Week 11 Achievements:

* Verified the real AWS services used by my workout generation flow.
* Confirmed the full path: S3 frontend -> API Gateway -> Lambda Rule Engine -> DynamoDB -> CloudWatch logs.
* Confirmed that plan generation also continues the asynchronous flow by sending an SQS message.
* Collected evidence for Lambda, API Gateway, S3, DynamoDB, and CloudWatch workshop pages.
* Prepared accurate report content based on actual AWS resources instead of generic service descriptions.
