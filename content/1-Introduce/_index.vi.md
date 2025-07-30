---
title : "Giới thiệu"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
**AWS Verified Access** là một dịch vụ của Amazon Web Services (AWS) được thiết kế để cung cấp quyền truy cập an toàn và liền mạch vào các ứng dụng và tài nguyên của công ty mà không cần sử dụng mạng riêng ảo (VPN) truyền thống. Dịch vụ này được xây dựng trên nguyên tắc Zero Trust, có nghĩa là không có người dùng hay thiết bị nào được tin cậy mặc định.

Điểm nổi bật:

Truy cập dựa trên Zero Trust: AWS Verified Access liên tục xác thực từng yêu cầu truy cập dựa trên các chính sách truy cập chi tiết, ngữ cảnh, đảm bảo rằng quyền truy cập chỉ được cấp và duy trì khi người dùng đáp ứng các yêu cầu bảo mật cụ thể.

Bảo mật nâng cao: Nó cho phép bạn định nghĩa các chính sách truy cập tinh vi dựa trên danh tính người dùng (tích hợp với AWS IAM Identity Center hoặc các nhà cung cấp định danh bên thứ ba như Okta, Azure AD, Google Workspace) và trạng thái bảo mật của thiết bị (tích hợp với các dịch vụ quản lý thiết bị của bên thứ ba).

Đơn giản hóa trải nghiệm người dùng: Người dùng có thể truy cập các ứng dụng trực tiếp qua trình duyệt hoặc ứng dụng mà không cần cài đặt và cấu hình VPN client, giúp trải nghiệm liền mạch hơn.

Đơn giản hóa hoạt động bảo mật: Quản trị viên có thể tạo, nhóm và quản lý các chính sách truy cập cho các ứng dụng và tài nguyên có yêu cầu bảo mật tương tự từ một giao diện duy nhất, giúp đơn giản hóa việc quản lý chính sách.

Khả năng mở rộng: AWS Verified Access được thiết kế để mở rộng cùng với môi trường AWS của bạn, dễ dàng quản lý và bảo mật quyền truy cập vào các ứng dụng khi tổ chức phát triển.

Khả năng quan sát: Cung cấp khả năng ghi nhật ký và hiển thị toàn diện về các nỗ lực truy cập, giúp nhanh chóng xác định và giải quyết các sự cố bảo mật và kết nối.

Hỗ trợ đa dạng giao thức: Ban đầu tập trung vào HTTP(S), hiện tại AWS Verified Access đã hỗ trợ kết nối qua các giao thức không phải HTTP(S), mở rộng khả năng ứng dụng.

