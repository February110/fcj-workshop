---
title: "Tự đánh giá"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

Trong quá trình tham gia chương trình First Cloud Journey, tôi vừa học các dịch vụ AWS thông qua bài lab, vừa áp dụng kiến thức đó vào dự án cuối kỳ của nhóm là **PeriodIQ**.

Vai trò chính của tôi trong PeriodIQ là **Người 2 - Rule Engine & Sinh giáo án**. Tôi phụ trách luồng sinh giáo án, bao gồm API handler, Lambda Rule Engine, giao diện Workout Plan, kiểm tra output trong DynamoDB, kiểm tra CloudWatch logs và chuẩn bị minh chứng cho demo cuối.

Link dự án PeriodIQ đang chạy: <https://d1di1pzmfypszp.cloudfront.net>

### Tổng quan tự đánh giá

| STT | Tiêu chí | Tự đánh giá | Mức độ |
| --- | --- | --- | --- |
| 1 | Kiến thức chuyên môn và nền tảng AWS | Tôi nắm được các dịch vụ AWS chính dùng trong dự án, đặc biệt là Lambda, API Gateway, S3, DynamoDB, CloudWatch và SQS. | Tốt |
| 2 | Áp dụng kiến thức vào thực tế | Tôi áp dụng kiến thức từ lab vào dự án thật bằng cách kết nối frontend, backend API, logic Rule Engine và tài nguyên AWS. | Tốt |
| 3 | Tinh thần trách nhiệm | Tôi hoàn thành scope Người 2 được giao và chuẩn bị các minh chứng cần thiết cho báo cáo/workshop. | Tốt |
| 4 | Khả năng học hỏi | Tôi học thêm các dịch vụ AWS mới và điều chỉnh cách triển khai theo nhu cầu của dự án. | Tốt |
| 5 | Làm việc nhóm | Tôi phối hợp với các thành viên khác về user input, output `WorkoutPlan`, luồng xác thực và luồng thông báo bất đồng bộ. | Tốt |
| 6 | Giao tiếp | Tôi có thể báo cáo tiến độ và làm rõ yêu cầu tích hợp, nhưng vẫn cần chủ động trao đổi sớm hơn khi gặp vướng mắc. | Khá |
| 7 | Giải quyết vấn đề | Tôi xử lý các vấn đề tích hợp và kiểm tra trong dự án, đặc biệt ở API flow, output structure và logs. | Tốt |
| 8 | Viết tài liệu | Tôi đã tài liệu hóa project flow, AWS services, screenshots, logs và worklogs, nhưng vẫn có thể cải thiện độ nhất quán và chi tiết. | Khá |
| 9 | Quản lý thời gian | Tôi hoàn thành phần chính của dự án, nhưng một số nội dung báo cáo vẫn phải chỉnh sửa ở giai đoạn cuối. | Khá |
| 10 | Đóng góp tổng thể | Tôi đóng góp feature sinh giáo án hoạt động được và tài liệu hỗ trợ cho demo cuối của PeriodIQ. | Tốt |

### Điểm mạnh

* Hiểu rõ hơn về kiến trúc serverless thông qua việc làm dự án thật.
* Hoàn thành luồng Rule Engine và Workout Plan đúng với vai trò được giao.
* Biết cách liên kết phần triển khai kỹ thuật với minh chứng báo cáo như screenshots, logs, DynamoDB records và live CloudFront URL.
* Cải thiện khả năng đọc thông tin trên AWS Console và kiểm tra một feature hoạt động end to end.

### Điểm cần cải thiện

* Cần lên kế hoạch sớm hơn để chuẩn bị nội dung báo cáo và screenshots.
* Cần viết integration contracts rõ hơn trước khi triển khai, đặc biệt với các cấu trúc dữ liệu dùng chung.
* Cần bổ sung nhiều test cases hơn cho các mục tiêu tập luyện, fitness level, physical limitations và edge cases khác nhau.
* Cần trao đổi sớm hơn khi vấn đề triển khai có ảnh hưởng đến thành viên khác trong nhóm.

### Nhận xét tổng thể

Kỳ thực tập giúp tôi chuyển từ việc học từng dịch vụ AWS riêng lẻ sang hiểu cách các dịch vụ phối hợp trong một ứng dụng thật. Thông qua PeriodIQ, tôi có thêm kinh nghiệm thực tế trong việc xây dựng một feature serverless, kiểm tra feature đó trên AWS và tài liệu hóa kết quả thành báo cáo có cấu trúc.
