---
title: "Chia sẻ, đóng góp ý kiến"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 7. </b> "
---

### Đánh giá chung

Chương trình First Cloud Journey mang lại cho tôi một lộ trình học cloud khá thực tế. Chương trình không chỉ dừng lại ở việc đọc tài liệu hoặc làm theo bài lab, mà còn yêu cầu áp dụng kiến thức đã học vào dự án cuối kỳ của nhóm. Điều này giúp quá trình thực tập sát với thực tế hơn và giúp tôi hiểu cách các dịch vụ AWS được sử dụng trong một ứng dụng thật.

### Trải nghiệm học tập

Các bài lab AWS giúp tôi xây dựng nền tảng ban đầu. Tôi bắt đầu từ các dịch vụ cơ bản như IAM, VPC, EC2, S3 và DynamoDB, sau đó chuyển sang các dịch vụ liên quan trực tiếp đến dự án PeriodIQ như Lambda, API Gateway, CloudWatch, SQS và triển khai frontend bằng S3/CloudFront.

Phần giá trị nhất là áp dụng các dịch vụ đó vào PeriodIQ. Với vai trò **Người 2 - Rule Engine & Sinh giáo án**, tôi phải nhìn tổng thể luồng hoạt động thay vì chỉ học từng dịch vụ riêng lẻ: user nhập thông tin, frontend gọi API, Lambda xử lý, DynamoDB lưu output, CloudWatch ghi logs và giao diện hiển thị kết quả cuối.

### Sự hỗ trợ từ mentor và team

Mentor và team hỗ trợ khá tốt khi tôi gặp câu hỏi về AWS services, cấu trúc báo cáo và cách triển khai dự án. Phần hướng dẫn giúp tôi tránh việc chỉ chép lại các bước lab, thay vào đó tập trung giải thích vì sao mỗi dịch vụ được dùng trong dự án của mình.

Việc làm việc nhóm cũng rất quan trọng vì PeriodIQ được chia thành nhiều vai trò. Phần của tôi phụ thuộc vào input từ luồng xác thực và cũng cần tạo output để các luồng khác sử dụng, ví dụ dữ liệu `WorkoutPlan` và message bất đồng bộ sau khi sinh giáo án.

### Điều tôi thấy hữu ích nhất

* Các bài lab thực hành giúp tôi hiểu khái niệm cloud nhanh hơn.
* Dự án cuối kỳ giúp việc học sát thực tế hơn.
* Cấu trúc báo cáo và workshop giúp tôi biết cách trình bày công việc kỹ thuật rõ ràng.
* Bản deploy PeriodIQ thật giúp tôi có kết quả cụ thể để kiểm tra và trình bày.

Link dự án PeriodIQ đang chạy: <https://d1di1pzmfypszp.cloudfront.net>

### Góp ý cải thiện

* Nên có checklist rõ hơn cho minh chứng dự án cuối kỳ, ví dụ screenshots, logs và sơ đồ kiến trúc cần chuẩn bị.
* Có thể bổ sung thêm ví dụ về cách chuyển kiến thức từ bài lab AWS thành nội dung tài liệu dự án.
* Nên khuyến khích các nhóm xác định integration contracts sớm hơn, đặc biệt là API payload và database schema dùng chung.
* Nên tiếp tục giữ yêu cầu làm dự án cuối kỳ vì phần này giúp thực tập sinh liên kết kiến thức AWS với triển khai thực tế.

### Nhận xét cuối

Nhìn chung, kỳ thực tập này hữu ích vì kết hợp được việc học, triển khai, làm việc nhóm và viết tài liệu. Sau chương trình, tôi hiểu rõ hơn về kiến trúc serverless trên AWS và cách trình bày một dự án cloud một cách có hệ thống.
