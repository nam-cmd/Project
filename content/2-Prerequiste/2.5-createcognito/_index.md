---
title : "Create cognito user pools"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 2.5 </b> "
---

## Create cognito user pools

1. Go to AWS Console, access **Cognito** service, search for Load balancers, select **User Pools**. Click **Create User Pool**.

![Cognito](/images/images/6/Cognito1.png?featherlight=false&width=90pc)

2. Application type select Traditional web application.

    Name your application: Enter a name for your User Pool (e.g. MyWebAppUserPool or MobileAppUsers). This name is only visible in the AWS console.

    Options for sign-in identifiers: select Email .

    Required attributes for sign-up: select Email.

    Add a return URL: enter your callback URL.

    {{% notice note %}}The Callback URL you provide to Cognito (or any identity provider) must exactly match the URL that your application will handle the redirection to after authentication.{{% /notice %}}

    Click **Create user directory**.

    ![Cognito](/images/images/6/Cognito1.png?featherlight=false&width=90pc)
3. After creating the User pool, return to the User pool Console and select the User pool you just created.

In the control bar, select User management and then select Create user.

![Cognito](/images/images/6/Cognito3.png?featherlight=false&width=90pc)

4. In Create user, enter as shown in the image and then select Create user.
![Cognito](/images/images/6/Cognito4.png?featherlight=false&width=90pc)
We do it again but in the Email address section we will not check Mark email address as verified.
After creating, we have the following 2 users:
![Cognito](/images/images/6/Cognito5.png?featherlight=false&width=90pc)

5. After successfully copying my Cognito domain. Next, I copied the Client ID and Client Secret that I created for the client. In total, I had all four pieces of information in the clipboard: the user pool ID, the Client ID, and the Client Secret of the Cognito domain. Now, with all of this important information, we are ready to use it to create a Verified Access trust provider in AWS.
![Cognito](/images/images/6/Cognito6.png?featherlight=false&width=90pc)
![Cognito](/images/images/6/Cognito7.png?featherlight=false&width=90pc)