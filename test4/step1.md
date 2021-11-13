Docker-Compose can define and run multi-container by using a YAML file to configure the containers.

Get docker-compose.yml file by execute this command

wget https://raw.githubusercontent.com/kenpoon2000/katacoda-scenarios/main/test4/docker-compose.yml{{execute}}

Start up MySQL and Wordpress service by execute this command, it may take some time.

docker-compose up{{execute}}

After everything is started, go to Wordpress interface by click this link

https://[[HOST_SUBDOMAIN]]-20080-[[KATACODA_HOST]].environments.katacoda.com/


<pre class="file" data-target="clipboard">
version: '3.2' 
 
services: 
    mysql-server: 
        container_name: mysql 
        ports: 
            - "13306:3306"      
        environment: 
            MYSQL_ROOT_PASSWORD: secret 
            MYSQL_DATABASE: wordpress 
            MYSQL_USER: wordpress_user 
            MYSQL_PASSWORD: secret 
        image: mysql/mysql-server 

    wordpress: 
        image: wordpress:latest 
        container_name: wordpress 
        ports: 
            - "20080:80" 
        environment: 
            WORDPRESS_DB_HOST: mysql-server:3306 
            WORDPRESS_DB_USER: wordpress_user 
            WORDPRESS_DB_PASSWORD: secret 
        depends_on: 
            - mysql-server
                
</pre>
