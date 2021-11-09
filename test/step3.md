Create company user:

Admin has all power in Company database.

`create user 'admin'@'localhost' identified by 'password';`{{execute}}

`grant all privileges on Company.* to 'admin'@'localhost';`{{execute}}

`FLUSH PRIVILEGES;`{{execute}}
 
Create user Manager which has all power exclude drop in Company database.

`create user 'manager'@'localhost' identified by 'password';`{{execute}}

`grant create,DELETE,INSERT,SELECT,UPDATE on Company.* to 'manager'@'localhost';`{{execute}}

`FLUSH PRIVILEGES;`{{execute}}

Create user Sale which can insert customer information, insert,update and select product information and orders.

`create user 'sale'@'localhost' identified by 'password';`{{execute}}

`grant INSERT on Company.customer to 'sale'@'localhost';`{{execute}}

`grant INSERT,UPDATE,SELECT on Company.product to 'sale'@'localhost';`{{execute}}

`grant INSERT, UPDATE, SELECT on Company.orders to 'sale'@'localhost';`{{execute}}

`FLUSH PRIVILEGES;`{{execute}}
