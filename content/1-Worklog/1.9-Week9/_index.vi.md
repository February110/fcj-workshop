---
title: "Worklog Tuần 9"
date: 2024-01-01
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Bắt đầu triển khai vai trò của tôi trong PeriodIQ: Rule Engine & Sinh giáo án.
* Kết nối thuật toán đã thiết kế với backend API path theo từng bước nhỏ.
* Chuẩn bị một vài test case đơn giản thay vì cố bao phủ mọi scenario tập luyện.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 1 | - Rà soát kiến trúc nhóm PeriodIQ <br>- Xác nhận scope của tôi: Lambda API Handler, Lambda Rule Engine và hỗ trợ Workout Plan UI | 15/06/2026 | 15/06/2026 | Ghi chú kiến trúc nhóm PeriodIQ |
| 2 | - Implement hoặc refine request handling path `/api/workoutplans/generate` <br>- Kết nối endpoint với service-layer call | 16/06/2026 | 17/06/2026 | Source code API handler của PeriodIQ |
| 3 | - Implement Rule Engine từng phần <br>- Bắt đầu với Volume Filter và Conflict Resolution đơn giản | 17/06/2026 | 18/06/2026 | Source code Rule Engine của PeriodIQ |
| 4 | - Thêm logic Progression Builder đầu tiên <br>- Sinh output giáo án 4 tuần cơ bản | 18/06/2026 | 19/06/2026 | Source code Rule Engine của PeriodIQ |
| 5 | - Chạy một vài bài test generation cơ bản <br>- Đồng bộ với team về input và output fields mà module khác sử dụng | 19/06/2026 | 19/06/2026 | Ghi chú tích hợp nhóm PeriodIQ |


### Kết quả đạt được tuần 9:

* Bắt đầu implementation thật cho vai trò Người 2 trong PeriodIQ.
* Kết nối workout generation endpoint với backend service logic.
* Implement Rule Engine theo từng stage nhỏ thay vì làm tất cả cùng lúc.
* Sinh được output giáo án 4 tuần cơ bản đầu tiên để test.
* Làm rõ input và output contracts với các thành viên khác trong khi vẫn giữ scope tập trung.
