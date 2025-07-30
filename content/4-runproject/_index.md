---
title : "Run Project"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 4. </b> "
---


### Run Project

1. After the Verified Access endpoint is created and switched to active state.

The next step is to create a new record: a C-name record (CNAME) with the subdomain name "HR" to match the application domain.

We go back to Route53 > Hosted zones in use > Create record

Record name(Record name): hr.

Record type(Record type): CNAME – Routes traffic to another domain name and to some AWS resources.

Value: endpoint domain taken from Verified Access endpoints.

Click the Create record button.

![endpoint](/images/images/9/endpoint5.png?featherlight=false&width=90pc)

2. After completing these configuration steps, to test the application, we need to open a new window in the browser and enter the URL: <https://hr.Yourdomain.com>. Here my domain name is: https://hr.builder.id.com. Our Wb page will appear.

Next, enter the email address and password of user 1 that we created in the cognito user pools section and click Sign in.

![endpoint](/images/images/9/endpoint6.png?featherlight=false&width=90pc)

Next, the website will ask us to change the password for user1, enter the new password and click Send.

![endpoint](/images/images/9/endpoint7.png?featherlight=false&width=90pc)

![endpoint](/images/images/9/endpoint8.png?featherlight=false&width=90pc)

After clicking Send, we have logged into the HR application welcome to the HR.

![endpoint](/images/images/9/endpoint9.png?featherlight=false&width=90pc)

Next, we open a new tab and log in with user2, the steps are the same as with user1. But the login is not successful.

![endpoint](/images/images/9/endpoint10.png?featherlight=false&width=90pc)

Because when we set up the Verified Access trust provider, we configured a Cognito policy to only grant access to users with verified email(user1). Therefore, users with unverified email will not be granted access(user2).

![Cognito](/images/images/6/Cognito5.png?featherlight=false&width=90pc)