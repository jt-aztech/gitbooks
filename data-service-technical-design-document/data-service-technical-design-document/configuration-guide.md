# ⚙️ Configuration Guide

### Environment Variables

The following environment variables are used by the data service, they are read from a server side .yml file which should be specified by the service running the application:

```
SERVER_PORT: The port on which the microservice will listen for incoming HTTP requests. Default: 8888.
BINANCE_MAX_CONNECTIONS_PER_SOCKET: The maximum amount of streams allowed per WebSocket connection.
BINANCE_WS_HOST: The Binance WebSocket host.
BINANCE_WS_URI: The Binance WebSocket URI.
BINANCE_WS_PORT: The Binance WebSocket port.
BINANCE_GENESIS_KLINES_IN_DAYS: The amount of days worth of data to get on a new subscription.
KLINE_METRIC_NAME: The prometheus metric name for kline statistics.
DB_HOST: The hostname of the PostgreSQL database server.
DB_DATABASE: The name of the PostgreSQL database used by the microservice.
DB_USERNAME: The usernamve of the PostgreSQL database server.
DB_PASSWORD: The password of the PostgreSQL database used by the microservice.
JWT_SECRET_KEY: The secret key used for JWT token generation and validation.
CORS_ALLOWED_ORIGIN: The allowed origin for Cross-Origin Resource Sharing (CORS).
RABBITMQ_HOST: The host where RabbitMQ is running.
RABBITMQ_PORT: The port on which rabbitMQ is listening.
RABBITMQ_USERNAME: The username to authenticate with RabbitMQ.
RABBITMQ_PASSWORD: The password to authenticate with RabbitMQ.
RABBITMQ_QUEUE_NAME: The queue to which to publish the messages.
```
