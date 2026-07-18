---
title: "Worklog Tuần 3"
date: 2026-05-04
weight: 3
chapter: false
pre: "  1.3.  "
---

### Mục tiêu tuần 3:

- Thiết lập và kết nối với các dịch vụ bên ngoài AWS (External Services).
- Đảm bảo Lambda có thể tương tác với cơ sở dữ liệu và cache.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Khởi tạo project Amazon RDS for PostgreSQL 16 làm primary datastore.<br>Cấu hình pg pool cho kết nối. | 04/05/2026 | 04/05/2026 | [Tài liệu Amazon RDS cho PostgreSQL](https://docs.aws.amazon.com/rds/) |
| 3 | Thiết kế các table cơ bản cho LingoRise (Users, Courses, MockTests). | 05/05/2026 | 05/05/2026 | [Kiến trúc dữ liệu LingoRise](/vi/2-proposal/) |
| 4 | Tích hợp AWS SDK và thiết lập cấu hình môi trường local / dotenv cho Node.js backend. | 06/05/2026 | 06/05/2026 | [Tài liệu AWS SDK](https://docs.aws.amazon.com/sdk-for-javascript/) & [Thư viện dotenv](https://www.npmjs.com/package/dotenv) |
| 5 | Cài đặt thư viện kết nối Database (pg, pg-pool) vào project Node.js 20 local. | 07/05/2026 | 07/05/2026 | [Tài liệu thư viện npm](https://docs.npmjs.com/) |
| 6 | Viết script và test kết nối thành công từ local tới RDS PostgreSQL. | 08/05/2026 | 08/05/2026 | [Tài liệu phát triển Node.js](https://nodejs.org/docs/) |

### Kết quả đạt được tuần 3:

- Hoàn thiện thiết lập môi trường Data Layer bên ngoài AWS.
- Phát triển và chạy thử nghiệm mã nguồn local, thực hiện truy vấn SQL thành công đến cơ sở dữ liệu RDS PostgreSQL.


