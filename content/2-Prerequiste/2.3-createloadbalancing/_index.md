---
title : "Create LOAD BALANCING"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

#### Create LOAD BALANCING

1. Go to AWS Console, access EC2 service, search for Load balancers, select **Create Load balancers**.

![MFA](/images/images/4/imageloadbl1.png?featherlight=false&width=90pc)

2. In Load balancer types select **Application Load Balancer**

In Basic configuration section, name the Load balancer, Scheme select **Internal**.
In Network mapping select **VPC and Subnets** created.
In Security groups section select **create a new security group**.
In Inbound rules section, enter as shown in the image. Then select **Create security group**.
After creating the security group, return to the Create Load balancer page. In the security group section, select the security group you just created.

In the Listeners and routing section, select **Create target group**.

Select Lamdba Function and name the target group, then click next. In the next section, select the Lamdba Function you created, version select $latest, click **Create target group**

Then return to Create Load balancers, in the Listeners and routing section, select the target group you just created, then click **Create Load balancers** again.

After creating, return to the Load balancers console to check if the newly created Load balancers are active.

![MFA](/images/images/4/imageloadbl2.png?featherlight=false&width=90pc)
![MFA](/images/images/4/imageloadbl3.png?featherlight=false&width=90pc)
![MFA](/images/images/4/imageloadbl4.png?featherlight=false&width=90pc)
![MFA](/images/images/4/imageloadbl5.png?featherlight=false&width=90pc)
![MFA](/images/images/4/imageloadbl6.png?featherlight=false&width=90pc)
![MFA](/images/4/imageloadbl7.png?featherlight=false&width=90pc)
! [MFA](/images/images/4/imageloadbl8.png?featherlight=false&width=90pc)
![MFA](/images/images/4/imageloadbl9.png?featherlight=false&width=90pc)
![MFA](/images/images/4/imageloadbl10.png?featherlight=false&width=90pc)
![MFA](/images/images/4/imageloadbl11.png?featherlight=false&width=90pc)
![MFA](/images/4/imageloadbl12.png?featherlight=false&width=90pc)
![MFA](/images/images/4/imageloadbl13.png?featherlight=false&width=90pc)