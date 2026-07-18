---
title: "Worklog Tuần 5"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

- Hoàn thiện Presentation Layer cho LingoRise: domain, CDN, và triển khai frontend.
- Kết nối giao diện người dùng với API, Cognito, và luồng xác thực end-to-end.
- Xác nhận cách các dịch vụ AWS phối hợp với dữ liệu ngoài AWS để đi gần hơn tới sản phẩm hoàn chỉnh.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Rà soát domain `lingorise.xyz`, cấu hình Route 53 và kiểm tra luồng phân giải DNS đến AWS edge. | 18/05/2026 | 18/05/2026 | [Tài liệu AWS Route 53](https://docs.aws.amazon.com/route53/) & [Tài liệu AWS CloudFront](https://docs.aws.amazon.com/cloudfront/) |
| 3 | Kiểm tra CloudFront và Amplify Hosting để đảm bảo frontend Next.js được phân phối ổn định. | 19/05/2026 | 19/05/2026 | [Tài liệu AWS Amplify](https://docs.aws.amazon.com/amplify/) & [Tài liệu AWS CloudFront](https://docs.aws.amazon.com/cloudfront/) |
| 4 | Tích hợp màn hình đăng nhập/đăng ký với Amazon Cognito và xác thực JWT phía client. | 20/05/2026 | 20/05/2026 | [Tài liệu Amazon Cognito](https://docs.aws.amazon.com/cognito/) |
| 5 | Nối frontend with API Gateway và Lambda, kiểm tra các request protected theo từng vai trò Learner/Admin. | 21/05/2026 | 21/05/2026 | [Tài liệu API Gateway](https://docs.aws.amazon.com/apigateway/) & [Tài liệu AWS Lambda](https://docs.aws.amazon.com/lambda/) |
| 6 | Đồng bộ dữ liệu hiển thị từ S3 và RDS PostgreSQL và hoàn thiện luồng request end-to-end của website. | 22/05/2026 | 22/05/2026 | [Sơ đồ Kiến trúc LingoRise](/vi/2-proposal/) |

### Kết quả đạt được tuần 5:

- Cấu hình và xác thực hoạt động ổn định của tên miền (domain) cùng lớp phân phối frontend qua Route 53, CloudFront và AWS Amplify.
- Tích hợp giao diện website với luồng xác thực Cognito và thiết lập kết nối gọi API từ hệ thống backend.
- Đồng bộ hóa sự phối hợp giữa Frontend, API Gateway, Lambda, S3 và các dịch vụ ngoài AWS để hình thành kiến trúc ứng dụng web LingoRise hoàn chỉnh.


