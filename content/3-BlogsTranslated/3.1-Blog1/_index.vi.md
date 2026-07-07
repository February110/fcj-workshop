---
title: "Subdomain Takeover"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Subdomain Takeover: Khi một DNS record bị quên trở thành attack vector

Blog này giải thích cách Subdomain Takeover có thể xảy ra khi DNS record vẫn còn tồn tại sau khi tài nguyên AWS phía sau đã bị xóa. Ví dụ, một record trong Route 53 vẫn có thể trỏ đến S3 static website endpoint, CloudFront distribution, Elastic Beanstalk environment hoặc một cloud service khác không còn tồn tại.

Khi tài nguyên gốc bị xóa nhưng DNS record vẫn còn, attacker có thể tạo lại hoặc chiếm một tài nguyên tương thích và phục vụ nội dung dưới subdomain bị bỏ quên. Một lỗi cleanup nhỏ vì vậy có thể trở thành rủi ro bảo mật.

## Ý chính

* Dangling DNS record là nguyên nhân phổ biến dẫn đến subdomain takeover.
* Rủi ro tăng cao khi DNS records không được rà soát sau khi xóa S3 bucket, CloudFront distribution hoặc application environment.
* Route 53 nên được xem là một phần của attack surface, không chỉ là thành phần networking.
* Có thể tự động phát hiện bằng cách đối chiếu DNS records với tài nguyên thật trong AWS account.

## Ý tưởng phát hiện trên AWS

Workflow phát hiện được đề xuất sử dụng các dịch vụ AWS:

1. AWS Config ghi nhận thay đổi của các tài nguyên được hỗ trợ.
2. Lambda kiểm tra Route 53 hosted zones và DNS records.
3. Function đối chiếu DNS targets với các tài nguyên hiện có như S3, CloudFront và Elastic Beanstalk.
4. Nếu phát hiện dangling record, hệ thống gửi finding đến Security Hub và gửi thông báo qua SNS.

## Bài học rút ra

Subdomain takeover có thể phòng tránh nếu team duy trì DNS hygiene tốt. Mỗi lần xóa tài nguyên nên đi kèm bước rà soát DNS, và DNS records nên được giám sát liên tục thay vì chỉ kiểm tra lúc deploy ban đầu.
