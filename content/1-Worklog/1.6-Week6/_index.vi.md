---
title: "Worklog Tuần 6"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Bắt đầu học các dịch vụ backend serverless liên quan đến dự án PeriodIQ.
* Học Lambda và API Gateway chậm hơn để hiểu request flow.
* Chỉ map các khái niệm AWS phù hợp vào phần Rule Engine & Sinh giáo án.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Họp nhóm: review kiến trúc hệ thống PeriodIQ (thiết kế serverless 7 layer trên AWS) và chia dự án thành 5 nhóm vai trò, mỗi nhóm phụ trách 3-4 AWS services | 25/05/2026 | 25/05/2026 | Ghi chú họp nhóm PeriodIQ |
| 2-3 | - Học AWS Lambda fundamentals <br>- Hiểu function runtime, handler, event payload, IAM role và CloudWatch logs | 25/05/2026 | 26/05/2026 | <https://000022.awsstudygroup.com/> |
| 3-4 | - Tiếp tục học Lambda <br>- Xem Lambda nhận input và trả response như thế nào <br>- Ghi chú những gì cần log để troubleshoot | 26/05/2026 | 27/05/2026 | <https://000022.awsstudygroup.com/> |
| 4-5 | - Học basic API Gateway request flow <br>- Hiểu cách frontend request có thể gọi backend logic | 27/05/2026 | 28/05/2026 | Ghi chú API PeriodIQ |
| 5-6 | - Map Lambda và API Gateway vào PeriodIQ <br>- Xác định `POST /api/workoutplans/generate` nằm ở đâu trong project | 28/05/2026 | 29/05/2026 | Ghi chú API PeriodIQ |
| 6 | - Phác thảo request/response đơn giản cho Workout Plan generation <br>- Ghi chú output DynamoDB ban đầu cho generated plans | 29/05/2026 | 29/05/2026 | Ghi chú Rule Engine PeriodIQ |


### Kết quả đạt được tuần 6:

* Hiểu Lambda là compute layer cho backend serverless.
* Tham gia buổi họp nhóm đầu tiên của PeriodIQ và hiểu kiến trúc serverless 7 layer cùng cách chia vai trò trong nhóm.
* Hiểu ý tưởng cơ bản API Gateway gọi Lambda từ frontend request.
* Map request path serverless vào endpoint sinh giáo án của PeriodIQ.
* Phác thảo input và output đơn giản đầu tiên cho Rule Engine.
* Làm rõ trọng tâm của tôi là logic sinh giáo án, không phải toàn bộ mọi service trong kiến trúc.
