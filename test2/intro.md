## Objective

This tutorial using MySQL and Grafana to create a database Auditing, Monitoring, Alerting example.

## Grafana https://grafana.com

Grafana is a open source application for analytics and monitoring database.

It support monitoring multiple database

It support plugins to help people develop 

Alert rule function can help system detect accident or attack

## 2MySQL Simple Dashboard create by meo https://grafana.com/grafana/dashboards/7991

2MySQL Simple Dashboard using collector to summarize databases information and show it on the preset dashboard.

It update every 10 minutes

User can customize the dashboard as well by using collected database information

## Why need to Audit,Monitor,Alert?

Once the server subject to Insider/External Attacks, the dashboard can alert the admin. It can help the security team to protect the system from attack as soon as possible.

In insider attack, it means an authorized access perform malicious action on the system. Some common malicious actions are:
•	Stealing data
•	Install malicious application/script
•	Damage the system

In external attack, it means someone perform malicious action from internet to damage the database. Some common malicious actions are:
•	DDOS
•	Brute force attack
•	SQL Injection
