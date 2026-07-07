---
title: "Blogs đã đăng"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

# BLOGS ĐÃ ĐĂNG

Phần này liệt kê và giới thiệu các blog tôi đã đăng lên [AWS Study Group](https://awsstudygroup.com/).

### [Blog 1 - Subdomain Takeover: Khi một DNS record bị quên trở thành attack vector](3.1-Blog1/)

Blog này trình bày kỹ thuật tấn công Subdomain Takeover, trong đó một DNS record bị bỏ quên vẫn trỏ đến tài nguyên AWS đã bị xóa như S3, CloudFront hoặc Elastic Beanstalk có thể bị attacker chiếm lại. Bài viết giải thích cách tấn công xảy ra và đề xuất hướng phát hiện trên AWS bằng AWS Config và Lambda để đối chiếu Route 53 records với tài nguyên thật trong account, sau đó cảnh báo qua Security Hub và SNS.

### [Blog 2 - Xây dựng kiến trúc Hybrid Multi-Tenant cho Stateful Services trên AWS](3.2-Blog2/)

Blog này tóm tắt một case study trên AWS Architecture Blog về hệ thống ad-serving của Amazon Ads, chuyển từ mô hình tốn kém "một AWS account cho mỗi tenant" sang kiến trúc hybrid 3 tầng Tier-Cell-Infra Group, sử dụng Route 53 weighted routing, ALB rules theo từng tenant, ECS clusters riêng và PrivateLink dùng chung. Thiết kế này giúp giảm thời gian onboarding tenant từ 52 ngày xuống còn 7 ngày.

### [Blog 3 - Session Policies trong Amazon EKS Pod Identity](3.3-Blog3/)

Blog này giới thiệu tính năng session policies trong Amazon EKS Pod Identity. Tính năng này cho phép giới hạn IAM permissions linh hoạt và chính xác cho từng pod mà không cần tạo quá nhiều IAM roles riêng biệt, giúp áp dụng nguyên tắc least privilege hiệu quả hơn trong môi trường Kubernetes quy mô lớn.
