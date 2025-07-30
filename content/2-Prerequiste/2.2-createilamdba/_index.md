---
title : "Create LAMBDA"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

#### CREAT LAMBDA

1. Return to AWS Console, access the Lambda service.

2. In Lambda Console select **Functions**, select **Create Functions**

![LAMDBA](/images/images/3/imagelamdb1.png?featherlight=false&width=90pc)

3. In Basic information, name the Function, Runtime select **Python 3.12**
After completing, select **Create Function**.

![LAMDBA](/images/images/3/imagelamdba2.png?featherlight=false&width=90pc)

4. Then you will be taken to the created Function. In your function select Code and scroll down to the Code source section. In the Code source section add the following code. Then select **Deploy**.

    ```import json
    def lambda_handler(event, context):
    response = {
        "statusCode": 200,
        "headers": {
            "Content-Type": "text/html",
        },
        "body": """
        <!DOCTYPE html>
        <html>
        <head>
            <title>Welcome to HR Application</title>
            <style>
                body {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    height: 100vh;
                    margin: 0;
                    background-color: powderblue;
                }
                h1 {
                    color: teal;
                    font-family: verdana;
                    font-size: 300%;
                }
            </style>
        </head>
        <body>
            <h1>Welcome to the HR Application</h1>
        </body>
        </html>
        """
    }

    return response
    ```
![MFA](/images/images/3/imagelamdba3.png?featherlight=false&width=90pc)
5. After successfully Deploy, select Configuration, click edit. In the Time out section, set it to 5 min 0 sec and then click save, we will not change anything else.

![LAMDBA](/images/images/3/imagelamdba4.png?featherlight=false&width=90pc)

![LAMDBA](/images/images/3/imagelamdb5.png?featherlight=false&width=90pc)