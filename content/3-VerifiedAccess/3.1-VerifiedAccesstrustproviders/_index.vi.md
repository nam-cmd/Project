---
title : "Verified Access trust providers"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 3.1. </b> "
---

## Tạo Verified Access trust providers

1. Đăng nhập vào AWS Management Console.

2. Đi đến dịch vụ VPC.

3. Trong thanh điều hướng bên trái, cuộn xuống và tìm Verified Access. Chọn Trust providers.
![access](/images/images/7/access1.png?featherlight=false&width=90pc)

4. Chọn Create Verified Access trust provider.

   Tùy chọn:

   -Name tag (Tên thẻ): Nhập tên dễ nhớ cho nhà cung cấp tin cậy của bạn (ví dụ: MyOrgOIDCProvider).

   -Description (Mô tả): Cung cấp mô tả ngắn gọn.

   -Policy reference name (Tên tham chiếu chính sách): Nhập một định danh duy nhất sẽ được sử dụng trong các quy tắc chính sách của Verified Access. Ví dụ: my_oidc_idp.

   -Trust provider type (Loại nhà cung cấp tin cậy): Chọn User trust provider.

   -User trust provider type (Loại nhà cung cấp tin cậy người dùng): Chọn OpenID Connect (OIDC).

   -Cấu hình OIDC options (Tùy chọn OIDC):

   -Issuer (Nhà phát hành): Nhập URL của nhà phát hành từ IdP của bạn(https://cognito-idp.<region>.amazonaws.com/<UserPoolID>).

   -Authorization endpoint (Điểm cuối ủy quyền): Nhập URL điểm cuối ủy quyền từ IdP của bạn(https://<CognitoDomain>.amazoncognito.com/oauth2/authorize).

   -Token endpoint (Điểm cuối mã thông báo): Nhập URL điểm cuối mã thông báo từ IdP của bạn(https://<CognitoDomain>.amazoncognito.com/oauth2/token).

   -User info endpoint (Điểm cuối thông tin người dùng): Nhập URL điểm cuối thông tin người dùng từ IdP của bạn(https://<CognitoDomain>.amazoncognito.com/oauth2/userInfo).

   -Client ID (Mã khách hàng): Nhập Client ID từ IdP đã lưu của bạn.

   -Client secret (Bí mật khách hàng): Nhập Client Secret từ IdP đã lưu  của bạn.

   -Scope: Nhập "openid profile email". 

    ![access](/images/images/7/access2.png?featherlight=false&width=90pc)
    ![access](/images/images/7/access3.png?featherlight=false&width=90pc)
   
5.   Chọn Create Verified Access trust provider.
    ![access](/images/images/7/access4.png?featherlight=false&width=90pc)

