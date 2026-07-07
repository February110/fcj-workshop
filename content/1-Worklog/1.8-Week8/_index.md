---
title: "Week 8 Worklog"
date: 2024-01-01
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Design the Rule Engine logic for generating a 4-week workout plan in PeriodIQ.
* Break the algorithm into clear rule stages: Volume Filter, Conflict Resolution, and Progression Builder.
* Prepare project integration points with DynamoDB and the asynchronous notification flow.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Design the Volume Filter rule based on goal, fitness level, and days per week | 08/06/2026 | 08/06/2026 | PeriodIQ Rule Engine design notes |
| 3 | - Design Conflict Resolution rules for physical limitations, CNS stress, and unsafe overload conditions | 09/06/2026 | 09/06/2026 | PeriodIQ training rule notes |
| 4 | - Design the Progression Builder for Week 1 base volume, Week 2 volume overload, Week 3 peak intensity, and Week 4 deload | 10/06/2026 | 10/06/2026 | PeriodIQ periodization notes |
| 5 | - Define the DynamoDB output structure for `WorkoutPlan.Weeks`, including week, day, exercise, set, rep, RPE, rest time, and target weight | 11/06/2026 | 11/06/2026 | PeriodIQ DynamoDB schema notes |
| 6 | - Review async continuation after plan generation, including SQS message and later progress/notification flow | 12/06/2026 | 12/06/2026 | PeriodIQ team integration notes |


### Week 8 Achievements:

* Designed the main algorithm stages for the PeriodIQ Rule Engine.
* Defined the expected 4-week periodization structure.
* Planned how physical limitations and recovery rules affect the generated plan.
* Defined the nested DynamoDB output used by the frontend detail page.
* Prepared the handoff between Rule Engine output and the async processing flow.
