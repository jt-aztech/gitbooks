# 🗜️ Component Documentation

* REST API Component
  * See [api-documentation](api-documentation/ "mention")
* MongoDB Database Component
  * Collections
    * Strategy
    * Kline - open, high, low,close data points over time
* RabbitMQ Message Broker New data points are picked up for processing via a sequential queue ensuring order is maintained.&#x20;
* Strategy engine is used to run any strategy along with any algorithms associated with that strategy.
* Processed strategy results are stored in a cache to ensure they can be retrieved quickly.
* Monitoring Component Metrics are exposed via the Prometheus Vert.x library and collected by Prometheus server.&#x20;
* Grafana dashboards designed to give an overview of system health, as well as indicate our service level indicators.&#x20;
* Configuration Component Configuration settings are passed and validated as environment variables.
