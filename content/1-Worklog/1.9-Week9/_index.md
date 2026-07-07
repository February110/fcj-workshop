---
title: "Week 9 Worklog"
date: 2024-01-01
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Start implementing my PeriodIQ role: Rule Engine & Workout Generation.
* Connect the planned algorithm to real backend and frontend components.
* Prepare test cases for multiple user profiles and training goals.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Review the PeriodIQ team architecture and confirm my service scope: Lambda API Handler, Lambda Rule Engine, and S3 Workout Plan UI | 15/06/2026 | 15/06/2026 | PeriodIQ team architecture notes |
| 3 | - Implement or refine the `/api/workoutplans/generate` request handling path and service-layer call | 16/06/2026 | 16/06/2026 | PeriodIQ API handler source code |
| 4 | - Implement the main Rule Engine stages: Volume Filter, Conflict Resolution, and Progression Builder | 17/06/2026 | 17/06/2026 | PeriodIQ Rule Engine source code |
| 5 | - Add test scenarios for Hypertrophy, Endurance, beginner/intermediate users, different days per week, and physical limitations | 18/06/2026 | 18/06/2026 | PeriodIQ Rule Engine test scenarios |
| 6 | - Coordinate with other members on data contracts: user profile input, WorkoutPlan output, and SQS message after plan generation | 19/06/2026 | 19/06/2026 | PeriodIQ team integration notes |


### Week 9 Achievements:

* Started the actual PeriodIQ implementation for my Person 2 role.
* Connected the workout generation endpoint to backend service logic.
* Implemented the main rule stages needed for a 4-week plan.
* Prepared scenario-based tests for different user training inputs.
* Clarified integration contracts with Auth and Async Notification flows without changing my Person 2 scope.
