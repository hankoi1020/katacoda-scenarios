Docker-Compose can define and run multi-container by using a YAML file to configure the containers. 

First of all, we need to make a YAML file `docker-compose.yml`

You can get this file by execute this command
`wget https://raw.githubusercontent.com/kenpoon2000/katacoda-scenarios/main/test/docker-compose.yml`{{execute}}

After download the yml file, you can start up the applications by execute command:
`docker-compose up`{{execute}}


<pre class="file" data-target="clipboard">
version: '3.2' 
 
services: 
    mysql-server: 
        container_name: mysql 
        ports: 
            - "13306:3306"      
        environment: 
            MYSQL_ROOT_PASSWORD: secret 
        image: mysql/mysql-server                     
</pre>
