---
title: "Worklog Tuần 6"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Học các pattern backend serverless và map vào Rule Engine của PeriodIQ.
* Tách rõ ghi chú học lab AWS với ghi chú triển khai dự án PeriodIQ.
* Chuẩn bị ghi chú thiết kế backend cho endpoint sinh giáo án.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Học Lambda handler structure, runtime settings, environment variables và execution role | 25/05/2026 | 25/05/2026 | <https://000022.awsstudygroup.com/> |
| 3 | - Áp dụng phần học Lambda vào bản nháp Rule Engine của PeriodIQ <br>- Xác định cách Rule Engine có thể chạy như một API path backed by Lambda | 26/05/2026 | 26/05/2026 | Ghi chú thiết kế backend PeriodIQ |
| 4 | - Học thiết kế route API Gateway và cách Lambda truy cập DynamoDB | 27/05/2026 | 27/05/2026 | <https://000066.awsstudygroup.com/><br><https://000078.awsstudygroup.com/><br><https://000060.awsstudygroup.com/> |
| 5 | - Phác thảo request/response cho `POST /api/workoutplans/generate` <br>- Xác định các field cần có cho giáo án đã sinh như `Goal`, `FitnessLevel`, `StartDate`, `EndDate` và `Weeks` | 28/05/2026 | 28/05/2026 | Ghi chú API và schema DynamoDB của PeriodIQ |
| 6 | - Tổng hợp request path serverless cho vai trò của tôi: S3 frontend -> API Gateway -> Lambda Rule Engine -> DynamoDB -> CloudWatch | 29/05/2026 | 29/05/2026 | Ghi chú kiến trúc PeriodIQ |


### Kết quả đạt được tuần 6:

* Xác định các backend services cần cho chức năng sinh giáo án.
* Phác thảo API route và payload structure cho plan generation.
* Xác định các field output DynamoDB mà Rule Engine cần tạo.
* Tách link lab cho phần học AWS và ghi chú PeriodIQ cho phần làm dự án.
* Chuẩn bị được serverless architecture path rõ ràng cho scope Người 2.
