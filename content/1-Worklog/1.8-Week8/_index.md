---
title: "Week 8 Worklog"
date: 2024-01-01
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Design the first practical version of the Rule Engine logic for PeriodIQ.
* Break the algorithm into a small number of understandable rule stages.
* Prepare the DynamoDB output structure needed by the frontend detail page.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 1 | - Review the training inputs needed by the Rule Engine <br>- Confirm which fields are required for the first version | 08/06/2026 | 08/06/2026 | PeriodIQ Rule Engine design notes |
| 2 | - Design Volume Filter at a basic level <br>- Decide how goal, fitness level, and days per week affect weekly volume | 09/06/2026 | 10/06/2026 | PeriodIQ training rule notes |
| 3 | - Design simple Conflict Resolution rules <br>- Avoid obviously unsafe combinations and overloaded training days | 10/06/2026 | 11/06/2026 | PeriodIQ training rule notes |
| 4 | - Design the first Progression Builder draft <br>- Plan Week 1 base, Week 2 increase, Week 3 harder week, and Week 4 deload | 11/06/2026 | 12/06/2026 | PeriodIQ periodization notes |
| 5 | - Draft the DynamoDB output structure for `WorkoutPlan.Weeks` <br>- Keep the output focused on week, day, exercise, sets, reps, and target weight | 12/06/2026 | 12/06/2026 | PeriodIQ DynamoDB schema notes |


### Week 8 Achievements:

* Designed the first version of the PeriodIQ Rule Engine stages.
* Defined a simple 4-week periodization structure.
* Planned basic safety rules without over-expanding the algorithm.
* Drafted the nested DynamoDB output needed by the frontend detail page.
* Kept async notification work outside my main Person 2 implementation scope.
