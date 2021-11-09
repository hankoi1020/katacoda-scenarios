Logout root

`quit`{{execute}}

Login as sale

`mysql -usale -p`{{execute}}

Enter password:

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

Check the updated order

`select * from orders;`{{execute}}

Try to delete order (Should be denied because sale only allow Insert,Update and Select)

`delete from orders where id=1;`{{execute}}

Try the same case in product table.

Insert new product

`insert into product(id,name,price,description) value(1,'cake',100,'cheese');`{{execute}}

Check the inserted product

`select * from product;`{{execute}}

Try to delete data in table product 

`delete from product where id=1;`{{execute}}

Try to drop all the tables and database.

`drop table product;`{{execute}}

`drop table customer;`{{execute}}

`drop table orders;`{{execute}}

`drop database Company;`{{execute}}

You can see sale cannot delete any data and drop anything due to sale are not granted any DELETE and DROP privileges.

Logout sale

`exit`{{execute}}
