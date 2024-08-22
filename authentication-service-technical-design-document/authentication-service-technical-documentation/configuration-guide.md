# ⚙️ Configuration Guide

### Environment Variables

The following environment variables are used by the Authentication Service, they are read from a server side .yml file which should be specified by the service running the application:

```
SERVER_PORT: The port on which the microservice will listen for incoming HTTP requests. Default: 8888.
JWT_SECRET_KEY: The secret key used for JWT token generation and validation.
DB_HOST: The hostname of the PostgreSQL database server.
DB_PORT: The port number of the PostgreSQL database server. Default: 5432.
DB_DATABASE: The name of the PostgreSQL database used by the microservice.
DB_USER: The username for authenticating with the PostgreSQL database.
DB_PASSWORD: The password for authenticating with the PostgreSQL database.
SIGN_MESSAGE: The message used for signing when interacting with Ethereum wallets.
CORS_ALLOWED_ORIGIN: The allowed origin for Cross-Origin Resource Sharing (CORS).
FRONTEND_PROM_METRIC_NAME: The name of the metric used for frontend performance monitoring.
ADMIN_ADDRESS: The address associated with the admin account.
```
