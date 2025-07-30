---
title : "Create Domain"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 2.4 </b> "
---


## Domain
1. Prepare a domain name

![](/images/images/5/imageroute1.png?featherlight=false&width=90pc)

{{% notice note %}}
If you do not have a domain name, register one or you will not be able to do the following.

{{% /notice %}}

If you do not have a domain name, follow these two ways:
Method 1: Register a domain name through AWS Route 53. Amazon will do all the necessary steps for you.
Method 2: Register a domain name through another provider (e.g. GoDaddy, Namecheap, Hostinger, PAVietnam, etc.)

{{% notice note %}}
If you register a domain name through another provider. You need to "delegate" the DNS management of that domain to Route 53
{{% /notice %}}
After successfully registering, you should update the Name Servers (NS) at your root domain provider:
Step 1: Create a Public Hosted Zone for your domain on Route 53:
-Log in to AWS Console, go to Route 53.
-Select Hosted zones > Create hosted zone.
-Enter your domain name (e.g. Workshop.com).
![](/images/images/5/Domain3.png?featherlight=false&width=90pc)
-Select Public hosted zone and create.
-After creating, Route 53 will give you 4 unique Name Servers (NS) (e.g. ns-xxx.awsdns-yy.org). Make a note of these 4 NS addresses.
![](/images/images/5/Domain4.png?featherlight=false&width=90pc)
Step 2:
- Log in to the domain management page of the provider where you registered your domain (e.g. GoDaddy, Namecheap).
- Find the DNS management section, domain settings, or change Name Servers (usually named like "DNS Management", "Manage Nameservers", "Domain Settings").
- Delete all default Name Servers of the current provider.
- Add 4 Name Servers that you got from Route 53 (in step 1).
- Save the changes.
2. Connect to AWS Certificate Manager (ACM)
Log in to AWS Console, go to Certificate Manager.
Select List certificates > Request > Next > Enter Domain name > Request.
![](/images/images/5/Domain5.png?featherlight=false&width=90pc)
![](/images/images/5/Domain6.png?featherlight=false&width=90pc)

Go back to Certificate Manager Console, select the newly created certificates > Create records in Route 53 > Create records.
![](/images/images/5/Domain7.png?featherlight=false&width=90pc)
Go back to Route 53 and select the Hosted zones you created. Now there is a new record in the Hosted zones.
![](/images/images/5/Domain8.png?featherlight=false&width=90pc)
Continue with Certificate Manager, select the created Certificate, check the status from Pending validation
to Issued, so now we have an AWS certificate.
![](/images/images/5/Domain9.png?featherlight=false&width=90pc)