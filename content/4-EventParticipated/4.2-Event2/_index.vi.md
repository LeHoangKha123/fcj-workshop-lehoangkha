---
title: "Event 2"
date: 2026-06-13
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Bài thu hoạch “AWS First Cloud AI Journey — Hội thảo chia sẻ nghề nghiệp & văn hóa tại MNCs”

### Mục Đích Của Sự Kiện

- Hướng tới việc thu hẹp khoảng cách giữa lý thuyết học tập và môi trường doanh nghiệp thực tế.
- Cung cấp định hướng nghề nghiệp thông qua chia sẻ trải nghiệm thực chiến về lộ trình, văn hóa làm việc tại các công ty đa quốc gia (MNCs) và startup tăng trưởng nhanh.
- Xác định bộ kỹ năng cốt lõi và tư duy phát triển sự nghiệp trong ngành dữ liệu và đám mây.

### Danh Sách Diễn Giả

- **Mr. Dat Pham** - Data Analytics Engineer
- **Mr. Cuong Nguyen** - Process Engineer
- **Trong H. Truong** - DevOps Engineer @ Endava Vietnam
- **Danh Hoang Hieu Nghi** - AI Engineer, AWS Community Builder, AWS Student Builder Group Leader
- **Đinh Trung Kiên** - Lead Developer at a startup
- **Nguyễn Minh Thọ** - Student

### Nội Dung Nổi Bật

#### Thực tế công việc và bộ kỹ năng tại doanh nghiệp
- Vai trò của kỹ sư dữ liệu thay đổi linh hoạt theo ngành nghề (domain): từ thiết kế dashboard báo cáo hiệu suất tại các startup như Kamereo đến tối ưu hóa chi phí và thiết bị IoT tại tập đoàn sản xuất như Colgate-Palmolive.
- 4 kỹ năng sống còn: Tư duy phản biện, kỹ năng giao tiếp, khả năng kể chuyện với dữ liệu (Data Storytelling), và giải quyết vấn đề dựa trên dữ liệu.
- Lộ trình thăng tiến được chia thành 3 mốc: Follower (Người thực thi) $\rightarrow$ Learner (Người học chủ động) $\rightarrow$ Problem Solver (Người giải quyết vấn đề).

#### Bức tranh toàn cảnh về DevOps
- Phá vỡ góc nhìn lối mòn: DevOps không chỉ dừng ở cài đặt công cụ hay sửa lỗi ban đêm, mà là chiến lược cốt lõi để tăng tốc phân phối phần mềm và độ tin cậy.
- Phạm vi công việc thực tế được định hình bởi quy mô dự án, cấu trúc nhóm và mức độ tự động hóa hạ tầng đám mây.
- Bản đồ hóa 10 giai đoạn hệ sinh thái công cụ: từ Plan & Code (Git, Jira), Build & Test (Jenkins), Release & Deploy (Terraform), đến Operate (Kubernetes, AWS) và Security/Platform Engineering (SonarQube).

#### Lộ trình phát triển hệ sinh thái AWS
- Vòng lặp 8 bước trưởng thành: Bắt đầu từ sự tò mò (Student Curiosity) đến tham gia lab thực hành, xây dựng portfolio dự án thực tế, và cuối cùng là trở thành AWS Partner để chia sẻ lại kiến thức cho cộng đồng (Share Back).
- Đặc quyền cộng đồng AWS Student Builder: Cung cấp môi trường thực chiến thông qua các tín chỉ AWS Credits và voucher thi chứng chỉ quốc tế, giúp giảm rào cản chi phí.

#### Kiến trúc hệ thống URL Shortening trên AWS
- **Cơ sở hạ tầng**: Tận dụng Route 53, CloudFront và WAF để điều hướng và bảo mật; Amplify cho frontend tĩnh; và Fargate (ECS) chạy Spring Boot API phía sau Application Load Balancer.
- **Chiến lược xử lý dữ liệu**: Sử dụng DynamoDB làm kho lưu trữ chính, kết hợp Amazon ElastiCache cho Redis để tối ưu hóa tốc độ đọc truy xuất.
- **Mô hình Key Generation Service (KGS)**: Chạy tiến trình ngầm để sinh trước mã khóa độc bản, đẩy vào hàng đợi Redis (LPUSH) và trích xuất (RPOP) ngay khi có yêu cầu. Phương pháp này giúp tránh nghẽn ghi (write bottleneck) khi hệ thống chịu tải cao.

### Những Gì Học Được

#### Tư Duy Thiết Kế
- **Thiết kế hướng Domain**: Công nghệ và mã nguồn chỉ thực sự phát huy giá trị khi được gắn chặt với bối cảnh và mục tiêu cụ thể của doanh nghiệp.
- **Tư duy Problem Solver**: Nhận thức rõ sự cần thiết phải chuyển dịch từ việc thực thi nhiệm vụ theo kịch bản có sẵn sang việc chủ động phân tích bài toán kinh doanh, tìm nguyên nhân gốc rễ và đề xuất giải pháp.
- **Data Storytelling**: Việc xây dựng hạ tầng kỹ thuật là chưa đủ; năng lực cốt lõi còn nằm ở khả năng biến dữ liệu thành thông điệp có ý nghĩa để giao tiếp với các bên liên quan.

#### Kiến Trúc Kỹ Thuật
- **Chiến lược tối ưu hóa tác vụ ghi**: Hiểu sâu sắc mô hình tính toán trước (KGS Pattern) để xử lý tình huống hệ thống chịu lượng request khổng lồ đồng thời.
- **Kiến trúc phân tán**: Cách thức kết hợp giữa một cơ sở dữ liệu NoSQL (DynamoDB) bền vững và một in-memory cache (Redis) để đạt hiệu suất cao nhất.
- **Hệ sinh thái IaC (Infrastructure as Code)**: Tầm quan trọng của việc đóng gói hạ tầng thành mã để đảm bảo tính nhất quán và tự động hóa trong vòng đời triển khai (CI/CD).

### Ứng Dụng Vào Công Việc
- **Kiến trúc hệ thống**: Áp dụng triết lý phân tách các tác vụ nặng thành các background task (như mô hình KGS) kết hợp in-memory queue để loại bỏ điểm nghẽn cổ chai.
- **Triển khai tự động**: Đưa các công cụ tự động hóa cấp phát tài nguyên (như AWS SAM hoặc Terraform) vào luồng vận hành để chuẩn hóa quy trình phát hành sản phẩm.
- **Tối ưu hóa cơ sở dữ liệu**: Đánh giá và triển khai các giải pháp Distributed Caching cho các luồng xử lý có tỷ lệ đọc cao nhằm giảm tải cho Database chính.
- **Quản trị chất lượng**: Xây dựng văn hóa ghi chép tài liệu dự án minh bạch (portfolio) để theo dõi tiến độ kỹ thuật và làm cơ sở đo lường hiệu suất.

### Trải nghiệm trong event

Tham gia "Hội thảo chia sẻ nghề nghiệp & văn hóa tại MNCs" mang lại góc nhìn chuyên nghiệp, thực tế về khoảng cách giữa môi trường học thuật và các tiêu chuẩn vận hành khắt khe tại doanh nghiệp đa quốc gia. Một số trải nghiệm nổi bật:

#### Lĩnh hội tư duy thiết kế hệ thống cấp doanh nghiệp
- Qua case study phân tích hệ thống URL Shortening, hiểu rõ cách các dịch vụ như AWS Fargate, DynamoDB, và Redis tương tác chặt chẽ để tạo nên một kiến trúc chịu lỗi và khả năng mở rộng không giới hạn.
- Ấn tượng mạnh mẽ với kỹ thuật giải quyết bài toán "write bottleneck" bằng cách sinh mã khóa trước thông qua KGS Pattern. Đây là minh chứng rõ nét cho tư duy kỹ thuật đi trước một bước nhằm bảo vệ hệ thống khỏi rủi ro sập nguồn.

#### Định vị bản thân trên bản đồ công nghệ
- Hội thảo giúp hệ thống hóa lại toàn bộ chu trình DevOps thành 10 giai đoạn rõ ràng, từ đó xác định chính xác năng lực hiện tại và các mảng công cụ cần bổ sung để đáp ứng tiêu chuẩn ngành.
- Nhận thức sâu sắc về việc thay đổi tư duy làm việc: không chỉ dừng lại ở vị trí "Người học" (Learner) mà phải nỗ lực tiến tới vai trò "Người giải quyết vấn đề" (Problem Solver), chịu trách nhiệm về chất lượng đầu ra cuối cùng.

#### Bài học rút ra
- Cốt lõi của việc phát triển phần mềm không nằm ở số lượng công nghệ được sử dụng, mà nằm ở việc giải pháp đó tối ưu hóa chi phí và hiệu suất cho doanh nghiệp ra sao.
- Việc tích lũy chứng chỉ thông qua các chương trình như AWS Student Builder là bàn đạp vững chắc, nhưng khả năng trình bày kiến trúc dự án rõ ràng (Portfolio) và kể chuyện kỹ thuật (Data Storytelling) mới là chìa khóa tạo lợi thế cạnh tranh cốt lõi.
- Việc tự động hóa luồng triển khai (CI/CD) không còn là lựa chọn thêm vào, mà là yêu cầu bắt buộc để duy trì tốc độ phát hành nhanh chóng và an toàn trong môi trường hiện đại.

#### Một số hình ảnh khi tham gia sự kiện
![Ảnh chụp tại sự kiện ](images/1.jpg)

> Tổng thể, hội thảo không chỉ mang lại góc nhìn chân thực về lộ trình phát triển và hệ sinh thái DevOps, mà còn định hình lại tư duy nghề nghiệp của tôi: chuyển dịch mạnh mẽ từ một người thực thi thụ động (Follower) sang tâm thế của một kỹ sư chủ động giải quyết vấn đề (Problem Solver), sẵn sàng thiết kế những kiến trúc chịu tải cao đáp ứng tiêu chuẩn khắt khe của doanh nghiệp.