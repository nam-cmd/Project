---
title : "Verified Access instances"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.2. </b> "
---
### Verified Access instances

 1. Đăng nhập vào AWS Management Console

 2. Truy cập dịch vụ VPC:

    -Trong thanh tìm kiếm ở trên cùng, nhập "VPC" và chọn VPC từ kết quả.

    -Hoặc, trong bảng điều khiển dịch vụ, tìm đến mục Networking & Content Delivery và chọn VPC.

3.  Điều hướng đến Verified Access Instances:

    -Trong thanh điều hướng bên trái của bảng điều khiển VPC, cuộn xuống phần Verified Access.

    -Chọn Verified Access instances.

4.  Bắt đầu tạo Verified Access Instance mới:

    -Trên trang Verified Access instances, nhấp vào nút Create Verified Access instance.
    ![instances](/images/images/8/instances1.png?featherlight=false&width=90pc)

5.  Cấu hình Verified Access Instance:

    -Name tag (Tên thẻ):

    Nhập một tên dễ nhận biết cho Verified Access instance của bạn (ví dụ: MyInternalAppVAInstance). Tên này sẽ xuất hiện trong bảng điều khiển và các tài nguyên liên quan.

    -Description (Mô tả - Tùy chọn):

    Cung cấp mô tả ngắn gọn về mục đích của instance này.

    -Trust providers (Nhà cung cấp tin cậy):

    Đây là phần quan trọng nhất. Bạn cần chọn (hoặc thêm mới) các nhà cung cấp tin cậy mà bạn đã tạo trước đó.

    -Nhấp vào Add trust provider.

    Trong cửa sổ bật lên, chọn loại nhà cung cấp tin cậy (ví dụ: User trust provider).

    Từ danh sách thả xuống Trust provider, chọn nhà cung cấp tin cậy cụ thể mà bạn đã tạo (ví dụ: nhà cung cấp OIDC bạn đã thiết lập với Cognito).

    Bạn có thể thêm nhiều nhà cung cấp tin cậy nếu cần (ví dụ: một cho danh tính người dùng và một cho quản lý thiết bị).

    -Tags (Thẻ - Tùy chọn):

    Ở thẻ value đã được xác minh ở đây vì đây là nhà cung cấp mà chúng ta đã tạo ở bước trước.

    -Xem lại và tạo Instance:

    Kiểm tra lại tất cả các cài đặt bạn đã cấu hình.

    ![instances](/images/images/8/instances2.png?featherlight=false&width=90pc)

6.   Khi bạn hài lòng, nhấp vào nút Create Verified Access instance.
