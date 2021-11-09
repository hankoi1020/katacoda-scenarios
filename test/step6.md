Login as admin

`mysql -uadmin -p`{{execute}}

`Enter password`{{execute}}

`password`

show available databases

`show databases;`{{execute}}

Select Company as current database

`use Company`{{execute}}

Try to DROP table and Company

`drop table customer;`{{execute}}

`drop table product;`{{execute}}

`drop table orders;`{{execute}}

`drop table test;`{{execute}}

`drop database Company;`{{execute}}

Since the password is default password, we should change the password to another

`alter user 'admin'@'localhost' identified by 'newpassword';`{{execute}}

But in the real life case, you should change the password to a complicated combination rather than this example
