---
title : "Chương Tử Luân - Admin Panel & Data"
date : 2024-01-01
weight : 6
chapter : false
pre : " <b> 5.6. </b> "
---

Đây là phần mô tả vai trò **Admin Panel & Data** do Chương Tử Luân phụ trách trong dự án PeriodIQ. Vai trò này phụ trách ba dịch vụ AWS cốt lõi:

| Dịch vụ AWS | Vai trò |
|---|---|
| **Amazon DynamoDB** | Thiết kế toàn bộ schema 8 bảng, tạo bảng, GSI, seed data |
| **Lambda Admin API** | Xây dựng 4 controller backend (Exercise, Template, Rule, AdminStats) |
| **API Gateway (HTTP)** | Cấu hình routes, JWT Authorizer Cognito, CORS |

Ngoài ra, vai trò này bao gồm toàn bộ **Admin Panel frontend** — 4 trang quản trị (Dashboard, Exercises, Rules, Templates) — và unit test cho toàn bộ controller thuộc phạm vi này.

#### Nội dung

1. [Amazon DynamoDB](5.6.1-dynamodb/)
2. [Lambda Admin API](5.6.2-lambda-admin-api/)
3. [Admin Panel Frontend](5.6.3-admin-panel-frontend/)
