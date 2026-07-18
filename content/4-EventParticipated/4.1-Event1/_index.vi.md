---
title: "Event 1"
date: 2026-05-23
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Bài thu hoạch “AWS First Cloud AI Journey — Community Day”

### Mục Đích Của Sự Kiện
- Phân tích các bài toán thực tiễn trong việc vận hành Generative AI trên hệ thống lớn.
- Chia sẻ chiến lược tối ưu hóa quy trình DevOps và Platform Engineering.
- Hướng dẫn thiết kế kiến trúc hệ thống chịu tải đột biến và quản trị rủi ro tài chính trên môi trường điện toán đám mây AWS.

### Danh Sách Diễn Giả
- **Tinh Truong** - Platform Engineer, GoTymeX
- **Pham Nguyen Hai Anh** - Cloud Consultant, G-AsiaPacific Vietnam & AWS Community Builder
- **Nguyen Tuan Thinh** - DevOps Engineer, First Cloud AI Journey
- **Team VIB** - Đại diện nhóm kỹ sư GenAI và phát triển phần mềm
- **Duc Dao** - Solution Architect, Cloud Kinetics
- **Vy Lam** - Senior Business Systems Analyst, VPBank

### Nội Dung Nổi Bật

#### Tầm quan trọng của Ngữ cảnh (Context Is Everything)
- **Thiếu ngữ cảnh là AI thất bại**: AI không cần dữ liệu rác, mà cần đầu vào được đóng khung chặt chẽ (Mục tiêu, Tình huống, Ràng buộc, Bằng chứng).
- **Tránh bẫy "Internet Puller"**: Nhồi nhét tài liệu dung lượng lớn chỉ làm tăng chi phí token và pha loãng thông tin quan trọng.
- **Second AI Brain**: Xây dựng hệ thống ghi nhớ giúp AI tự động trích xuất đúng mảnh thông tin cần thiết thay vì hỏi lại từ đầu.

#### Tự động hóa kiểm định hệ thống (GenAI-Powered Auto Audit)
- Sử dụng **Amazon Q Business** để kết nối hơn 40 cổng dữ liệu nội bộ.
- Tự động hóa các tác vụ lặp lại: nghe ghi âm, tạo biên bản cuộc họp (MoM) và điều phối lịch trình.
- Ứng dụng LLM chủ động rà quét hạ tầng AWS, đối chiếu tiêu chuẩn an toàn thông tin để phát hiện lỗ hổng.

#### Quản trị nền tảng phân phối và Rủi ro chi phí (CloudFront)
- Tận dụng sức mạnh phân phối tài nguyên từ mạng lưới Edge-to-Origin.
- **Nghịch lý Pay-As-You-Go**: Lưu lượng đột biến do bùng nổ người dùng (viral) hoặc bị tấn công DDoS có thể biến hóa đơn CDN thành thảm họa tài chính.
- Bắt buộc thiết lập **CloudWatch Billing Alerts** để cảnh báo chi phí và dùng **AWS WAF** tại lớp viền bảo vệ máy chủ gốc.

#### Chiến lược Hackathon 36 giờ (Xây dựng UTMorpho)
- Quy hoạch kiến trúc cốt lõi và schema API ngay từ đầu để frontend và backend có thể chạy độc lập, song song.
- Chấp nhận đánh đổi, quản lý nợ kỹ thuật có chủ đích để tung ra sản phẩm khả thi tối thiểu (MVP) đúng hạn.
- Tập trung vào tính năng cốt lõi thay vì tham lam ôm đồm quá nhiều chi tiết.

#### Bản chất khó đoán của LLM (Non-Determinism)
- Thiết lập **Temperature = 0** trên thực tế không đảm bảo kết quả cố định tuyệt đối.
- Nguyên nhân gốc rễ: Sai số dấu phẩy động cực nhỏ trong quá trình tính toán trên hàng ngàn lõi GPU xử lý song song và sự dao động của tải hệ thống API.
- Giải pháp: Viết system prompt khắt khe và phải dùng JSON schema validation để lọc kết quả ở backend.

#### Hệ thống Multi-Agent cấp doanh nghiệp
- Khắc phục lỗ hổng của Single-Agent (tràn ngữ cảnh, ảo giác, "single point of failure").
- Đề xuất mô hình "Hội đồng AI" gồm nhiều agent chuyên môn hóa sâu (như phân tích rủi ro, kiểm toán công nghệ, dòng tiền) phối hợp dưới một lớp điều phối trung tâm.
- Bảo vệ khối lượng công việc LLM qua kiến trúc an ninh 5 lớp (Perimeter, VPC, Identity, Application, Data).

### Những Gì Học Được

#### Tư Duy Thiết Kế
- **Tối giản hóa ngữ cảnh**: Cung cấp lượng dữ liệu tối thiểu và cấu hình vừa đủ để giải quyết đúng vấn đề thay vì ném một tập dữ liệu hỗn độn cho mô hình.
- **Chia để trị (Multi-Agent)**: Phân rã logic AI thành các chuyên gia độc lập, tương tự như nguyên lý Clean Architecture, giúp can thiệp khoanh vùng lỗi dễ dàng mà không ảnh hưởng hệ thống liền kề.

#### Kiến Trúc Kỹ Thuật
- Bản chất vật lý của tính toán trên GPU giải thích hiện tượng trôi dạt kết quả AI. Bài học rút ra là không bao giờ được phép đoán mò hay đặt niềm tin mù quáng vào kết quả sinh ra từ LLM.
- Quản trị hạ tầng Cloud không chỉ là làm cho "code chạy được", mà phải là thiết lập các giới hạn sinh tồn chủ động để hệ thống tự bảo vệ trước rủi ro tài chính.

#### Chiến Lược Hiện Đại Hóa & Bảo Mật
- **Phòng thủ ở tầng ứng dụng**: Validate nghiêm ngặt định dạng đầu ra và luôn xây dựng bộ parser xử lý ngoại lệ (fallback) cho phản hồi của AI.
- Bảo vệ hệ thống phân phối nội dung tĩnh ngay từ biên bằng CloudFront OAC.

### Ứng Dụng Vào Công Việc
- **Tối ưu kiến trúc AI**: Áp dụng tư duy phân tách Multi-Agent để xây dựng các luồng xử lý độc lập (ví dụ: một luồng tạo nội dung, một luồng tự động đánh giá).
- **Xử lý ngoại lệ**: Bổ sung bộ parser mạnh mẽ (sử dụng biểu thức chính quy như `extractJsonObject()`) để chủ động ứng phó với tình trạng định dạng JSON bị lệch từ API.
- **Bảo mật hạ tầng**: Thực hành cấu hình Origin Access Control (OAC) để bảo vệ tài nguyên lưu trữ và thiết lập báo động ngân sách chặt chẽ.
- **Viết code phòng thủ**: Đưa mọi nhiệm vụ thành tiêu chí kiểm chứng rõ ràng; luôn viết các test tái hiện trước khi đưa ứng dụng có tích hợp AI lên môi trường thực tế.

### Trải nghiệm trong event

Tham gia sự kiện **AWS First Cloud AI Journey — Community Day** là một trải nghiệm thực chiến cực kỳ giá trị, giúp tôi thấu hiểu sâu sắc sự khác biệt giữa việc gọi API cơ bản và việc vận hành một hệ thống AI có kiến trúc hoàn chỉnh. Một số trải nghiệm nổi bật:

#### Học hỏi từ các diễn giả có chuyên môn cao
- Các kỹ sư và chuyên gia từ VPBank, VIB, GoTymeX đã bóc tách những góc khuất kỹ thuật (technical blindspots) thường không được đề cập trên các tài liệu chính thức.
- Lĩnh hội được góc nhìn hệ thống của doanh nghiệp khi đánh giá rủi ro công nghệ và tối ưu hóa chi phí vận hành.

#### Trải nghiệm kỹ thuật thực tế
- Thấu hiểu bản chất toán học đằng sau sự khó đoán của LLM, từ đó thay đổi hoàn toàn tư duy, không còn phụ thuộc thụ động vào tham số `Temperature = 0`.
- Nắm bắt được cách thiết kế và luồng giao tiếp giữa các thành phần trong một kiến trúc Multi-Agent phân tán.

#### Ứng dụng công cụ hiện đại
- Khám phá tiềm năng to lớn của **Amazon Q Business** trong việc kết nối đa cổng dữ liệu và giải phóng sức người khỏi các tác vụ tổng hợp thông tin nhàm chán.
- Cập nhật các bộ công cụ phòng thủ hiện đại như AWS WAF tích hợp vào hệ sinh thái phân phối nội dung.

#### Kết nối và trao đổi
- Có cơ hội thảo luận trực tiếp với các kiến trúc sư đám mây và mentor kỳ cựu.
- Trao đổi sâu về các phương án thiết kế cơ sở dữ liệu và chiến lược phòng ngừa sốc hóa đơn (bill shock) cho các dự án độc lập.

#### Bài học rút ra
- Dữ liệu rác tạo ra kết quả rác. Việc cung cấp **Ngữ cảnh** chính xác biến một mong muốn mơ hồ thành một bài toán kỹ thuật có thể đo lường và giải quyết.
- Việc xây dựng cơ chế phòng thủ (từ validate đầu ra của model đến thiết lập giới hạn chi tiêu hạ tầng) là yếu tố sống còn trước khi đưa bất kỳ tính năng AI nào vào vận hành.

#### Một số hình ảnh khi tham gia sự kiện
![Ảnh chụp tại sự kiện ](/images/Event1/5.jpg)

![Ảnh chụp tại sự kiện ](/images/Event1/1.jpg)

![Ảnh chụp tại sự kiện ](/images/Event1/2.jpg)

![Ảnh chụp tại sự kiện ](/images/Event1/3.jpg)

![Ảnh chụp tại sự kiện ](/images/Event1/4.jpg)

> Tổng thể, sự kiện không chỉ cung cấp các mẫu kiến trúc tiên tiến mà còn định hình lại phương pháp luận lập trình của tôi: luôn thận trọng, đặt tính đơn giản lên hàng đầu, và chuyển hóa mọi rủi ro tiềm ẩn thành các bài test kiểm chứng rõ ràng trước khi viết code.