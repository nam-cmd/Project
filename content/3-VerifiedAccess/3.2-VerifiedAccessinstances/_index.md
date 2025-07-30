---
title : "Verified Access instances"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.2. </b> "
---
### Verified Access instances

1. Sign in to the AWS Management Console

2. Access the VPC service:

-In the search bar at the top, type "VPC" and select VPC from the results.

-Or, in the service console, go to Networking & Content Delivery and select VPC.

3. Navigate to Verified Access Instances:

-In the left navigation bar of the VPC console, scroll down to the Verified Access section.

-Select Verified Access instances.

4. Start creating a new Verified Access Instance:

-On the Verified Access instances page, click the Create Verified Access instance button.

![instances](/images/images/8/instances1.png?featherlight=false&width=90pc)

5. Configure Verified Access Instance:

-Name tag:

Enter a recognizable name for your Verified Access instance (e.g. MyInternalAppVAInstance). This name will appear in the dashboard and related resources.

-Description (Optional):

Provide a brief description of the purpose of this instance.

-Trust providers:

This is the most important part. You need to select (or add new) the trust providers you created earlier.

-Click Add trust provider.

In the pop-up window, select the type of trust provider (e.g. User trust provider).

From the Trust provider drop-down list, select the specific trust provider you created (for example, the OIDC provider you set up with Cognito).

You can add multiple trust providers if needed (for example, one for user identity and one for device management).

-Tags (Optional):

The value tag is verified here because this is the provider we created in the previous step.

-Review and Create Instance:

Double-check all the settings you configured.

![instances](/images/images/8/instances2.png?featherlight=false&width=90pc)

6. When you are satisfied, click the Create Verified Access instance button.