Proposal Connect to an internal web application using AWS Verified Access
1. Mục đích
Đề xuất này nhằm triển khai giải pháp AWS Verified Access để kết nối an toàn và hiệu quả tới ứng dụng web nội bộ của công ty mà không cần sử dụng VPN, đồng thời đảm bảo kiểm soát truy cập linh hoạt, nâng cao bảo mật và cải thiện trải nghiệm người dùng.

2. Lý do lựa chọn AWS Verified Access
✅ Loại bỏ nhu cầu sử dụng VPN truyền thống

✅ Xác thực theo thời gian thực dựa trên danh tính và trạng thái thiết bị

✅ Trải nghiệm người dùng mượt mà, truy cập ứng dụng từ xa dễ dàng

✅ Hỗ trợ chính sách truy cập theo ứng dụng và người dùng

✅ Ghi nhận nhật ký truy cập tập trung phục vụ cho giám sát và bảo mật

3. Tính năng nổi bật
Xác thực người dùng (User Authentication) thông qua Amazon Cognito

Đánh giá thiết bị (Device Posture Assessment) đảm bảo thiết bị đáng tin cậy

Tùy biến truy cập theo ứng dụng

Gộp nhóm ứng dụng nội bộ để quản lý hiệu quả

Theo dõi truy cập qua centralized logs

4. Các tình huống ứng dụng (Use Cases)
Bảo vệ người dùng làm việc từ xa hoặc phân tán (remote/distributed users)

Quản lý truy cập đến các ứng dụng nội bộ một cách linh hoạt

Dễ dàng mở rộng và tích hợp hệ thống hiện tại

Thu thập và phân tích nhật ký truy cập tập trung


5. Các bước triển khai
Tạo Amazon Cognito User Pool

Tạo người dùng Cognito

Tạo Trust Provider trong AWS Verified Access dựa trên Cognito

Tạo Instance của AWS Verified Access

Cấu hình Group và chính sách truy cập cơ bản

Tạo Endpoint truy cập ứng dụng

Cập nhật DNS trong Amazon Route 53

Kiểm thử truy cập vào ứng dụng

6. Lợi ích kỳ vọng
Tăng cường bảo mật ứng dụng nội bộ

Tiết kiệm chi phí vận hành VPN và hạ tầng mạng

Cải thiện khả năng mở rộng và quản trị người dùng

Đáp ứng các yêu cầu tuân thủ (compliance) về truy cập và bảo mật

7. Kết luận
Việc triển khai AWS Verified Access là một giải pháp hiện đại giúp doanh nghiệp đảm bảo an toàn cho các ứng dụng nội bộ mà không ảnh hưởng đến trải nghiệm người dùng.

Chúng tôi đề xuất tiến hành thử nghiệm và áp dụng giải pháp này trong thời gian tới nhằm nâng cao năng lực bảo mật tổng thể.
