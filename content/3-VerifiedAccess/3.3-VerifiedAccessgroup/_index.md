---
title : "Verified Access group"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3.3. </b> "
---
### Verified Access group
1. Navigate to Verified Access Groups:

    -In the left navigation bar of the VPC console, scroll down to the Verified Access section.

    -Select Verified Access groups.

2. Begin creating a new Verified Access Group:

    -On the Verified Access groups page, click the Create Verified Access group button.
![instances](/images/images/8/instances3.png?featherlight=false&width=90pc)

3. Configure the Verified Access Group:

    -Verified Access instance:

    Select the Verified Access instance you created earlier from the drop-down list. A Verified Access group must always be associated with an instance.

    -Name tag:

    Enter a recognizable name for your Verified Access group (e.g. HRWebAppGroup or InternalToolsGroup).

    -Description (Optional):

    Provide a brief description of the purpose or applications in this group.

    -Policy definition:

    This is where you define the access policy for this group in Cedar. All applications (Verified Access Endpoints) in this group will inherit this policy.

    You can enter your policy directly into the editor.

    {{% notice info %}}
    permit(principal,action,resource)
    when {
    context.cognitopolicy.email_verified == "true"
    };
    {{% /notice %}}
    {{% notice %}}(Remember that the cognitopolicy must match the Policy reference name you gave your Trust Provider).{{% /notice %}}
    Tags (Optional):

    Add key-value tags to help you organize and manage your resources.
![instances](/images/images/8/instances4.png?featherlight=false&width=90pc)

4. When you are satisfied, click the Create Verified Access group button.
![instances](/images/images/8/instances5.png?featherlight=false&width=90pc)