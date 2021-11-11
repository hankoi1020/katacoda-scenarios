We use Docker-Compose to create multiple container (MySQL, Grafana) at the same time 

We install MySQL and Grafana by Docker using YAML file `docker-compose.yml`

You can get this file by execute this command

`wget https://raw.githubusercontent.com/kenpoon2000/katacoda-scenarios/main/test2/docker-compose.yml`{{execute}}

After download the yml file, you can start up the applications by execute command:

`docker-compose up`{{execute}}


YAML code:

<pre class="file" data-target="clipboard">
version: '3.2' 

services: 
    db1: 
        container_name: mysql    
        ports:
            - "33060:3306"
        environment: 
            MYSQL_ROOT_PASSWORD: 12345   #Root user password
            MYSQL_USER: grafana
            MYSQL_PASSWORD: 12345        #grafana user password
        image: mysql/mysql-server  
        
    grafana:
        image: grafana/grafana:latest 
        ports: 
            - "3000:3000"     
</pre>
