---
title : "Giới thiệu"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.1. </b> "
---

#### PeriodIQ là gì?

PeriodIQ là một ứng dụng serverless sinh giáo án tập gym cá nhân hoá trong 4 tuần dựa trên trình độ, cân nặng, mục tiêu tập luyện và Personal Record của người dùng, thông qua một rule engine (Volume Filter -> Conflict Resolution -> Progression Builder). Toàn bộ kiến trúc (16 dịch vụ AWS trải trên 8 tầng) được mô tả ở phần [Proposal](../../2-proposal/).

#### Team đã chia công việc như thế nào

| Mục | Vai trò | Dịch vụ AWS |
|---|---|---|
| Lê Hoài Huân | Auth & User Profile | Amazon Cognito, AWS WAF, Amazon CloudFront |
| **Trần Anh Tài (tôi)** | **Rule Engine & Sinh giáo án** | **Lambda (API Handler + Rule Engine), Amazon S3** |
| Lê Hữu Duy Hoàng | Tiến trình & Async Notification | Amazon SQS, Lambda Worker, Amazon SNS |
| Chương Tử Luân | Admin Panel & Data | Lambda Admin API, Amazon DynamoDB, API Gateway |
| Phạm Văn Sỹ | CI/CD & Monitoring | AWS CodePipeline, AWS CodeBuild, CloudFormation/SAM, Amazon CloudWatch |

#### Phạm vi của workshop này

Workshop này mô tả kiến trúc chung của team và tập trung vào **vai trò của tôi, Trần Anh Tài - Rule Engine & Sinh giáo án**. Phần của tôi kiểm tra luồng sinh giáo án từ frontend đến API Gateway, Lambda Rule Engine, DynamoDB và CloudWatch. Các mục còn lại tóm tắt các vai trò hỗ trợ do những thành viên khác phụ trách.

> **Project Note:** deployment live của PeriodIQ được giữ lại cho phần đánh giá cuối, nên báo cáo này không xoá tài nguyên production dùng chung của nhóm.
