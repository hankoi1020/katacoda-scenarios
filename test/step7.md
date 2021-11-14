## Show the user privileges

Logout

`exit`{{execute}}

Login as root user

`mysql -r -psecret`{{execute}}

You can check the privileges of each user by input these commands

`SHOW GRANTS FOR 'sale'@'localhost';`{{execute}}

`SHOW GRANTS FOR 'manager'@'localhost';`{{execute}}

`SHOW GRANTS FOR 'admin'@'localhost';`{{execute}}


## Revoke user privileges

Once you find a user is too much privileges, you can revoke it

For example:

Revoke INSERT previlege from sale on customer table:

`revoke insert on Company.customer from 'sale'@'localhost';`{{execute}}

Check whether revoke or not

`SHOW GRANTS FOR 'sale'@'localhost';`{{execute}}

Revoke ALL privilege from admin on Company

`revoke all privileges on Company.* from 'admin'@'localhost';`{{execute}}
