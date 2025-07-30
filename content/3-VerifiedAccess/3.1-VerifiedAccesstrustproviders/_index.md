---
title : "Verified Access trust providers"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 3.1. </b> "
---

## Create Verified Access trust providers

1. Log in to the AWS Management Console.

2. Go to the VPC service.

3. In the left navigation bar, scroll down and find Verified Access. Select Trust providers.
![access](/images/images/7/access1.png?featherlight=false&width=90pc)

4. Select Create Verified Access trust provider.

Optional:

-Name tag: Enter a memorable name for your trust provider (e.g., MyOrgOIDCProvider).

-Description: Provide a brief description.

-Policy reference name: Enter a unique identifier that will be used in Verified Access policy rules. For example: my_oidc_idp.

-Trust provider type: Select User trust provider.

-User trust provider type: Select OpenID Connect (OIDC).

-Configure OIDC options:

-Issuer: Enter the issuer URL from your IdP (https://cognito-idp.<region>.amazonaws.com/<UserPoolID>).

-Authorization endpoint: Enter the authorization endpoint URL from your IdP (https://<CognitoDomain>.amazoncognito.com/oauth2/authorize).

-Token endpoint: Enter the token endpoint URL from your IdP (https://<CognitoDomain>.amazoncognito.com/oauth2/token).

-User info endpoint: Enter the user info endpoint URL from your IdP (https://<CognitoDomain>.amazoncognito.com/oauth2/userInfo).

-Client ID: Enter the Client ID from your saved IdP.

-Client secret: Enter the Client Secret from your saved IdP.

-Scope: Enter "openid profile email".

![access](/images/images/7/access2.png?featherlight=false&width=90pc) 
![access](/images/images/7/access3.png?featherlight=false&width=90pc)

5. Select Create Verified Access trust provider. 
![access](/images/images/7/access4.png?featherlight=false&width=90pc)