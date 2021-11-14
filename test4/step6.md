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

`docker exec -it mysql /bin/bash`{{execute}}

Login as root user

`mysql -r -psecret`{{execute}}

Check the existing databases

`show databases;`{{execute}}

Use Wordpress databases, which Wordpress and WooCommerce data are stored in this database

`use wordpress;`{{execute}}

Check the existing tables

`show tables;`{{execute}}

You may see some tables name as wp_, wc_ at first which mean Wordpress and Woocommerce

The review and comment we just leave are storing in wp_comments, let see can we found something

Check the attributes of the table

`describe wp_comments;`{{execute}}

There is 15 attributes, seem it include some personal data as well like author email, ip address, website

![圖片](https://user-images.githubusercontent.com/74434769/141664199-61dc5078-a4cb-44f8-8de8-8bc62588a1ec.png)

Let try to select some data related to user

`select comment_ID,comment_author,comment_author_email,comment_author_url,comment_author_IP, comment_content, comment_agent from wp_comments;`{{execute}}

You may see the review and comment we just post

These data are contain some personal data like Name, email,website, ip and the device information

![圖片](https://user-images.githubusercontent.com/74434769/141664293-2e3814ce-8581-4a61-88fd-2be3eef3950a.png)


