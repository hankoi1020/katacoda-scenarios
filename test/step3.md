Create company user:

Create user Admin which has all power in Company database and password as "password".

`create user 'admin'@'localhost' identified by 'password';`{{execute}}

Grant all privileges:

`grant all privileges on Company.* to 'admin'@'localhost';`{{execute}}
 
Create user Manager which has all power exclude DROP in Company database

`create user 'manager'@'localhost' identified by 'password';`{{execute}}

`grant create,DELETE,INSERT,SELECT,UPDATE on Company.* to 'manager'@'localhost';`{{execute}}


Create user Sale which can insert customer information, insert,update and select product information and orders.

`create user 'sale'@'localhost' identified by 'password';`{{execute}}

`grant INSERT on Company.customer to 'sale'@'localhost';`{{execute}}

`grant INSERT,UPDATE,SELECT on Company.product to 'sale'@'localhost';`{{execute}}

`grant INSERT, UPDATE, SELECT on Company.orders to 'sale'@'localhost';`{{execute}}

After grant a privilege, reload the grant table by using this command

`FLUSH PRIVILEGES;`{{execute}}
