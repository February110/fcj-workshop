---
title: "Week 9 Worklog"
date: 2024-01-01
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Start implementing my PeriodIQ role: Rule Engine & Workout Generation.
* Connect the planned algorithm to the backend API path in small steps.
* Prepare a few simple test cases instead of trying to cover every training scenario.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 1 | - Review the PeriodIQ team architecture <br>- Confirm my scope: Lambda API Handler, Lambda Rule Engine, and Workout Plan UI support | 15/06/2026 | 15/06/2026 | PeriodIQ team architecture notes |
| 2 | - Implement or refine the `/api/workoutplans/generate` request handling path <br>- Connect the endpoint to the service-layer call | 16/06/2026 | 17/06/2026 | PeriodIQ API handler source code |
| 3 | - Implement the Rule Engine gradually <br>- Start with Volume Filter and simple Conflict Resolution | 17/06/2026 | 18/06/2026 | PeriodIQ Rule Engine source code |
| 4 | - Add the first Progression Builder logic <br>- Generate a basic 4-week plan output | 18/06/2026 | 19/06/2026 | PeriodIQ Rule Engine source code |
| 5 | - Run a few basic generation tests <br>- Sync with teammates on input and output fields used by other modules | 19/06/2026 | 19/06/2026 | PeriodIQ team integration notes |


### Week 9 Achievements:

* Started the actual PeriodIQ implementation for my Person 2 role.
* Connected the workout generation endpoint to backend service logic.
* Implemented the Rule Engine in smaller stages instead of all at once.
* Generated the first basic 4-week plan output for testing.
* Clarified input and output contracts with other team members while keeping my scope focused.
