---
title : "Verified Access group"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3.3. </b> "
---
### Verified Access group
1. Điều hướng đến Verified Access Groups:

    -Trong thanh điều hướng bên trái của bảng điều khiển VPC, cuộn xuống phần Verified Access.

    -Chọn Verified Access groups.

2. Bắt đầu tạo Verified Access Group mới:

    -Trên trang Verified Access groups, nhấp vào nút Create Verified Access group.

![instances](/images/images/8/instances3.png?featherlight=false&width=90pc)

3. Cấu hình Verified Access Group:

    -Verified Access instance (Instance truy cập đã được xác minh):

    Chọn Verified Access instance mà bạn đã tạo trước đó từ danh sách thả xuống. Một nhóm Verified Access luôn phải được liên kết với một instance.

    -Name tag (Tên thẻ):

    Nhập một tên dễ nhận biết cho Verified Access group của bạn (ví dụ: HRWebAppGroup hoặc InternalToolsGroup).

    -Description (Mô tả - Tùy chọn):

    Cung cấp mô tả ngắn gọn về mục đích hoặc các ứng dụng trong nhóm này.

    -Policy definition (Định nghĩa chính sách):

    Đây là nơi bạn định nghĩa chính sách truy cập cho nhóm này bằng ngôn ngữ Cedar. Tất cả các ứng dụng (Verified Access Endpoints) trong nhóm này sẽ kế thừa chính sách này.

    Bạn có thể nhập policy của mình trực tiếp vào trình soạn thảo.
    {{% notice info %}}
    permit(principal,action,resource)
    when {
    context.cognitopolicy.email_verified == "true"
    };
    {{% /notice %}}
    {{% notice %}}(Nhớ rằng cognitopolicy phải khớp với Policy reference name bạn đã đặt cho Trust Provider của mình).{{% /notice %}}
    Tags (Optional):
      
    -Tags (Thẻ - Tùy chọn):
    Thêm các thẻ key-value để giúp bạn tổ chức và quản lý tài nguyên của mình.
![instances](/images/images/8/instances4.png?featherlight=false&width=90pc)

4. Khi bạn hài lòng, nhấp vào nút Create Verified Access group.
![instances](/images/images/8/instances5.png?featherlight=false&width=90pc)