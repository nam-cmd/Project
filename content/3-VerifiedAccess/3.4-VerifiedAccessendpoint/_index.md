---
title : "Verified Access endpoint"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 3.4. </b> "
---
### Verified Access endpoint
1. Access the VPC service:

-In the search bar at the top, type "VPC" and select VPC from the results.

-Or, in the service console, navigate to Networking & Content Delivery and select VPC.

2. Navigate to Verified Access Endpoints:

-In the left navigation bar of the VPC console, scroll down to the Verified Access section.

-Select Verified Access endpoints.

3. Start creating a new Verified Access Endpoint:

-On the Verified Access endpoints page, click the Create Verified Access endpoint button.

![endpoint](/images/images/9/endpoint1.png?featherlight=false&width=90pc)

4. Configure Verified Access Endpoint:

-Verified Access group:

Select the Verified Access group you created earlier from the drop-down list. This endpoint will be assigned to that group and inherit the group's policies.

-Endpoint details:

Protocol: The protocol that Verified Access will use to communicate with your application's destination. Here we select Http.

Attachment type: Select VPC.

VPC: Select the prepared VPC.

Endpoint type: Confirm your destination type (Load Balancer or Network Interface). Here it is Load balancer.

Load balancer: Select the prepared Load balancer.

![endpoint](/images/images/9/endpoint2.png?featherlight=false&width=90pc)

-Port: The port where your Load Balancer listens for traffic for the target application, since we chose Http our Port is 80.

-Load balancer ARN: You will select the ARN (Amazon Resource Name) of your internal Application Load Balancer (ALB) or Network Load Balancer (NLB) from the drop-down list.

-Subnet: You will select the subnets where your Load Balancer is deployed. Verified Access will use these subnets to establish connectivity.

-Security groups: You will select the security groups that Verified Access will use to allow access to your Load Balancer. Make sure that the Load Balancer security group allows traffic from the security groups used by Verified Access.

-Endpoint domain prefix: You can enter a custom prefix for the Endpoint domain (for example, hr). Verified Access will generate a fully qualified domain name for your Endpoint based on this prefix and the default Verified Access domain (for example, hr.example.verified-access.us-east-1.amazonaws.com). This gives you an easier-to-remember URL.

-Application details: Application domain: This is where you enter the domain name that users will use to access your application (for example, hr.business.id.vn). This is the custom domain name that you want to map to the Verified Access Endpoint.

-Domain certificate ARN: If you use a custom application domain, you need to provide the ARN of a valid TLS/SSL certificate managed by AWS Certificate Manager (ACM) in the same region. This certificate will be used by Verified Access to encrypt traffic from users to your Endpoint.

![endpoint](/images/images/9/endpoint3.png?featherlight=false&width=90pc)

-Review and create Endpoint:

Check all the settings you have configured.

When you are satisfied, click the Create Verified Access endpoint button.

![endpoint](/images/images/9/endpoint4.png?featherlight=false&width=90pc)

5. Extremely Important Steps After Creating the Endpoint:

Once the Verified Access endpoint is created and active:

Get the Redirect URI: Go to the details of the endpoint you just created. In the Details or Summary section, you will find an Endpoint domain (e.g. hr-app.example.verified-access.us-east-1.amazonaws.com).

Update your IdP: Use this domain to build the Redirect URI for your client in your Identity Provider (IdP) (e.g. Cognito, Okta, Azure AD). The redirect URI will look like this:
https://<ENDPOINT_DOMAIN>/oauth2/idpresponse

For example: https://hr-app.example.verified-access.us-east-1.amazonaws.com/oauth2/idpresponse
You must add this URI to the list of allowed redirect URIs in your OIDC application configuration on the IdP (for example, in the Amazon Cognito User Pool App client). Otherwise, authentication will fail after the user logs in to the IdP.