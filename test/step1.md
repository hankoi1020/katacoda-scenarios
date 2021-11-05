Docker-Compose can define and run multi-container by using a YAML file to configure the containers. 

First of all, we need to make a YAML file "docker-compose.yml"

You can get this file by execute this command
"git clone https://github.com/kenpoon2000/katacoda-scenarios/blob/750b58cec34a77f37522dbb88ef28bc649ca1e1a/test/docker-compose.yml" {{execute}}

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
