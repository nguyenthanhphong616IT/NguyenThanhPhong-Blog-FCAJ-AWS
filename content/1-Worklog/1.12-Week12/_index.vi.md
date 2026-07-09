---
title: "Worklog Tuần 12"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

# Tuần 12: Rà soát hạ tầng, đánh giá chi phí và nghiệm thu
**Dự án:** Hệ thống đánh giá CV bằng AI smart
**Thời gian triển khai:** 06/07/2026 – 12/07/2026

### Phân công công việc: Phong (AWS Infrastructure)

#### 1. Công việc đã làm
- **Kiểm tra tổng thể:** Thực hiện kiểm tra tổng thể hạ tầng AWS trước khi bàn giao sản phẩm.
- **Bảo mật & Quyền truy cập:**
  - Rà soát toàn bộ IAM Policies của các Lambda Function theo nguyên tắc Least Privilege, loại bỏ các quyền truy cập không cần thiết.
  - Kiểm tra cấu hình Amazon S3 Block Public Access, CloudFront Origin Access Control và các chính sách Bucket Policy nhằm đảm bảo dữ liệu không bị truy cập trái phép.
- **Đánh giá chi phí:** Đánh giá và phân tích chi phí triển khai theo kiến trúc Serverless Pay-per-request, so sánh với mô hình máy chủ truyền thống để chứng minh hiệu quả về chi phí.
- **Tài liệu & Báo cáo nghiệm thu:**
  - Hoàn thiện tài liệu thiết kế hạ tầng AWS bằng AWS CDK, bổ sung sơ đồ triển khai và tài liệu mô tả kiến trúc Infrastructure as Code.
  - Viết báo cáo phần AWS Infrastructure, giải thích chi tiết cách triển khai hạ tầng bằng AWS CDK, kiến trúc Serverless và mô hình DynamoDB Single-Table Design, phục vụ cho quá trình nghiệm thu và bảo vệ đồ án.

#### 2. Khó khăn / Tồn đọng
- Cần rà soát kỹ toàn bộ quyền IAM và chính sách bảo mật trước khi triển khai Production nhằm tránh phát sinh lỗ hổng bảo mật.
- Việc tổng hợp tài liệu kỹ thuật và mô tả kiến trúc yêu cầu đối chiếu nhiều thành phần trong hệ thống để đảm bảo tính chính xác và đầy đủ.
