- promotheus : monitoring system
  
*metrics are typically used to track, measure, and analyze various aspects of system performance, user activity,
and resource usage.

1/example System Metrics :
CPU Usage: Measures the percentage of CPU capacity being utilized over time.
Memory Usage: Tracks the amount of RAM being used by the application or system.

2/ Application Metrics
Response Time: The time taken by the application to respond to a request.
Error Rate: The number of failed requests or errors divided by the total number of requests.
Throughput: The number of requests processed per unit of time.

->promotheus stores metrics into time-series database

->promotheus give simple user interface where you can visualize,query,monitor the metrics

->data scraper that pulls metrics from http

- grafana : collect data from promotheus and visualize them with beautiful graphs, il allows us to make rule set
when there's change in metrics and will notify us over email/slack….

1- launch command to pull prometheus image from docker hub : docker pull prom/prometheus

2- launch this command : docker run -p 9090:9090 -v [path to your file prometheus.yml unders src/ressoucres] prom/prometheus

3/after second command you'll be able to use prometheus server : ![image](https://github.com/user-attachments/assets/d3ba929c-079b-4917-94fb-d1915d8fbc63)

4/ run command to run grafana image : docker run -p 3000:3000 grafana/grafana
![image](https://github.com/user-attachments/assets/bd0c23ef-546e-4ef1-b711-b2f7b929b8a7)

5/add data source and your prometheus url : ![image](https://github.com/user-attachments/assets/71d87280-974f-4c04-80a6-d1a94750b46d)

6/ add dashboard to data source prometheus and select metric : ![image](https://github.com/user-attachments/assets/d6ebfa0c-5b27-4cc5-9e8f-11b282d12fc7)



