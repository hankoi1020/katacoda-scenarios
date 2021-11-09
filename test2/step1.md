We use Docker-Compose to create multiple container (MySQL, Grafana) at the sam time 

We install MySQL and Grafana by Docker using YAML file `docker-compose.yml`

You can get this file by execute this command

`wget https://raw.githubusercontent.com/kenpoon2000/katacoda-scenarios/main/test2/docker-compose.yml`{{execute}}

After download the yml file, you can start up the applications by execute command:

`docker-compose up`{{execute}}


YAML code:

<pre class="file" data-target="clipboard">
version: '3.9' 

services: 
    db1: 
        ports:
            - "33060:3306"
        environment: 
            MYSQL_ROOT_PASSWORD: 12345 #Password for root user in MySQL
            MYSQL_DATABASE: wordpress   #Create a database for Wordpress 
            MYSQL_USER: wordpress  #Create a Wordpress user in MySQL
            MYSQL_PASSWORD: 12345      #Password for wordpress_user            
        image: mysql/mysql-server       
            
    grafana:
        image: grafana/grafana:latest 
        ports: 
            - "3000:3000"        
</pre>
