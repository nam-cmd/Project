---
title : "AWS Services to Prepare for"
date : "2025-07-28"
weight : 2
chapter : false
pre : " <b> 2.</b> "
---

This entire architecture is deployed in a VPC (Virtual Private Cloud), leveraging two Availability Zones to ensure high availability.

In this VPC, I have set up two private subnets, creating a secure environment for our resources. To distribute traffic efficiently and securely, I use an Internal Application Load Balancer. This is a key component that routes requests to our application.

The unique feature of this architecture is the use of AWS Lambda as the primary compute environment. Instead of traditional servers, we will host the entire simple HR application website in Lambda functions. This approach helps to minimize operational costs, eliminate the burden of server management, and automatically scale on demand.

In the next presentation, I'll walk you through step-by-step how to build this architecture directly in the AWS console, showing how surprisingly simple the deployment process is.


### Content
  - [Create VPC](2.1-createvpc/)
  - [Create Lambda](2.2-createlambda/)
  - [Create Load Balancing ](2.1.3-createloadbalancing/)
  - [Create Domain](2.4-createdomain/)
  - [Create Cognito user pools](2.5-createcognito/)
  