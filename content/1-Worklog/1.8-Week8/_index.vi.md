---
title: "Worklog Tuần 8"
date: 2024-01-01
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Thiết kế phiên bản thực tế đầu tiên của logic Rule Engine trong PeriodIQ.
* Tách thuật toán thành một số stage dễ hiểu.
* Chuẩn bị DynamoDB output structure cần cho trang detail của frontend.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 1 | - Rà soát input tập luyện mà Rule Engine cần <br>- Xác nhận các field bắt buộc cho phiên bản đầu tiên | 08/06/2026 | 08/06/2026 | Ghi chú thiết kế Rule Engine PeriodIQ |
| 2 | - Thiết kế Volume Filter ở mức cơ bản <br>- Quyết định goal, fitness level và số ngày tập ảnh hưởng weekly volume như thế nào | 09/06/2026 | 10/06/2026 | Ghi chú training rules của PeriodIQ |
| 3 | - Thiết kế simple Conflict Resolution rules <br>- Tránh các tổ hợp quá tải hoặc lịch tập không an toàn rõ ràng | 10/06/2026 | 11/06/2026 | Ghi chú training rules của PeriodIQ |
| 4 | - Thiết kế bản nháp Progression Builder đầu tiên <br>- Lên plan Week 1 base, Week 2 tăng nhẹ, Week 3 nặng hơn và Week 4 deload | 11/06/2026 | 12/06/2026 | Ghi chú periodization của PeriodIQ |
| 5 | - Phác thảo DynamoDB output structure cho `WorkoutPlan.Weeks` <br>- Giữ output tập trung vào week, day, exercise, sets, reps và target weight | 12/06/2026 | 12/06/2026 | Ghi chú schema DynamoDB của PeriodIQ |


### Kết quả đạt được tuần 8:

* Thiết kế phiên bản đầu tiên của các stage trong PeriodIQ Rule Engine.
* Xác định cấu trúc periodization 4 tuần đơn giản.
* Lên basic safety rules mà không mở rộng thuật toán quá mức.
* Phác thảo nested DynamoDB output cần cho frontend detail page.
* Giữ phần async notification ngoài scope triển khai chính của Người 2.
