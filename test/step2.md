## Create Company use case

Let create a simple company scenario in MySQL by create different user.

Open a new terminal and go in to the mysql container interactive bash terminal

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
