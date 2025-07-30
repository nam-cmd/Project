---
title : "Tạo Lambda"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2.2 </b> "
---

#### Tạo Lambda

1. Quay về AWS Console, truy cập vào dịch vụ Lambda.

2. Trong Lambda Console chọn **Functions**, chọn **Create Functions**

![LAMDBA](/images/images/3/imagelamdb1.png?featherlight=false&width=90pc)

3. Trong Basic information đặt tên cho Function, Runtime chọn **Python 3.12**
Sau khi hoàn tất chọn **Create Function**.

![LAMDBA](/images/images/3/imagelamdba2.png?featherlight=false&width=90pc)

4. Sau đó bạn sẽ được đưa đến Function được tạo. Ở function của bạn chọn Code và kéo xuóng phần Code source. Trong phần Code  source thêm đoạn code sau. Sau đó chọn **Deploy**.
   
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
5. Sau khi Deploy thành công chọn Configuration, nhấn chọn edit. Trong phần Time out chỉnh thành 5 min 0 sec rồi nhấn save, chúng ta sẽ không thay đổi bất kỳ nào khác.

    ![LAMDBA](/images/images/3/imagelamdba4.png?featherlight=false&width=90pc)

    ![LAMDBA](/images/images/3/imagelamdb5.png?featherlight=false&width=90pc)