# 🗜️ Component Documentation

* REST API Component
  * see [api-documentation](api-documentation/ "mention")
* MetaMask Integration Component
  * Relies on the web interface using web3js for integration with MetaMask.
* PostgreSql Database Component
  * Table
    * account: Stores user account information including Ethereum wallet address, nonce, and creation timestamp.
* Web Interface Component
  * React application responsible for user interface.
  * Posts round trip time after each API call back to /metrics endpoint.
  * Expects code and route as tags for the round trip time values.
* Monitoring Component
  * Metrics are exposed via the Prometheus vertx library and collected by Prometheus server.
  * Grafana dashboards designed to give an overview of system health, as well as indicate our service level indicators.
* Configuration Component
  * Configuration settings are passed and validated as environment variables.
  * Sample configuration includes settings for server port, JWT secret key, database connection, CORS settings, frontend Prometheus metric name, and admin address.
