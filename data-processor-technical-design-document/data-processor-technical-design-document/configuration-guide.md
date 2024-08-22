# ⚙️ Configuration Guide

#### Environment variables

The following environment variables are used by the data processor service, they are read from a server side .yml file which should be specified by the service running the application:

```
SERVER_PORT: The port on which the microservice will listen for incoming HTTP requests. Default: 8888.
JWT_SECRET_KEY: The secret key used for JWT token generation and validation.
CORS_ALLOWED_ORIGIN: The allowed origin for Cross-Origin Resource Sharing (CORS).
DB_HOST: The hostname of the PostgreSQL database server.
DB_DATABASE: The name of the PostgreSQL database used by the microservice.
DB_USERNAME: The usernamve of the PostgreSQL database server.
DB_PASSWORD: The password of the PostgreSQL database used by the microservice.
RABBITMQ_HOST: The host where RabbitMQ is running.
RABBITMQ_PORT: The port on which rabbitMQ is listening.
RABBITMQ_USERNAME: The username to authenticate with RabbitMQ.
RABBITMQ_PASSWORD: The password to authenticate with RabbitMQ.
RABBITMQ_QUEUE_NAME: The queue to which to publish the messages.
FRONTEND_PROM_METRIC_NAME: The name of the metric used for frontend performance monitoring.
```
