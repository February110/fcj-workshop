---
title: "Hybrid Multi-Tenant Architecture"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# Xây dựng kiến trúc Hybrid Multi-Tenant cho Stateful Services trên AWS

Blog này tóm tắt một case study trên AWS Architecture Blog về hệ thống ad-serving của Amazon Ads. Mô hình ban đầu sử dụng một AWS account cho mỗi tenant, dẫn đến chi phí vận hành cao và thời gian onboarding chậm. Kiến trúc mới sử dụng mô hình hybrid multi-tenant để giữ được mức độ cô lập cần thiết nhưng giảm bớt việc lặp lại hạ tầng.

## Ý tưởng kiến trúc chính

Case study giới thiệu mô hình 3 tầng:

* **Tier:** nhóm các tenant có yêu cầu dịch vụ hoặc yêu cầu kinh doanh tương tự.
* **Cell:** giới hạn blast radius và cho phép scale từng nhóm tenant độc lập.
* **Infra Group:** chia sẻ các thành phần hạ tầng khi an toàn và tiết kiệm chi phí.

Mô hình này kết hợp các thành phần dedicated để đảm bảo isolation với các thành phần shared để tăng hiệu quả vận hành.

## Dịch vụ và pattern AWS

Thiết kế sử dụng nhiều building blocks của AWS:

* Route 53 weighted routing để chuyển traffic an toàn.
* Application Load Balancer rules để route traffic theo tenant.
* Amazon ECS clusters riêng khi cần isolation.
* AWS PrivateLink cho private connectivity dùng chung.
* Tự động hóa vận hành để giảm công sức onboarding tenant thủ công.

## Giá trị chính

Kết quả quan trọng nhất là cải thiện vận hành. Khi chuyển khỏi mô hình "một account cho mỗi tenant", team giảm thời gian onboarding tenant từ 52 ngày xuống còn 7 ngày nhưng vẫn giữ được mức isolation cần thiết cho stateful services.

## Bài học rút ra

Multi-tenant architecture không chỉ là chia sẻ tài nguyên. Một thiết kế thực tế cần cân bằng giữa isolation, chi phí, vận hành, tốc độ deploy và giới hạn phạm vi lỗi. Hybrid tenancy thường thực tế hơn so với việc chọn hoàn toàn siloed hoặc hoàn toàn shared infrastructure.
