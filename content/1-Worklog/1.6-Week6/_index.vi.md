---
title: "Worklog Tuần 6"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

- Hoàn thiện luồng tích hợp end-to-end giữa frontend, API, Lambda và các dịch vụ dữ liệu.
- Kiểm tra độ ổn định của hệ thống LingoRise trước khi bước sang giai đoạn hoàn thiện sản phẩm cuối cùng.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Rà soát lại toàn bộ luồng request từ Route 53, CloudFront, Amplify đến API Gateway và Lambda. | 25/05/2026 | 25/05/2026 | [Sơ đồ Kiến trúc LingoRise](/vi/2-proposal/) |
| 3 | Kiểm thử xác thực Cognito, phân quyền IAM Role và luồng truy cập theo từng vai trò Learner/Admin. | 26/05/2026 | 26/05/2026 | [Tài liệu Amazon Cognito](https://docs.aws.amazon.com/cognito/) & [Tài liệu AWS IAM](https://docs.aws.amazon.com/iam/) |
| 4 | Kiểm thử tương tác giữa Lambda với S3, và Amazon RDS for PostgreSQL 16. | 27/05/2026 | 27/05/2026 | [Tài liệu AWS S3](https://docs.aws.amazon.com/s3/) & [Tài liệu Amazon RDS](https://docs.aws.amazon.com/rds/) |
| 5 | Bổ sung xử lý lỗi, log CloudWatch và các kiểm tra cuối cho API và frontend. | 28/05/2026 | 28/05/2026 | [Tài liệu AWS CloudWatch](https://docs.aws.amazon.com/cloudwatch/) |
| 6 | Tổng hợp kết quả tích hợp, tinh chỉnh giao diện và chuẩn bị bước hoàn thiện sản phẩm LingoRise song ngữ ưu tiên tiếng Việt. | 29/05/2026 | 29/05/2026 | [Ghi chú nội bộ dự án](/vi/1-worklog/) |

### Kết quả đạt được tuần 6:

- Rà soát và kiểm thử tích hợp (integration testing) luồng xử lý end-to-end của toàn hệ thống.
- Xác thực khả năng vận hành liền mạch của Lambda với Cognito, S3 và Amazon RDS for PostgreSQL 16 trong cùng một luồng nghiệp vụ.
- Bổ sung cơ chế ghi log và kiểm tra điều kiện biên để chuẩn bị cho các bước hoàn thiện hệ thống.
- Định hình rõ nét kiến trúc và lộ trình hoàn thiện sản phẩm LingoRise phiên bản song ngữ (ưu tiên tiếng Việt) làm sản phẩm bàn giao cuối kỳ.


