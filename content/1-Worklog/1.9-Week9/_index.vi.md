---
title: "Worklog Tuần 9"
date: 2024-01-01
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Bắt đầu triển khai vai trò của tôi trong PeriodIQ: Rule Engine & Sinh giáo án.
* Kết nối thuật toán đã thiết kế với backend và frontend components thật.
* Chuẩn bị test cases cho nhiều user profiles và training goals.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Rà soát kiến trúc nhóm PeriodIQ và xác nhận scope của tôi: Lambda API Handler, Lambda Rule Engine và S3 Workout Plan UI | 15/06/2026 | 15/06/2026 | Ghi chú kiến trúc nhóm PeriodIQ |
| 3 | - Implement hoặc refine request handling path `/api/workoutplans/generate` và service-layer call | 16/06/2026 | 16/06/2026 | Source code API handler của PeriodIQ |
| 4 | - Implement các stage chính của Rule Engine: Volume Filter, Conflict Resolution và Progression Builder | 17/06/2026 | 17/06/2026 | Source code Rule Engine của PeriodIQ |
| 5 | - Thêm test scenarios cho Hypertrophy, Endurance, beginner/intermediate users, số buổi mỗi tuần khác nhau và physical limitations | 18/06/2026 | 18/06/2026 | Test scenarios Rule Engine của PeriodIQ |
| 6 | - Phối hợp với các thành viên khác về data contracts: user profile input, WorkoutPlan output và SQS message sau khi sinh giáo án | 19/06/2026 | 19/06/2026 | Ghi chú tích hợp nhóm PeriodIQ |


### Kết quả đạt được tuần 9:

* Bắt đầu implementation thật cho vai trò Người 2 trong PeriodIQ.
* Kết nối workout generation endpoint với backend service logic.
* Implement các rule stages chính cần cho giáo án 4 tuần.
* Chuẩn bị scenario-based tests cho nhiều input tập luyện khác nhau.
* Làm rõ integration contracts với luồng Auth và Async Notification nhưng vẫn giữ đúng scope Người 2 của tôi.
