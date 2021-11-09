Open a new terminal to grant privilege to granfana in database

Open the interactive bash

`docker exec -it mysql /bin/sh`{{execute}}

Login to MySQL as Root user

`mysql -uroot -p12345`{{execute}}

`grant all on *.* to 'grafana'@'%';`{{execute}}



After Grafana installed, get in Grafana interface by this link and do the basic setup

https://[[HOST_SUBDOMAIN]]-3000-[[KATACODA_HOST]].environments.katacoda.com/

Login by enter User name `admin` and password `admin`

You can change the password or skip it since it just a example

Next, go to `configuration` and select `Data sources`

![圖片](https://user-images.githubusercontent.com/74434769/141003725-cf556412-d50d-47ef-947d-e5eac6cb6df8.png)

Press `Add data source` and search MySQL and select it

![圖片](https://user-images.githubusercontent.com/74434769/141003949-9c8003f7-4282-460d-ad2b-9b394c9ba767.png)

Setting as this, password of grafana is 12345 (preset in YAML file)

![圖片](https://user-images.githubusercontent.com/74434769/141006629-3bb89f4f-26a2-4774-a428-4b14ea3f0a45.png)

After that, press Save&Test
