---
title: "Worklog Tuần 7"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

- Tích hợp tính năng tạo âm thanh giọng đọc (TTS) cho các bài nghe.
- Tối ưu hóa hiệu năng kết nối cơ sở dữ liệu và phân quyền hệ thống.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Rà soát IAM Role của Lambda, tinh chỉnh quyền truy cập S3, Cognito và tích hợp Edge-TTS theo nguyên tắc Least Privilege. | 01/06/2026 | 01/06/2026 | [Tài liệu AWS IAM](https://docs.aws.amazon.com/iam/) |
| 3 - 5 | Nghiên cứu và xây dựng cầu nối Edge-TTS bằng Python bridge trên môi trường AWS Lambda.<br>Giải quyết các vấn đề về dung lượng gói Lambda, quyền truy cập file nháp trên ổ đĩa read-only và tối ưu hóa thời gian xử lý. | 02/06/2026 | 04/06/2026 | [Thư viện Edge-TTS (GitHub)](https://github.com/rany2/edge-tts) & [Lập trình Python trên AWS Lambda](https://docs.aws.amazon.com/lambda/latest/dg/lambda-python.html) |
| 6 | Tối ưu hóa các truy vấn SQL nâng cao trên RDS PostgreSQL và cấu hình pool kết nối tối ưu tránh cạn kiệt tài nguyên Lambda. | 05/06/2026 | 05/06/2026 | [Tài liệu Amazon RDS cho PostgreSQL](https://docs.aws.amazon.com/rds/) |

### Kết quả đạt được tuần 7:
- Tích hợp thành công giải pháp chuyển đổi văn bản thành giọng nói tự nhiên (Edge-TTS), tự động hóa quy trình soạn thảo đề thi nghe (Listening) cho Admin.
- Tối ưu hóa và giải quyết thành công việc thực thi các script Python trung gian trên Lambda, xử lý tốt giới hạn dung lượng phân vùng `/tmp` và kích thước file zip.
- Cấu hình cơ chế kết nối (connection pool) tối ưu để đảm bảo các truy vấn RDS PostgreSQL hoạt động ổn định, loại bỏ lỗi quá tải kết nối (max connections).
