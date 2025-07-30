---
title : "Các dịch vụ AWS cần chuẩn bị"
date :  "2025-07-28" 
weight : 2
chapter : false
pre : " <b> 2. </b> "
---

Toàn bộ kiến trúc này được triển khai trong một VPC (Virtual Private Cloud), tận dụng hai Availability Zones (Vùng khả dụng) để đảm bảo tính sẵn sàng cao.

Trong VPC này, tôi đã thiết lập hai private subnets (mạng con riêng), tạo một môi trường bảo mật cho các tài nguyên của chúng ta. Để phân phối lưu lượng truy cập một cách hiệu quả và an toàn, tôi sử dụng một Internal Application Load Balancer (Bộ cân bằng tải ứng dụng nội bộ). Đây là thành phần quan trọng giúp định tuyến các yêu cầu đến ứng dụng của chúng ta.

Điểm đặc biệt của kiến trúc này là việc sử dụng AWS Lambda làm môi trường tính toán chính. Thay vì máy chủ truyền thống, chúng ta sẽ lưu trữ toàn bộ trang web ứng dụng nhân sự đơn giản trong các hàm Lambda. Phương pháp này giúp giảm thiểu chi phí vận hành, loại bỏ gánh nặng quản lý máy chủ và tự động mở rộng theo nhu cầu.

Trong phần trình bày tiếp theo, tôi sẽ hướng dẫn chi tiết từng bước cách xây dựng kiến trúc này trực tiếp trên bảng điều khiển AWS, cho thấy quá trình triển khai đơn giản đến bất ngờ.


### Nội dung
  - [Tạo VPC](2.1-createvpc/)
  - [Tạo Lambda](2.2-createlambda/)
  - [Tạo Load balancing](2.1.3-createloadbalancing/)
  - [Tạo Domain](2.4-createdomain/)
  - [Tạo cognito user pools](2.5-createcognito/)
