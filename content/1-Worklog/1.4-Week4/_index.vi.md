---
title: "Worklog Tuần 4"
date: 2026-05-11
weight: 4
chapter: false
pre: "  1.4.  "
---

### Mục tiêu tuần 4:

- Xây dựng lõi Compute Layer với AWS Lambda và Express.js (serverless-http).
- Hoàn thiện cái nhìn tổng thể về kiến trúc Serverless của LingoRise, từ frontend đến các dịch vụ bên ngoài AWS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Khởi tạo Express app và bọc bằng serverless-http wrapper.<br>Tích hợp middleware xác thực JWT lấy từ Amazon Cognito vào các Express routes. | 11/05/2026 | 11/05/2026 | [Tài liệu serverless-http](https://www.npmjs.com/package/serverless-http) |
| 3 - 5 | Nghiên cứu AWS SAM (Serverless Application Model) và CloudFormation.<br>Viết file cấu hình <code>template.yaml</code>, định nghĩa các Lambda resources và xử lý các lỗi tạo stack CloudFormation. | 12/05/2026 | 14/05/2026 | [Tài liệu AWS SAM](https://docs.aws.amazon.com/serverless-application-model/) & [Tài liệu CloudFormation](https://docs.aws.amazon.com/cloudformation/) |
| 6 | Cấu hình các biến môi trường SSM Parameter Store (SecureString) cho các hàm Lambda.<br>Triển khai thử nghiệm backend lên AWS Lambda qua AWS SAM CLI và kiểm tra log. | 15/05/2026 | 15/05/2026 | [Tài liệu AWS SAM CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html) |

### Kiến trúc LingoRise đã khảo sát trong tuần

- **Presentation Layer**: Người dùng truy cập domain qua Route 53, CloudFront phân phối asset, và AWS Amplify Hosting phục vụ frontend Next.js.
- **API Layer**: Frontend gọi API Gateway theo mô hình REST proxy để chuyển tiếp request đến Lambda.
- **Compute Layer**: AWS Lambda chạy Express.js thông qua `serverless-http`, xử lý logic đăng ký và xác thực.
- **Identity Layer**: Lambda xác thực JWT từ Amazon Cognito trước khi cho phép thực hiện các thao tác admin/user.
- **Data Layer**: Lambda ghi/đọc S3 để lưu assets, file phát sinh, và dùng RDS PostgreSQL cho dữ liệu nghiệp vụ chính.
- **Monitoring Layer**: CloudWatch được dùng để ghi log và theo dõi hoạt động của hệ thống.
- **External Services**: RDS PostgreSQL, S3, VNPay Gateway và LLM Provider được kết nối như các dịch vụ ngoài AWS để hoàn thiện luồng xử lý.

### Kết quả đạt được tuần 4:

- Triển khai (deploy) các Lambda function cốt lõi lên môi trường AWS thông qua công cụ AWS SAM.
- Nghiên cứu cấu trúc file `template.yaml`, giải quyết triệt để các lỗi phân quyền và triển khai liên quan đến CloudFormation.
- Xây dựng API chạy Express có khả năng phân tích request và tích hợp xác thực danh tính người dùng qua Cognito trên AWS.
- Làm chủ luồng xử lý tổng thể (end-to-end) của request đi qua API Gateway, Lambda, Cognito, S3 cùng các dịch vụ tích hợp (RDS PostgreSQL, cổng thanh toán VNPay, LLM Provider).
