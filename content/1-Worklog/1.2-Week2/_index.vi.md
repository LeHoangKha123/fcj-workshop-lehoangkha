---
title: "Worklog Tuần 2"
date: 2026-04-27
weight: 2
chapter: false
pre: "  1.2.  "
---

### Mục tiêu tuần 2:

- Khởi tạo các tài nguyên nền tảng bảo mật (Identity Layer) và lưu trữ (Data Layer).
- Cấu hình phân quyền IAM Role tuân thủ nguyên tắc quyền tối thiểu (Principle of Least Privilege).

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 - 4 | Nghiên cứu tài liệu và khởi tạo Amazon Cognito User Pool cho Learner và Admin.<br>Cấu hình App Client, thiết lập JWT tokens và phân quyền nhóm (User Group). | 27/04/2026 | 29/04/2026 | [Tài liệu AWS Cognito](https://docs.aws.amazon.com/cognito/) |
| 5 | Tạo các bucket Amazon S3 để lưu trữ assets và tài liệu dạng nháp.<br>Thiết lập CORS và block public access cho các S3 Buckets. | 30/04/2026 | 30/04/2026 | [Tài liệu AWS S3](https://docs.aws.amazon.com/s3/) |
| 6 | Viết policy và khởi tạo IAM Role riêng (Scoped Role) dành cho AWS Lambda.<br>Gắn quyền truy cập S3, Cognito Admin operations vào IAM Role. | 01/05/2026 | 01/05/2026 | [Tài liệu AWS IAM](https://docs.aws.amazon.com/iam/) |

### Kết quả đạt được tuần 2:

- Triển khai thành công Cognito User Pool để quản lý người dùng và cấp phát JWT, hoàn tất nghiên cứu chuyên sâu về cấu hình tiêu chuẩn bảo mật.
- Khởi tạo và bảo mật các S3 bucket theo đúng tiêu chuẩn vận hành để lưu trữ tài nguyên câu hỏi.
- Thiết lập Lambda Execution Role tuân thủ nguyên tắc đặc quyền tối thiểu (Least Privilege), đảm bảo an toàn và bảo mật thông tin.
