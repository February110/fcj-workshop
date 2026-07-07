---
title: "Worklog Tuần 8"
date: 2024-01-01
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Thiết kế logic Rule Engine để sinh giáo án tập 4 tuần trong PeriodIQ.
* Tách thuật toán thành các nhóm luật rõ ràng: Volume Filter, Conflict Resolution và Progression Builder.
* Chuẩn bị integration points của dự án với DynamoDB và luồng async notification.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Thiết kế luật Volume Filter dựa trên goal, fitness level và days per week | 08/06/2026 | 08/06/2026 | Ghi chú thiết kế Rule Engine PeriodIQ |
| 3 | - Thiết kế Conflict Resolution rules cho physical limitations, CNS stress và unsafe overload conditions | 09/06/2026 | 09/06/2026 | Ghi chú training rules của PeriodIQ |
| 4 | - Thiết kế Progression Builder cho Week 1 base volume, Week 2 volume overload, Week 3 peak intensity và Week 4 deload | 10/06/2026 | 10/06/2026 | Ghi chú periodization của PeriodIQ |
| 5 | - Định nghĩa DynamoDB output structure cho `WorkoutPlan.Weeks`, gồm week, day, exercise, set, rep, RPE, rest time và target weight | 11/06/2026 | 11/06/2026 | Ghi chú schema DynamoDB của PeriodIQ |
| 6 | - Rà soát async continuation sau khi sinh giáo án, gồm SQS message và luồng progress/notification về sau | 12/06/2026 | 12/06/2026 | Ghi chú tích hợp nhóm PeriodIQ |


### Kết quả đạt được tuần 8:

* Thiết kế các stage thuật toán chính cho Rule Engine của PeriodIQ.
* Xác định cấu trúc periodization 4 tuần mong đợi.
* Lên kế hoạch cách physical limitations và recovery rules ảnh hưởng giáo án được sinh.
* Định nghĩa nested DynamoDB output dùng cho trang detail của frontend.
* Chuẩn bị handoff giữa output của Rule Engine và luồng async processing.
