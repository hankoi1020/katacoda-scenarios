## Discover Sensitive Information in Wordpress

Beside Order, there still have some sensitive information store in Wordpress / Woocommerce

In Users > All Users, you can click the user name to check their information

![圖片](https://user-images.githubusercontent.com/74434769/141663399-db659f36-f3b0-4f59-b356-350be458558e.png)

![圖片](https://user-images.githubusercontent.com/74434769/141663410-d4ea86f2-a01e-4a86-9b58-8d53a99eae5d.png)

In sample user page, it include the name, email and website

![圖片](https://user-images.githubusercontent.com/74434769/141663427-68cce29f-725c-487b-b521-e10d885a8027.png)

Go down more you can see the Billing address and Shipping address as well with phone number and email address

![圖片](https://user-images.githubusercontent.com/74434769/141663444-60953c4b-7082-4cd3-983e-021105accdd4.png)

![圖片](https://user-images.githubusercontent.com/74434769/141663445-4fb8b3a9-2655-4dee-b3e0-495b339826bd.png)

## Discover Sensitive Information in MySQL

This data in Wordpress and Woocommerce will store into MYSQL database

Open a new terminal to explore the MySQL database

Go into the container by this command

`docker exec -it mysql /bin/bash`

Login as root user

`mysql -r -psecret`


