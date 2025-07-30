---
title : "Verified Access endpoint"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 3.4. </b> "
---
### Verified Access endpoint
1. Truy cập dịch vụ VPC:

-Trong thanh tìm kiếm ở trên cùng, nhập "VPC" và chọn VPC từ kết quả.

-Hoặc, trong bảng điều khiển dịch vụ, tìm đến mục Networking & Content Delivery và chọn VPC.

2. Điều hướng đến Verified Access Endpoints:

-Trong thanh điều hướng bên trái của bảng điều khiển VPC, cuộn xuống phần Verified Access.

-Chọn Verified Access endpoints.

3. Bắt đầu tạo Verified Access Endpoint mới:

-Trên trang Verified Access endpoints, nhấp vào nút Create Verified Access endpoint.

![endpoint](/images/images/9/endpoint1.png?featherlight=false&width=90pc)

4. Cấu hình Verified Access Endpoint:

-Verified Access group (Nhóm truy cập đã được xác minh):

Chọn Verified Access group mà bạn đã tạo trước đó từ danh sách thả xuống. Endpoint này sẽ được gán vào nhóm đó và kế thừa các chính sách của nhóm.

-Endpoint details (Chi tiết điểm cuối):

Protocol (Giao thức): Giao thức mà Verified Access sẽ sử dụng để giao tiếp với đích đến của ứng dụng của bạn. Ở đây chúng ta chọn Http.

Attachment type (Loại đính kèm): Chọn VPC.

VPC: Chọn VPC đã chuẩn bị.

Endpoint type (Loại điểm cuối): Xác nhận lại loại đích đến của bạn (Load Balancer hoặc Network Interface). Ở đây là Load balancer.

Load balancer (Bộ cân bằng tải): Chọn Load balancer đã chuẩn bị.

![endpoint](/images/images/9/endpoint2.png?featherlight=false&width=90pc)

-Port (Cổng): Cổng mà Load Balancer của bạn lắng nghe lưu lượng truy cập cho ứng dụng đích, do chúng ta chọn Http nên Port của chúng ta là 80.

-Load balancer ARN (ARN bộ cân bằng tải): Bạn sẽ chọn ARN (Amazon Resource Name) của Application Load Balancer (ALB) hoặc Network Load Balancer (NLB) nội bộ của bạn từ danh sách thả xuống.

-Subnet (Mạng con): Bạn sẽ chọn các mạng con nơi Load Balancer của bạn được triển khai. Verified Access sẽ sử dụng các mạng con này để thiết lập kết nối. 

-Security groups (Nhóm bảo mật): Bạn sẽ chọn các nhóm bảo mật mà Verified Access sẽ sử dụng để cho phép truy cập vào Load Balancer của bạn. Đảm bảo rằng nhóm bảo mật của Load Balancer cho phép lưu lượng truy cập đến từ các nhóm bảo mật được Verified Access sử dụng. 

-Endpoint domain prefix (Tiền tố tên miền điểm cuối): Bạn có thể nhập một tiền tố tùy chỉnh cho tên miền của Endpoint (ví dụ: hr). Verified Access sẽ tạo một tên miền đầy đủ cho Endpoint của bạn dựa trên tiền tố này và tên miền mặc định của Verified Access (ví dụ: hr.example.verified-access.us-east-1.amazonaws.com). Điều này giúp bạn có một URL dễ nhớ hơn.

-Application details (Chi tiết ứng dụng): Application domain (Tên miền ứng dụng): Đây là trường để bạn nhập tên miền mà người dùng sẽ sử dụng để truy cập ứng dụng của bạn (ví dụ: hr.buisiness.id.vn). Đây là tên miền tùy chỉnh mà bạn muốn ánh xạ tới Verified Access Endpoint.

-Domain certificate ARN (ARN chứng chỉ tên miền): Nếu bạn sử dụng tên miền ứng dụng tùy chỉnh, bạn cần cung cấp ARN của chứng chỉ TLS/SSL hợp lệ được quản lý bởi AWS Certificate Manager (ACM) trong cùng khu vực. Chứng chỉ này sẽ được Verified Access sử dụng để mã hóa lưu lượng truy cập từ người dùng đến Endpoint của bạn.

![endpoint](/images/images/9/endpoint3.png?featherlight=false&width=90pc)

-Xem lại và tạo Endpoint:

Kiểm tra lại tất cả các cài đặt bạn đã cấu hình.

Khi bạn hài lòng, nhấp vào nút Create Verified Access endpoint.

![endpoint](/images/images/9/endpoint4.png?featherlight=false&width=90pc)

5. Bước Cực Kỳ Quan Trọng Sau Khi Tạo Endpoint: 

Sau khi Verified Access endpoint được tạo và chuyển sang trạng thái active:

Lấy Redirect URI: Đi tới chi tiết của endpoint bạn vừa tạo. Trong phần Details hoặc Summary, bạn sẽ tìm thấy một Endpoint domain (ví dụ: hr-app.example.verified-access.us-east-1.amazonaws.com).

Cập nhật IdP của bạn: Sử dụng tên miền này để xây dựng Redirect URI cho ứng dụng khách của bạn trong Identity Provider (IdP) của bạn (ví dụ: Cognito, Okta, Azure AD). Redirect URI sẽ có dạng:
https://<ENDPOINT_DOMAIN>/oauth2/idpresponse

Ví dụ: https://hr-app.example.verified-access.us-east-1.amazonaws.com/oauth2/idpresponse
Bạn phải thêm URI này vào danh sách các URI được phép (allowed redirect URIs) trong cấu hình ứng dụng OIDC của bạn trên IdP (ví dụ: trong Amazon Cognito User Pool App client). Nếu không, quá trình xác thực sẽ thất bại sau khi người dùng đăng nhập vào IdP.
