## Discover Sensitive Information in MySQL (continue)

### wp_usermeta

The next table is wp_usermeta, which storing metadata of users

Check out the attributes

`describe wp_usermeta;`{{execute}}

![圖片](https://user-images.githubusercontent.com/74434769/141664397-7f0f2b36-086f-4bdc-a94d-382d512c4cbf.png)

Check out the data

`Select * from wp_usermeta;`{{execute}}

You can see it storing user information

- **Name for Creating account,Shipping, Billing**
- **Address for Shipping and Billing**
- **Email Address**
- **Phone number**

![圖片](https://user-images.githubusercontent.com/74434769/141664540-796c12d3-8051-49a9-90ac-eb392f475dee.png)

### wp_users

There is also a table call wp_users to store the account information

Check out the attributes

`describe wp_users;`{{execute}}

![圖片](https://user-images.githubusercontent.com/74434769/141664559-f124df09-ff4b-449d-b501-c88f6993deb9.png)

Check out the data

`select * from wp_users;`{{execute}}

![圖片](https://user-images.githubusercontent.com/74434769/141664578-951e2071-2152-45f3-98a3-e3df5641cdd6.png)

You can see it storing the **Username** , **Hashed Password**, **Email** and **Website**

Do you remember both user password are the same as "test", however the hashed password are not the same.

Therefore, you can see Wordpress will hashed the user password with salting to protect their password subject to rainbow table attack once the hash leaked



