Let create a simple company scenario in MySQL by create different user.

Open the mysql container interactive bash terminal

 `docker exec -it mysql /bin/sh`{{execute}}
 
Login into MySql as root

 `mysql -uroot -p`{{execute}}
 
 `secret`{{execute}}
 
Create database Company with tables.

`create database Company;`{{execute}}

`use Company;`{{execute}}

Create table Product, Customer and Orders

`CREATE TABLE product(id int, name VARCHAR(20), price int, description varchar(50));`{{execute}}

`create table customer(id int,name varchar(20), phone varchar(8), address varchar(50));`{{execute}}

`create table orders(id int,customer_id int,product_id int,volume int,price int,sale_id int);`{{execute}}




Login as Manager

`mysql -umanager -p`{{execute}}

Enter password

`password`{{execute}}

Show the available databases

`show databases;`{{execute}}

Select Company database

`use Company`{{execute}}

Show available tables

`show tables;`{{execute}}

Insert new customer

`insert into customer (id, name, phone, address) value (2,'ben',87654321,'address2');`{{execute}}

Try to check the data in customer

`select * from customer;`{{execute}}

View the data in orders

`select * from orders;`{{execute}}

Try to delete orders 1 sale just created

`delete from orders where id=1;`{{execute}}

Check the order whether deleted or not

`select * from orders;`{{execute}}

View the data in product

`select * from product`{{execute}}

Try to delete product id 1

`delete from product where id=1;`{{execute}}

Check whether deleted or not

`select * from product`{{execute}}

Try to DROP the tables and databases:

`drop table product;`{{execute}}

`drop table customer;`{{execute}}

`drop table orders;`{{execute}}

`drop database Company;`{{execute}}

Logout Manager

`quit`{{execute}}





