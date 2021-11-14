## Grant privileges 

Create company user and grant a suitable privilege by their rule

Create user Admin which has all power in Company database and password as "password".

`create user 'admin'@'localhost' identified by 'password';`{{execute}}

Grant all privileges to admin since admin user need to manage the database:

`grant all privileges on Company.* to 'admin'@'localhost';`{{execute}}
 
Create user Manager which has all power exclude DROP in Company database

Manager can manager all the record in database, but they cannot remove a whole table or database

`create user 'manager'@'localhost' identified by 'password';`{{execute}}

`grant create,DELETE,INSERT,SELECT,UPDATE on Company.* to 'manager'@'localhost';`{{execute}}


Create user Sale which can insert customer information, insert,update and select product information and orders.

Sale only need to process the order and product, or add a new customer. But they are not allow to view the customer information since it is persenal data.

`create user 'sale'@'localhost' identified by 'password';`{{execute}}

`grant INSERT on Company.customer to 'sale'@'localhost';`{{execute}}

`grant INSERT,UPDATE,SELECT on Company.product to 'sale'@'localhost';`{{execute}}

`grant INSERT, UPDATE, SELECT on Company.orders to 'sale'@'localhost';`{{execute}}

After grant a privilege, reload the grant table by using this command

`FLUSH PRIVILEGES;`{{execute}}
