Grafana also support alert function for dashbroad, we gonna use `Threads and Error` to do an example

We gonna make an alert that when the total error occurred more than 50 times within 10 minutes

Go to the 2Mysql simple dashboard page

Click `Threads and Error` and select Edit

![圖片](https://user-images.githubusercontent.com/74434769/141324368-190dab27-2805-4d61-9c33-393c8863f607.png)

You may see there are 2 querys for this dashboard (A and B)

![圖片](https://user-images.githubusercontent.com/74434769/141324557-f667bf53-692d-44af-b1dd-f00e80984144.png)

Query A is select the data about the threads connected/running

Query B is select the Slow Query, Aborted Connects and Aborted Clients

Now go to alert to apply alert rule to query B like this

Every 12 minutes evalute the condition

The condition is sum of the error occurred in the pass 12 minutes more than 50 times

![圖片](https://user-images.githubusercontent.com/74434769/141325948-303a5e48-4b05-4554-9c61-ceaa8e039391.png)


![圖片](https://user-images.githubusercontent.com/74434769/141332317-a8f99e95-5a4f-4ad8-b22c-9d469a8b3090.png)

Once you finish the rule setting, click `Apply` on the top right and save the dashboard

This is the sample of the alert, there will have a vertical red line on the graph 

![圖片](https://user-images.githubusercontent.com/74434769/141332097-95b6d93e-2443-4063-bd58-73db31634cd0.png)

![圖片](https://user-images.githubusercontent.com/74434769/141332134-fd8a727a-4f81-47c2-8550-0915bf41fb42.png)

In no alert case, the will have a vertical green line and say OK

![圖片](https://user-images.githubusercontent.com/74434769/141349169-bf00238d-21fe-47fa-8d20-f79ad0cf56ee.png)

![圖片](https://user-images.githubusercontent.com/74434769/141349232-44018b9d-f3e0-4fb4-98cd-ce0fa77d2035.png)


