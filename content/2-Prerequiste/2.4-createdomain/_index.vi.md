---
title : "Tạo Domain"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 2.4 </b> "
---


## Domain
1. Chuẩn bị một tên miền 

![](/images/images/5/imageroute1.png?featherlight=false&width=90pc)

{{% notice note %}}
Nếu bạn không có một tên miền hãy đang ký một tên miền nếu không thì không thể thực hiện các phần sau.
{{% /notice %}}

Nếu bạn chưa đang ký tên miền thì hãy làm theo hai cách sau đây:
Cách 1: Đăng ký tên miền thông qua AWS Route 53. Amazon sẽ thực hiện toàn bộ các bước cần thiết cho bạn.
Cách 2: Đăng ký tên miền thông qua một nhà cung cấp khác (ví dụ: GoDaddy, Namecheap, Hostinger, PAVietnam, vv.)
{{% notice note %}}
Nếu bạn đăng ký tên miền thông qua một nhà cung cấp khác. Bạn cần "ủy quyền" việc quản lý DNS của tên miền đó cho Route 53
{{% /notice %}}
Sau khi đăng ký thành công, bạn nên cập nhật lại Name Servers (NS) tại nhà cung cấp tên miền gốc của bạn:
Bước 1: Tạo một Public Hosted Zone cho tên miền của bạn trên Route 53:
-Đăng nhập vào AWS Console, vào Route 53.
-Chọn Hosted zones > Create hosted zone.
-Nhập tên miền của bạn (ví dụ: Workshop.com).
![](/images/images/5/Domain3.png?featherlight=false&width=90pc)
-Chọn Public hosted zone và tạo.
-Sau khi tạo, Route 53 sẽ cấp cho bạn 4 Name Servers (NS) duy nhất (ví dụ: ns-xxx.awsdns-yy.org). Ghi lại 4 địa chỉ NS này.
![](/images/images/5/Domain4.png?featherlight=false&width=90pc)
Bước 2:
- Đăng nhập vào trang quản lý tên miền của nhà cung cấp bạn đã đăng ký tên miền (ví dụ: GoDaddy, Namecheap).
- Tìm phần quản lý DNS, cài đặt tên miền, hoặc thay đổi Name Servers (thường có tên như "DNS Management", "Manage Nameservers", "Domain Settings").
- Xóa tất cả các Name Servers mặc định của nhà cung cấp hiện tại.
- Thêm 4 Name Servers mà bạn đã lấy từ Route 53 (ở bước 1).
- Lưu lại thay đổi.
2. kết nối với AWS Certificate Manager (ACM)
Đăng nhập vào AWS Console, vào Certificate Manager.
Chọn List certificates > Request > Next > Nhập tên Domain > Request.
![](/images/images/5/Domain5.png?featherlight=false&width=90pc)
![](/images/images/5/Domain6.png?featherlight=false&width=90pc)

Quay lại Certificate Manager Console chọn certificates vừa tạo > Create records in Route 53 > Create records.
![](/images/images/5/Domain7.png?featherlight=false&width=90pc)
Quay lại Route 53 chọn vào Hosted zones đã tạo. Lúc này trong Hosted zones đã có thêm 1 records mới.
![](/images/images/5/Domain8.png?featherlight=false&width=90pc)
tiếp tục với Certificate Manager chọn vào Certificate đã tạo kiểm tra phần status từ trạng Pending validation
đến trạng thái Issued nên bây giờ chúng ta có chứng chỉ AWS.
![](/images/images/5/Domain9.png?featherlight=false&width=90pc)