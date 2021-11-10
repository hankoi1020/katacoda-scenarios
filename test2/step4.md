let exit the container and download a sql file (wrote by meo) in order to create the collector

exit

wget https://raw.githubusercontent.com/meob/my2Collector/master/my2_80.sql

copy the file to container and rename it as my2.sql

docker cp my2_80.sql mysql:/my2.sql

go back to the container 

docker -it mysql /bin/sh

execute the sql file 

mysql < my2.sql -uroot -p12345

login to mysql

mysql -uroot -p12345

let see the collector my2 created or not

show databases;

use my2

show tables;

select * from status limit 10;

