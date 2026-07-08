---
title: "Week 6 Worklog"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Start learning serverless backend services that are relevant to the PeriodIQ final project.
* Study Lambda and API Gateway slowly enough to understand the request flow.
* Map only the relevant AWS concepts to my Rule Engine & Workout Generation responsibility.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Team meeting: reviewed the PeriodIQ system architecture (7-layer serverless design on AWS) and divided the project into 5 role groups, each owning 3-4 AWS services | 25/05/2026 | 25/05/2026 | PeriodIQ team meeting notes |
| 2-3 | - Learn AWS Lambda fundamentals <br>- Understand function runtime, handler, event payload, IAM role, and CloudWatch logs | 25/05/2026 | 26/05/2026 | <https://000022.awsstudygroup.com/> |
| 3-4 | - Continue Lambda study <br>- Review how a Lambda receives input and returns a response <br>- Note what needs to be logged for troubleshooting | 26/05/2026 | 27/05/2026 | <https://000022.awsstudygroup.com/> |
| 4-5 | - Learn the basic API Gateway request flow <br>- Understand how a frontend request can invoke backend logic | 27/05/2026 | 28/05/2026 | PeriodIQ API notes |
| 5-6 | - Map Lambda and API Gateway to PeriodIQ <br>- Identify where `POST /api/workoutplans/generate` fits in the project | 28/05/2026 | 29/05/2026 | PeriodIQ API notes |
| 6 | - Draft a simple request/response shape for Workout Plan generation <br>- Record early DynamoDB output notes for generated plans | 29/05/2026 | 29/05/2026 | PeriodIQ Rule Engine notes |


### Week 6 Achievements:

* Understood Lambda as the compute layer for a serverless backend.
* Joined the initial PeriodIQ team meeting and understood the 7-layer serverless architecture and role division.
* Learned the basic idea of API Gateway calling Lambda from a frontend request.
* Mapped the serverless request path to the PeriodIQ workout generation endpoint.
* Drafted the first simple input and output notes for the Rule Engine.
* Clarified that my focus was the workout generation logic, not every service in the full architecture.
