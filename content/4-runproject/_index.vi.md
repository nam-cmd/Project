---
title : "Run Project"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 4. </b> "
---

### Run Project

1. Sau khi Verified Access endpoint được tạo và chuyển sang trạng thái active.

    Bước tiếp theo là tạo một bản ghi mới: bản ghi tên C (CNAME) với tên miền phụ là "HR" để phù hợp với miền ứng dụng.

    Chúng ta quay lại Route53 > Hosted zones đang sử dụng > Create record 

    Record name(Tên bản ghi) : hr.

    Record type(Loại bản ghi): CNAME – Routes traffic to another domain name and to some AWS resources.

    Value: endpoint domain lấy từ Verified Access endpoints.

    Nhấp vào nút Create record.

![endpoint](/images/images/9/endpoint5.png?featherlight=false&width=90pc)
 
2. Sau khi hoàn tất các bước cấu hình này, để kiểm tra ứng dụng, chúng ta cần mở một cửa sổ mới trong trình duyệt và nhập URL: <https://hr.Yourdomain.com>. Ở đây tên miền của tôi là: https://hr.builder.id.com. Sẽ hiện ra trang Wb của chúng ta.

    Tiếp theo nhập địa chỉ email và mật khẩu user 1 chúng ta đã tạo ở phần cognito user pools rồi nhấn Sign in.

    ![endpoint](/images/images/9/endpoint6.png?featherlight=false&width=90pc)

    Tiếp theo trang web sẽ yêu cầu chúng ta thay đổi mật khẩu cho user1, nhập mật khẩu mới rồi nhấn Send.

    ![endpoint](/images/images/9/endpoint7.png?featherlight=false&width=90pc)

    ![endpoint](/images/images/9/endpoint8.png?featherlight=false&width=90pc)

    Sau khi nhấn Send chúng ta đã đăng nhập vào HR application welcome to the HR.

    ![endpoint](/images/images/9/endpoint9.png?featherlight=false&width=90pc)

    Tiếp tục chúng ta mởi một tap mới và đăng nhập với user2, các bước thực hiện giống như với user1. Nhưng đăng nhập không thành công.

    ![endpoint](/images/images/9/endpoint10.png?featherlight=false&width=90pc)

    Bời vì khi chúng ta thiết lập nhà cung cấp tin cậy Verified Access, đã cấu hình một chính sách Cognito chỉ cấp quyền truy cập cho những người dùng đã xác minh email(user1). Do đó, người dùng có email chưa được xác minh sẽ không được cấp quyền truy cập(user2). 

    ![Cognito](/images/images/6/Cognito5.png?featherlight=false&width=90pc)
