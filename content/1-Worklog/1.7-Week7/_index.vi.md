---
title: "Worklog Tuần 7"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Học vừa đủ luồng authenticated API để hiểu cách gửi request sinh giáo án.
* Áp dụng phần học đó vào luồng Workout Plan dành cho user trong PeriodIQ.
* Xác định input tối thiểu cho phiên bản Rule Engine đầu tiên.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 1 | - Học ý tưởng cơ bản về Cognito/authenticated request <br>- Hiểu vì sao frontend cần gửi authenticated API request | 01/06/2026 | 02/06/2026 | <https://000081.awsstudygroup.com/> |
| 2 | - Tiếp tục ghi chú API access <br>- Áp dụng ý tưởng vào request generate Workout Plan của PeriodIQ | 02/06/2026 | 03/06/2026 | Ghi chú API PeriodIQ |
| 3 | - Phác thảo các field đầu tiên của form Workout Plan <br>- Tập trung vào goal, fitness level, số ngày tập mỗi tuần và start date | 03/06/2026 | 04/06/2026 | Ghi chú thiết kế UI PeriodIQ |
| 4 | - Định nghĩa cách hiển thị giáo án cơ bản <br>- Gồm plan summary, My Plans list và cấu trúc detail page | 04/06/2026 | 05/06/2026 | Ghi chú màn hình Workout Plan của PeriodIQ |
| 5 | - Chuẩn bị checklist kiểm thử đơn giản cho product flow: generate plan, save plan và open detail | 05/06/2026 | 05/06/2026 | Checklist kiểm thử feature PeriodIQ |


### Kết quả đạt được tuần 7:

* Hiểu luồng authenticated API request cơ bản được frontend sử dụng.
* Xác định phiên bản đầu tiên của luồng người dùng Workout Plan.
* Giảm scope form ban đầu còn các input cần thiết cho generation.
* Chuẩn bị cấu trúc UI đơn giản để hiển thị generated plans.
* Tạo checklist kiểm thử thực tế cho các tuần triển khai sau.
