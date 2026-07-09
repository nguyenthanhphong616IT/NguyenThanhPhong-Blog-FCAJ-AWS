---
title: "Worklog Tuần 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

# Tuần 11: Tích hợp Frontend, Backend và tối ưu hệ thống
**Dự án:** Hệ thống đánh giá CV bằng AI smart
**Thời gian triển khai:** 29/06/2026 – 05/07/2026

### Phân công công việc: Phong (AWS Infrastructure)

#### 1. Công việc đã làm
- **Tích hợp API Gateway & Lambda:** Phối hợp với nhóm Backend kết nối toàn bộ AWS Lambda Functions với các phương thức trên Amazon API Gateway. Kiểm thử luồng xử lý dữ liệu từ `Frontend` → `API Gateway` → `Lambda` → `DynamoDB` nhằm đảm bảo toàn bộ hệ thống hoạt động xuyên suốt.
- **Lập lịch tự động (EventBridge):** Xây dựng AWS CDK để triển khai Amazon EventBridge Rules, phục vụ lập lịch tự động cho các tác vụ định kỳ theo múi giờ UTC.
- **Tối ưu CORS Policy:** Cấu hình và tối ưu CORS Policy trên Amazon S3 và API Gateway, chỉ cho phép các domain hợp lệ truy cập tài nguyên hệ thống.
- **Triển khai CI/CD Frontend:** Hoàn thiện quy trình triển khai Frontend tự động thông qua CI/CD, bao gồm:
  - Build mã nguồn Frontend.
  - Upload lên Amazon S3.
  - Thực hiện CloudFront Cache Invalidation để cập nhật phiên bản mới ngay sau khi triển khai.
- **Biến môi trường:** Kiểm tra và tối ưu các biến môi trường phục vụ quá trình Deploy trên nhiều môi trường khác nhau.

#### 2. Khó khăn / Tồn đọng
- Gặp lỗi CORS khi cấu hình bằng AWS CDK do thiết lập chưa đồng nhất giữa API Gateway và S3.
- Phải triển khai lại nhiều lần để kiểm tra cấu hình Mock Integration, Header và phương thức OPTIONS trước khi toàn bộ API hoạt động ổn định.
