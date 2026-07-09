---
title: "Worklog Tuần 10"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

# Tuần 10: Triển khai hạ tầng IaC và tích hợp dịch vụ
**Dự án:** Hệ thống đánh giá CV bằng AI smart
**Thời gian triển khai:** 22/06/2026 – 28/06/2026

### Phân công công việc: Phong (AWS Infrastructure)

#### 1. Công việc đã làm
- **AWS CDK & IaC:** Chuyển toàn bộ bản thiết kế hạ tầng sang mã nguồn AWS CDK, triển khai Infrastructure as Code để tạo tài nguyên AWS tự động.
- **Amazon DynamoDB:** Triển khai bảng `SmartCVTable`, cấu hình Point-in-Time Recovery (PITR) nhằm hỗ trợ khôi phục dữ liệu khi xảy ra sự cố. Cấu hình Time To Live (TTL) để tự động xóa các dữ liệu tạm thời và tối ưu dung lượng lưu trữ.
- **Xác thực (Amazon Cognito):** Triển khai Amazon Cognito User Pool, cấu hình xác thực người dùng bằng Email và tích hợp đăng nhập thông qua Google OAuth. Thiết lập AWS Secrets Manager để lưu trữ thông tin Client ID và Client Secret phục vụ Google OAuth, đảm bảo an toàn thông tin.
- **Amazon API Gateway:** Xây dựng Amazon API Gateway và cấu hình Cognito Authorizer để bảo vệ các API bằng JWT Token.
- **Lưu trữ & Phân phối nội dung:** Triển khai hai bucket `FrontendBucket` và `ResumeBucket` trên Amazon S3 phục vụ lưu trữ giao diện và hồ sơ ứng viên. Thiết lập CloudFront Distribution kết hợp Origin Access Control (OAC) để giới hạn truy cập trực tiếp vào S3, tăng cường bảo mật cho hệ thống.

#### 2. Khó khăn / Tồn đọng
- Quá trình tích hợp Google OAuth với Amazon Cognito gặp lỗi do cấu hình Callback URL chưa chính xác, phải kiểm tra và điều chỉnh nhiều lần mới hoàn thành luồng đăng nhập trên môi trường Local.
- Mất nhiều thời gian để kiểm tra IAM Role và quyền truy cập giữa các dịch vụ AWS nhằm đảm bảo triển khai thành công.
