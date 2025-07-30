---
title : "Introduction"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
**AWS Verified Access** is an Amazon Web Services (AWS) service designed to provide secure, seamless access to corporate applications and resources without the need for a traditional virtual private network (VPN). It is built on the principle of Zero Trust, meaning no user or device is trusted by default.

Highlights:

Zero Trust-based access: AWS Verified Access continuously authenticates each access request against granular, contextual access policies, ensuring that access is granted and maintained only when users meet specific security requirements.

Advanced security: It allows you to define sophisticated access policies based on user identity (integrating with AWS IAM Identity Center or third-party identity providers such as Okta, Azure AD, Google Workspace) and device security status (integrating with third-party device management services).

Simplify the user experience: Users can access applications directly through a browser or app without installing and configuring a VPN client, making the experience more seamless.

Simplify security operations: Administrators can create, group, and manage access policies for applications and resources with similar security requirements from a single interface, simplifying policy management.

Scalability: AWS Verified Access is designed to scale with your AWS environment, making it easy to manage and secure access to applications as your organization grows.

Observability: Provides comprehensive logging and visibility into access attempts, helping to quickly identify and resolve security and connectivity issues.

Multi-protocol support: Initially focused on HTTP(S), AWS Verified Access now supports connections over non-HTTP(S) protocols, expanding its application capabilities.