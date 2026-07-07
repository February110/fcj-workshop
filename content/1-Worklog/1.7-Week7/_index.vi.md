---
title: "Worklog Tuần 7"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Học cách frontend gọi backend API khi user đã xác thực.
* Áp dụng phần học đó vào luồng Workout Plan dành cho user trong PeriodIQ.
* Xác định input tối thiểu mà Rule Engine cần.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Học Cognito token flow và cách frontend gửi authenticated requests đến backend APIs | 01/06/2026 | 01/06/2026 | <https://000081.awsstudygroup.com/> |
| 3 | - Áp dụng phần học authentication vào contract gọi API Workout Plan của PeriodIQ | 02/06/2026 | 02/06/2026 | Ghi chú API PeriodIQ |
| 4 | - Phác thảo các field của form Workout Plan: goal, fitness level, days/week, start date, current 1RM, limitations và equipment | 03/06/2026 | 03/06/2026 | Ghi chú thiết kế UI PeriodIQ |
| 5 | - Định nghĩa cách hiển thị giáo án đã sinh trong UI: summary, My Plans list, detail page, week/day split, exercises, sets, reps, RPE, rest time và target weight | 04/06/2026 | 04/06/2026 | Ghi chú màn hình Workout Plan của PeriodIQ |
| 6 | - Chuẩn bị acceptance criteria cho product flow: generate plan, save plan, open detail, show deload week và show calculated target weights | 05/06/2026 | 05/06/2026 | Checklist kiểm thử feature PeriodIQ |


### Kết quả đạt được tuần 7:

* Xác định luồng người dùng Workout Plan trước khi triển khai.
* Liệt kê chính xác input mà Rule Engine cần.
* Áp dụng kiến thức authenticated API vào contract của generation endpoint.
* Định nghĩa cách giáo án 4 tuần được hiển thị cho user.
* Tạo acceptance criteria để kiểm thử feature ở các tuần sau.
