Let exit the container and download a sql file (wrote by meo:https://github.com/meob/my2Collector) in order to create the collector

`exit`{{execute}}

`exit`{{execute}}

`wget https://raw.githubusercontent.com/meob/my2Collector/master/my2_80.sql`{{execute}}

If you interested, you may view the my2_80.sql in this link"

https://raw.githubusercontent.com/meob/my2Collector/master/my2_80.sql

Copy the file to container and rename it as my2.sql

`docker cp my2_80.sql mysql:/my2.sql`{{execute}}

Go back to the container 

`docker -it mysql /bin/sh`{{execute}}

Execute the sql file as root user 

`mysql < my2.sql -uroot -p12345`{{execute}}

Login to mysql

`mysql -uroot -p12345`{{execute}}

Check the collector my2 created or not

`show databases;`{{execute}}

`use my2`{{execute}}

Show the tables in the collector

`show tables;`{{execute}}

You may see there are 2 tables name `current` and `status`

- **Current** is the current status of the database system, it contain a lot of status information of the system
- **Status** is storing information collected from Current with each collect time

You may peek the data in table status by this command, you could also change the limit number whatever you want to peek more data row

`select * from status limit 10;`{{execute}}

You may check the current status as well

`select * from current;`{{execute}}
