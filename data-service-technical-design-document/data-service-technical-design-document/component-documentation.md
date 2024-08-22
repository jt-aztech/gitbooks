# 🗜️ Component Documentation

* REST API Component
* MongoDB Database Component
  * Collections
    * Subscription
    * Kline - open, high, low,close data points over time
* WebSocket manager
  * Manages the WebSocket clients and the amount of streams per WebSocket
* WebSocket client
  * Receive data streams
  * Handle disconnections or interruptions
* RabbitMQ Message Broker
  * New data points are sent for processing via a sequential queue.
* Monitoring Component
  * Metrics are exposed via the Prometheus Vert.x library and collected by Prometheus server.
  * Grafana dashboards designed to give an overview of system health, as well as indicate our service level indicators.
* Configuration Component
  * Configuration settings are passed and validated as environment variables.
  * Sample configuration includes settings for server port, JWT secret key, database connection, CORS settings, Prometheus metric name and, Binance connection properties.
