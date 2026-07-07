---
title: "Worklog Tuần 10"
date: 2024-01-01
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

* Hoàn thành feature Workout Plan dành cho user trong PeriodIQ.
* Xác minh input từ frontend có thể tạo giáo án 4 tuần hợp lệ thông qua backend API.
* Làm output của Rule Engine hiển thị rõ ràng trên màn hình sản phẩm.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Xây dựng hoặc refine form Workout Plan trong React/Vite SPA host trên S3 | 22/06/2026 | 22/06/2026 | Source code frontend PeriodIQ |
| 3 | - Kết nối nút Generate 4-Week Plan đến `POST /api/workoutplans/generate` thông qua API Gateway | 23/06/2026 | 23/06/2026 | Code tích hợp API của PeriodIQ |
| 4 | - Xác minh giáo án được sinh xuất hiện trong My Plans và có thể mở bằng View Detail | 24/06/2026 | 24/06/2026 | Screenshot kiểm thử sản phẩm PeriodIQ<br><https://d1di1pzmfypszp.cloudfront.net> |
| 5 | - Kiểm tra UI output: week-by-week progression, day split, exercise list, sets, reps, RPE, rest time và target weight | 25/06/2026 | 25/06/2026 | Checklist UI Workout Plan của PeriodIQ<br><https://d1di1pzmfypszp.cloudfront.net> |
| 6 | - Xác nhận kết quả periodization: Week 1 base volume, Week 2 overload, Week 3 peak intensity và Week 4 deload | 26/06/2026 | 26/06/2026 | Sample output Rule Engine của PeriodIQ |


### Kết quả đạt được tuần 10:

* Hoàn thành product flow chính dành cho user trong vai trò của tôi.
* Xác minh frontend gọi generation API thành công.
* Xác nhận giáo án đã sinh hiển thị trong plan list và detail page của user.
* Kiểm tra output Rule Engine gồm training volume, intensity, rest time và target weight.
* Xác nhận tuần deload xuất hiện đúng trong chương trình 4 tuần.
