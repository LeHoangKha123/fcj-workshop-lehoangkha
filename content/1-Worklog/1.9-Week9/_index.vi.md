---
title: "Worklog Tuần 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

- Hoàn thiện kiểm thử chức năng thi thử (IELTS/TOEIC) và tích hợp hệ thống hàng đợi quét chữ OCR.
- Kiểm tra các luồng dữ liệu quan trọng và thiết lập cơ chế giám sát.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Kiểm thử luồng thi thử IELTS/TOEIC và tính năng lưu câu hỏi sai (Mistake Patterns) của học viên. | 15/06/2026 | 15/06/2026 | [Ghi chú Kiểm thử Nội bộ](/vi/1-worklog/) |
| 3 - 5 | Nghiên cứu Tesseract.js OCR, xây dựng hàng đợi xử lý background queue (quét chữ từ ảnh đề thi) dùng câu lệnh <code>SELECT FOR UPDATE SKIP LOCKED</code> tránh xung đột.<br>Thiết lập scheduled worker và cơ chế dọn dẹp các bản nháp import quá hạn. | 16/06/2026 | 18/06/2026 | [Tài liệu Tesseract.js (GitHub)](https://github.com/naptha/tesseract.js) & [Tài liệu thư viện OCR](https://tesseract.projectnaptha.com/) |
| 6 | Kiểm tra cơ chế ghi audit logs cho toàn bộ thao tác ghi của Admin và chạy thử nghiệm chịu tải song song. | 19/06/2026 | 19/06/2026 | [Ghi chú Đảm bảo Chất lượng (QA)](/vi/1-worklog/) |

### Kết quả đạt được tuần 9:

- Thiết lập thành công hệ thống hàng đợi quét ký tự quang học (OCR) tự động từ hình ảnh câu hỏi, rút ngắn thời gian nhập liệu đề thi.
- Ứng dụng thành công cơ chế chống xung đột hàng đợi trong PostgreSQL bằng kỹ thuật khóa `SKIP LOCKED` cho môi trường xử lý đa tiến trình.
- Đồng bộ hóa dữ liệu thi thử và hệ thống nhận diện mẫu lỗi sai (Mistake Patterns), hiển thị chính xác biểu đồ thống kê phân tích lỗi.
- Triển khai đầy đủ tính năng ghi nhật ký kiểm toán (audit logs) cho mọi hoạt động ghi/cập nhật của quản trị viên.
