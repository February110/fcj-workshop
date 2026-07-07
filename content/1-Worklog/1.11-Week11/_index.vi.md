---
title: "Worklog Tuần 11"
date: 2024-01-01
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:

* Xác minh các AWS resources đứng sau vai trò Rule Engine của tôi trong PeriodIQ.
* Xác nhận request path thật hoạt động từ frontend đến API Gateway, Lambda, DynamoDB và CloudWatch.
* Thu thập screenshots và log thật cho báo cáo workshop.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 1 | - Kiểm tra Lambda function `periodiq-rule-engine-dev` <br>- Xem trigger, runtime, description và thời điểm deploy gần nhất | 29/06/2026 | 30/06/2026 | Screenshot AWS Console - Lambda |
| 2 | - Kiểm tra API Gateway route `ANY /api/workoutplans/generate` <br>- Xác nhận route trỏ đến Rule Engine Lambda path | 30/06/2026 | 01/07/2026 | Screenshot AWS Console - API Gateway |
| 3 | - Kiểm tra S3 frontend bucket `periodiq-frontend-dev-345798130457` có các file build React/Vite đã deploy <br>- Mở link CloudFront project đang chạy | 01/07/2026 | 01/07/2026 | Screenshot AWS Console - S3 deployment<br><https://d1di1pzmfypszp.cloudfront.net> |
| 4 | - Kiểm tra các item `WorkoutPlan` đã sinh trong DynamoDB <br>- Xem nested output `Weeks` do Rule Engine tạo | 02/07/2026 | 03/07/2026 | Screenshot bảng DynamoDB |
| 5 | - Tạo giáo án và kiểm tra CloudWatch logs có `POST /api/workoutplans/generate`, HTTP 200 và Lambda START/END/REPORT | 03/07/2026 | 03/07/2026 | CloudWatch log evidence |


### Kết quả đạt được tuần 11:

* Xác minh các AWS services thật được dùng trong luồng sinh giáo án của tôi.
* Xác nhận path: S3 frontend -> API Gateway -> Lambda Rule Engine -> DynamoDB -> CloudWatch logs.
* Thu thập evidence cho các trang workshop Lambda, API Gateway, S3, DynamoDB và CloudWatch.
* Kiểm tra generated `WorkoutPlan.Weeks` output trong DynamoDB.
* Chuẩn bị nội dung báo cáo chính xác dựa trên tài nguyên AWS thật thay vì mô tả service chung chung.
