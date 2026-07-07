---
title: "Week 10 Worklog"
date: 2024-01-01
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Complete the user-facing Workout Plan feature for PeriodIQ.
* Verify that frontend input creates a valid 4-week plan through the backend API.
* Make the Rule Engine output visible and understandable on the product screen.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Build or refine the Workout Plan form in the React/Vite SPA hosted on S3 | 22/06/2026 | 22/06/2026 | PeriodIQ frontend source code |
| 3 | - Connect the Generate 4-Week Plan button to `POST /api/workoutplans/generate` through API Gateway | 23/06/2026 | 23/06/2026 | PeriodIQ API integration code |
| 4 | - Verify the generated plan appears in My Plans and can be opened through View Detail | 24/06/2026 | 24/06/2026 | PeriodIQ product test screenshots<br><https://d1di1pzmfypszp.cloudfront.net> |
| 5 | - Validate UI output: week-by-week progression, day split, exercise list, sets, reps, RPE, rest time, and target weight | 25/06/2026 | 25/06/2026 | PeriodIQ Workout Plan UI checklist<br><https://d1di1pzmfypszp.cloudfront.net> |
| 6 | - Confirm the periodization result: Week 1 base volume, Week 2 overload, Week 3 peak intensity, and Week 4 deload | 26/06/2026 | 26/06/2026 | PeriodIQ Rule Engine output samples |


### Week 10 Achievements:

* Completed the main user-facing product flow for my role.
* Verified that the frontend can call the generation API successfully.
* Confirmed that generated plans are visible in the user's plan list and detail page.
* Validated that Rule Engine output includes training volume, intensity, rest time, and target weight.
* Confirmed that the deload week appears as expected in the 4-week program.
