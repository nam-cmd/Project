---
title : "Tạo LOAD BALANCING"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

#### Tạo LOAD BALANCING

1. Vào AWS Console, truy cập vào dịch vụ EC2, tìm kiếm Load balancers, chọn **Create Load balancers**.

![MFA](/images/images/4/imageloadbl1.png?featherlight=false&width=90pc)

2. Trong Load balancer types chọn **Application Load Balancer** 
Trong phần Basic configuration đặt tên cho Load balancer, Scheme chọn **Internal**.
Trong Network mapping chọn **VPC và Subnets** đã tạo.
Ở phần Security groups chọn  **create a new security group**.
Ở phần Inbound rules nhập như trong hình. Rồi chọn **Create security group**. 
Sau khi tạo xong security group quay về trang Create Load balancer. Trong phần security group chọn security group vừa tạo.
Ở phần Listeners and routing chọn **Create target group**.
Chọn Lamdba Function và đặt tên cho target group, rồi nhấn next. Trong phần tiếp theo chọn Lamdba Function đã tạo, version chọn $latest, nhấn **Create target group**
Sau đó quay lại Create Load balancers phần Listeners and routing chọn target group vừa tạo rồi nhấn lại **Create Load balancers**.
Sau khi tạo xong quay lại Load balancers console khiểm tra xem Load balancers vừa tạo có được active hay không.

![MFA](/images/images/4/imageloadbl2.png?featherlight=false&width=90pc)
![MFA](/images/images/4/imageloadbl3.png?featherlight=false&width=90pc)
![MFA](/images/images/4/imageloadbl4.png?featherlight=false&width=90pc)
![MFA](/images/images/4/imageloadbl5.png?featherlight=false&width=90pc)
![MFA](/images/images/4/imageloadbl6.png?featherlight=false&width=90pc)
![MFA](/images/4/imageloadbl7.png?featherlight=false&width=90pc)
![MFA](/images/images/4/imageloadbl8.png?featherlight=false&width=90pc)
![MFA](/images/images/4/imageloadbl9.png?featherlight=false&width=90pc)
![MFA](/images/images/4/imageloadbl10.png?featherlight=false&width=90pc)
![MFA](/images/images/4/imageloadbl11.png?featherlight=false&width=90pc)
![MFA](/images/4/imageloadbl12.png?featherlight=false&width=90pc)
![MFA](/images/images/4/imageloadbl13.png?featherlight=false&width=90pc)