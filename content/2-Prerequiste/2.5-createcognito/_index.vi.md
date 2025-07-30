---
title : "Tạo cognito user pools"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 2.5 </b> "
---

## Tạo cognito user pools

1. Vào AWS Console, truy cập vào dịch vụ **Cognito**, tìm kiếm Load balancers, chọn **User Pools**. Nhấn **Create User Pool**.

![Cognito](/images/images/6/Cognito1.png?featherlight=false&width=90pc)

2. Application type chọn Traditional web application.
    Name your application: Nhập một tên cho User Pool của bạn (ví dụ: MyWebAppUserPool hoặc MobileAppUsers). Tên này chỉ hiển thị trong bảng điều khiển AWS.

    Options for sign-in identifiers: chọn Email .

    Required attributes for sign-up: chọn Email.

    Add a return URL: nhập URL callback của bạn.

    {{% notice note %}}URL Callback bạn cung cấp cho Cognito (hoặc bất kỳ nhà cung cấp danh tính nào) phải khớp chính xác với URL mà ứng dụng của bạn sẽ xử lý việc chuyển hướng sau xác thực.{{% /notice %}}

    Nhấp **Create user directory**.

![Cognito](/images/images/6/Cognito1.png?featherlight=false&width=90pc)
3. Sau khi tạo xong User pool ta quay trở lại User pool Console chọn User pool vừa tạo.
 Ở thanh điều khiển chọn User management rồi chọn Create user.

![Cognito](/images/images/6/Cognito3.png?featherlight=false&width=90pc)

4. Ở Create user nhập như trong hình rồi chọn Create user.
![Cognito](/images/images/6/Cognito4.png?featherlight=false&width=90pc)
chúng ta lại làm lại một lần nữa nhưng ở phần Email address chúng ta sẽ không đánh dấu tích vào Mark email address as verified.
Sau khi tạo xong chúng ta có 2 user sau:
![Cognito](/images/images/6/Cognito5.png?featherlight=false&width=90pc)

5. Sau khi hoàng thành sao chép tên miền Cognito của mình. Sau đó, tiếp tục sao chép Client ID và Client Secret mà tôi đã tạo cho ứng dụng khách. Tổng cộng, đã có cả bốn thông tin cần thiết trong bộ nhớ tạm: ID nhóm người dùng, Client ID và Client Secret của tên miền Cognito. Giờ đây, với tất cả những thông tin quan trọng này, chúng ta đã sẵn sàng sử dụng chúng để tạo một Verified Access trust provider trong AWS.
![Cognito](/images/images/6/Cognito6.png?featherlight=false&width=90pc)
![Cognito](/images/images/6/Cognito7.png?featherlight=false&width=90pc)