---
title: "Worklog Tuần 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

# Tuần 9: Khởi tạo hạ tầng AWS và thiết kế cơ sở dữ liệu
**Bắt đầu làm Dự án:** Hệ thống đánh giá CV bằng AI smart
**Thời gian triển khai:** 15/06/2026 – 21/06/2026

### Phân công công việc: Phong (AWS Infrastructure)

Trong tuần 9, với vai trò chịu trách nhiệm về hạ tầng AWS cho hệ thống đánh giá CV bằng AI, mình đã tập trung vào việc thiết kế kiến trúc tổng thể, tổ chức dự án IaC và tối ưu hóa cơ sở dữ liệu. Dưới đây là chi tiết các công việc đã thực hiện:

#### 1. Thiết kế kiến trúc hạ tầng
- **Vẽ sơ đồ hạ tầng mạng AWS (Topology):** Nghiên cứu yêu cầu của hệ thống đánh giá CV và thiết kế sơ đồ kiến trúc hạ tầng theo định hướng Serverless.
- **Mô tả luồng xử lý dữ liệu:** Xây dựng luồng dữ liệu tích hợp giữa các dịch vụ AWS cốt lõi bao gồm CloudFront, S3, API Gateway, Lambda, Cognito, DynamoDB và Amazon Bedrock (dành cho phần AI phân tích CV).

#### 2. Thiết kế cơ sở dữ liệu DynamoDB
- **Áp dụng Single-Table Design:** Thiết kế cơ sở dữ liệu Amazon DynamoDB theo mô hình Single-Table Design, phân tích chi tiết các nghiệp vụ và pattern truy vấn của hệ thống.
- **Bảng SmartCVTable:** Thống nhất với nhóm Backend việc lưu trữ các thực thể chính (`Applications`, `Notes`, `Settings`, `StatusEvents`) vào chung một bảng `SmartCVTable`.
- **Hệ thống khóa tối ưu:** Thiết lập hệ thống khóa sử dụng `PK`, `SK`, `GSI1PK`, `GSI1SK` nhằm gộp các entities, tối ưu hóa hiệu năng truy vấn và giảm tối đa chi phí vận hành.
- **Tài liệu hóa dữ liệu:** Xây dựng tài liệu mô tả cấu trúc dữ liệu, quy ước đặt khóa (key conventions) và các mẫu truy vấn (query patterns) để hỗ trợ nhóm phát triển API trong các giai đoạn sau.

#### 3. Khởi tạo hạ tầng dưới dạng mã (IaC)
- **Sử dụng AWS CDK (TypeScript):** Khởi tạo thư mục dự án hạ tầng bằng AWS Cloud Development Kit (CDK) sử dụng ngôn ngữ TypeScript.
- **Tổ chức cấu trúc:** Xây dựng cấu trúc Infrastructure as Code chuẩn, tổ chức các thư mục rõ ràng và chuẩn bị sẵn sàng các Stack để triển khai tài nguyên AWS tự động cho các Sprint tiếp theo.