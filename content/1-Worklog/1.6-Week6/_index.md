---
title: "Week 6 Worklog"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Learn serverless backend patterns and map them to the PeriodIQ Rule Engine.
* Separate AWS lab learning notes from PeriodIQ project implementation notes.
* Prepare backend design notes for the workout generation endpoint.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Learn Lambda handler structure, runtime settings, environment variables, and execution role | 25/05/2026 | 25/05/2026 | <https://000022.awsstudygroup.com/> |
| 3 | - Apply Lambda learning to the PeriodIQ Rule Engine draft <br>- Identify how the Rule Engine can run as a Lambda-backed API path | 26/05/2026 | 26/05/2026 | PeriodIQ backend design notes |
| 4 | - Learn API Gateway route design and DynamoDB access from Lambda | 27/05/2026 | 27/05/2026 | <https://000066.awsstudygroup.com/><br><https://000078.awsstudygroup.com/><br><https://000060.awsstudygroup.com/> |
| 5 | - Draft request/response shape for `POST /api/workoutplans/generate` <br>- Identify fields for generated workout plans such as `Goal`, `FitnessLevel`, `StartDate`, `EndDate`, and `Weeks` | 28/05/2026 | 28/05/2026 | PeriodIQ API and DynamoDB schema notes |
| 6 | - Summarize the serverless request path for my role: S3 frontend -> API Gateway -> Lambda Rule Engine -> DynamoDB -> CloudWatch | 29/05/2026 | 29/05/2026 | PeriodIQ architecture notes |


### Week 6 Achievements:

* Defined the backend services needed for the workout generation feature.
* Drafted the API route and payload structure for plan generation.
* Identified DynamoDB output fields required by the Rule Engine.
* Separated lab references for AWS learning from PeriodIQ notes for project work.
* Prepared a clear serverless architecture path for my Person 2 scope.
