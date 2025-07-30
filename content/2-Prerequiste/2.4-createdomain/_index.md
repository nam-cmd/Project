---
title : "Create Domain"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 2.4 </b> "
---

## Domain
1. Prepare a domain name

![MFA](/images/images/5/imageroute1.png?featherlight=false&width=90pc)

{{% notice note %}}
If you do not have a domain name, register one or you will not be able to do the following.

{{% /notice %}}

If you have not registered a domain name, follow these two ways:
Method 1: Register a domain name through AWS Route 53. Amazon will do all the necessary steps for you.
Method 2: Register a domain name through another provider (e.g. GoDaddy, Namecheap, Hostinger, PAVietnam, etc.)
{{% notice note %}}
If you register a domain name through another provider. You need to "delegate" the management of DNS for that domain name to Route 53
{{% /notice %}}
After successful registration, you should update the Name Servers (NS) at your original domain provider:
Step 1: Create a Public Hosted Zone for your domain on Route 53:
-Log in to AWS Console, go to Route 53.
-Select Hosted zones > Create hosted zone.
-Enter your domain name (e.g. Workshop.com).
![MFA](/images/images/5/Domain3.png?featherlight=false&width=90pc)
-Select Public hosted zone and create.
-After creation, Route 53 will give you 4 unique Name Servers (NS) (e.g. ns-xxx.awsdns-yy.org). Write down these 4 NS addresses.
![MFA](/images/images/5/Domain4.png?featherlight=false&width=90pc)
Step 2:
-Log in to the domain management page of the provider where you registered your domain (e.g. GoDaddy, Namecheap).
-Find the DNS management section, set up your domain name, or change the Name Servers (usually named like "DNS Management", "Manage Nameservers", "Domain Settings").
-Delete all the default Name Servers of your current provider.
-Add the 4 Name Servers that you got from Route 53 (in step 1).
-Save the changes.
2. Connect to AWS Certificate Manager (ACM)
Log in to AWS Console, go to Certificate Manager.
Select List certificates > Request > Next > Enter Domain name > Request.
![MFA](/images/images/5/Domain5.png?featherlight=false&width=90pc)
![MFA](/images/5/Domain6.png?featherlight=false&width=90pc)

Return to Certificate Manager Console, select the newly created certificates > Create records in Route 53 > Create records.
![MFA](/images/images/5/Domain7.png?featherlight=false&width=90pc)
Return to Route 53, select the created Hosted zones. Now in Hosted zones, there is a new record.
![MFA](/images/images/5/Domain8.png?featherlight=false&width=90pc)
Continue with Certificate Manager, select the created Certificate, check the status from Pending validation
to Issued, so now we have an AWS certificate.
![MFA](/images/images/5/Domain9.png?featherlight=false&width=90pc)