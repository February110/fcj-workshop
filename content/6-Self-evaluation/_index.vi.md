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

| STT | Tiêu chí | Mô tả | Tốt | Khá | Trung bình |
| --- | --- | --- | --- | --- | --- |
| 1 | Kiến thức chuyên môn & kỹ năng | Hiểu nền tảng AWS, biết áp dụng kiến thức vào thực tế, sử dụng công cụ cần thiết và đảm bảo chất lượng công việc. | <span style="color:#22c55e;font-weight:700;">✓</span> | ☐ | ☐ |
| 2 | Áp dụng kiến thức vào thực tế | Áp dụng kiến thức từ lab vào PeriodIQ thông qua Workout Plan UI, API route, Lambda Rule Engine, DynamoDB output và CloudWatch logs. | <span style="color:#22c55e;font-weight:700;">✓</span> | ☐ | ☐ |
| 3 | Tinh thần trách nhiệm | Hoàn thành scope Người 2 được giao và chuẩn bị minh chứng workshop/báo cáo phục vụ đánh giá. | <span style="color:#22c55e;font-weight:700;">✓</span> | ☐ | ☐ |
| 4 | Khả năng học hỏi | Học thêm các dịch vụ AWS khi cần và điều chỉnh cách triển khai theo yêu cầu của dự án. | <span style="color:#22c55e;font-weight:700;">✓</span> | ☐ | ☐ |
| 5 | Làm việc nhóm | Phối hợp với thành viên khác về input fields, cấu trúc output `WorkoutPlan`, phần handoff xác thực và demo cuối. | <span style="color:#22c55e;font-weight:700;">✓</span> | ☐ | ☐ |
| 6 | Giao tiếp | Có báo cáo tiến độ và làm rõ yêu cầu tích hợp, nhưng vẫn cần chủ động báo sớm hơn khi gặp vướng mắc. | ☐ | <span style="color:#22c55e;font-weight:700;">✓</span> | ☐ |
| 7 | Giải quyết vấn đề | Xử lý các vấn đề tích hợp và kiểm tra liên quan đến API flow, output structure, DynamoDB records và logs. | <span style="color:#22c55e;font-weight:700;">✓</span> | ☐ | ☐ |
| 8 | Viết tài liệu | Tài liệu hóa AWS services, screenshots, logs, worklogs và product flow, nhưng vẫn cần cải thiện độ nhất quán. | ☐ | <span style="color:#22c55e;font-weight:700;">✓</span> | ☐ |
| 9 | Quản lý thời gian | Hoàn thành phần chính đúng tiến độ, nhưng một số nội dung báo cáo và screenshots vẫn phải chỉnh ở giai đoạn cuối. | ☐ | <span style="color:#22c55e;font-weight:700;">✓</span> | ☐ |
| 10 | Đóng góp tổng thể | Đóng góp feature sinh giáo án hoạt động được và tài liệu hỗ trợ cho demo cuối của PeriodIQ. | <span style="color:#22c55e;font-weight:700;">✓</span> | ☐ | ☐ |

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
