---
title: "EKS Pod Identity Session Policies"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# Session Policies trong Amazon EKS Pod Identity

Blog này giới thiệu session policies trong Amazon EKS Pod Identity. Tính năng này giúp team áp dụng IAM permissions chính xác hơn cho Kubernetes workloads mà không cần tạo quá nhiều IAM roles riêng biệt.

## Vấn đề

Trong các môi trường Kubernetes lớn, nhiều ứng dụng chạy dưới dạng các pod riêng và cần quyền AWS khác nhau. Nếu tạo một IAM role cho từng biến thể quyền nhỏ, hệ thống sẽ khó quản lý. Ngược lại, dùng một role quá rộng cho nhiều pod sẽ làm yếu nguyên tắc least privilege.

## Session Policies hỗ trợ như thế nào

Session policies cho phép giới hạn effective permissions của một pod session. Thay vì tạo nhiều IAM roles, team có thể dùng một base role và gắn policy cụ thể hơn ở thời điểm tạo session. Cách này giúp kiểm soát quyền chi tiết hơn nhưng vẫn giữ việc quản lý IAM role đơn giản.

## Lợi ích

* Giảm tình trạng IAM role sprawl trong các EKS clusters lớn.
* Giúp áp dụng least privilege dễ hơn cho từng workload.
* Tăng bảo mật bằng cách thu hẹp quyền của pod.
* Đơn giản hóa vận hành so với việc tạo quá nhiều dedicated roles.

## Bài học rút ra

EKS Pod Identity session policies hữu ích cho các team cần cả bảo mật lẫn khả năng mở rộng. Tính năng này giúp platform team quản lý AWS permissions cho Kubernetes workloads linh hoạt hơn mà vẫn giữ được ranh giới least privilege.
