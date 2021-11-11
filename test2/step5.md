## Go to the Grafana My2 dashboard 

https://[[HOST_SUBDOMAIN]]-3000-[[KATACODA_HOST]].environments.katacoda.com/

Click here in the home page

![圖片](https://user-images.githubusercontent.com/74434769/141320009-53c68c43-c89d-48ca-a378-253a79bf5085.png)

You may see the dashbroad are start showing data (It might take some time due to collector collect data every 10 minutes)

You may also select the time range and refresh time by clicking this on top right of the page

![圖片](https://user-images.githubusercontent.com/74434769/141208645-61490430-4708-4d00-b512-c256650fa6e2.png)

![圖片](https://user-images.githubusercontent.com/74434769/141320285-bd11ac8b-1114-46df-8b45-8b3def7e0b4a.png)


## Dashboard explainations

**Threads & Errors**

- **Threads_connected:** the currently open connections

- **Threads_running:** Currently open connections which are not sleeping

- **Slow_queries:** Number of queries that take a lot of time to execute

- **Aborted_connects:** Number of fail attempts to login the database

- **Aborted_clients:** Connetions aborted that client not close properly

**Space Usage**

- **Total size of the databases used**

**SQL Commands/sec**

- **Each type of SQL commands (Delete, Insert, Select, Update) executed in every second**

**Network**

- **Data sent or received through the network in every second**

**Heatmap**

