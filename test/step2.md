Let create a simple company scenario in MySQL by create different user.

Go in the mysql container bash
 `docker exec -it mysql /bin/sh`{{execute}}
 
Login into MySql as root
 `mysql -uroot -p`{{execute}}
 `secret`{{execute}}
 
Create database Company with tables.
`create database Company;`
`use Company`;
`CREATE TABLE product(id int, name VARCHAR(20), price int, description varchar(50));`{{execute}}
`create table customer(id int,name varchar(20), phone varchar(8), address varchar(50));`{{execute}}
`create table orders(id int,customer_id int,product_id int,volume int,price int,sale_id int);`{{execute}}
 
Create company user.
Admin has all power in Company database.
create user 'admin'@'localhost' identified by 'password';
grant all privileges on Company.* to 'admin'@'localhost';
FLUSH PRIVILEGES;
 
Create user Manager which has all power exclude drop in Company database.
`create user 'manager'@'localhost' identified by 'password';`{{execute}}
`grant create,DELETE,INSERT,SELECT,UPDATE on Company.* to 'manager'@'localhost';`{{execute}}
`FLUSH PRIVILEGES;`{{execute}}

Create user Sale which can insert customer information, insert,update and select product information and oders.
`create user 'sale'@'localhost' identified by 'password';`{{execute}}
`grant INSERT on Company.customer to 'sale'@'localhost';`{{execute}}
`grant INSERT,UPDATE,SELECT on Company.product to 'sale'@'localhost';`{{execute}}
`grant INSERT, UPDATE, SELECT on Company.orders to 'sale'@'localhost';`{{execute}}
`FLUSH PRIVILEGES;`{{execute}}



Logout root
`quit`{{execute}}

Login as sale
`mysql -usale -p`{{execute}}
`password`{{execute}}

Show the available databases, you can see there is only 2 is available for user sale
`show databases;`{{execute}}

Use database Company
`use Company`{{execute}}
Show the available tables
`show tables;`{{execute}}

Select customer information (Should be denied because sale only can insert)
`select * from customer;`{{execute}}
Insert new customer
`insert into customer (id, name, phone, address) value (1,'ken',12345678,'address');`{{execute}}

Insert new order
`insert into orders(id,customer_id,product_id,volume,price,sale_id) value (1,1,1,5,100,1);`{{execute}}
Check the inserted order
`select * from orders;`{{execute}}
Update the order
`update orders set price=50 where id=1;`{{execute}}
Check
`select * from orders;`{{execute}}
Try to delete order (Should be denied because sale only allow Insert,Update and Select)
`delete from orders where id=1;`{{execute}}

Try the same case in product table.
Insert
`insert into product(id,name,price,description) value(1,'cake',100,'cheese');`{{execute}}
Select
`select * from product`{{execute}}
Delete
`delete from product where id=1;`{{execute}}

Try to drop all the tables and database.
`drop table product;`{{execute}}
`drop table customer;`{{execute}}
`drop table orders;`{{execute}}
`drop database Company;`{{execute}}

You can see sale cannot delete any data and drop anything due to sale are not granted any DELETE and DROP privileges.

Logout sale
`exit`{{execute}}



mysql -umanager -p
password

show databases;
use Company
show tables;
insert into customer (id, name, phone, address) value (2,'ben',87654321,'address2');
select * from customer;
select * from orders;
delete from orders where id=1;
select * from orders;
select * from product
delete from product where id=1;
drop table product;
drop table customer;
drop table orders;
drop database Company;





