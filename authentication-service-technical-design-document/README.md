# 🛠️ Authentication Service Technical Documentation

The authentication service, developed in Java using the Vert.x framework and backed by a PostgreSQL database, focuses on authenticating users with their Ethereum private keys via MetaMask. When a user attempts to access a protected resource without a valid JSON Web Token (JWT) or with an expired JWT, they are redirected to the login page to complete the authentication process.

Nginx serves as an API gateway to efficiently route requests to the appropriate services. To address architectural needs, Prometheus facilitates metrics collection. These metrics, along with their respective URL paths, are visualized using Grafana for comprehensive monitoring and alerting.

### Contents

[architecture-overview.md](authentication-service-technical-documentation/architecture-overview.md "mention")

[data-flow-diagram.md](authentication-service-technical-documentation/data-flow-diagram.md "mention")

[component-documentation.md](authentication-service-technical-documentation/component-documentation.md "mention")

[code-documentation.md](authentication-service-technical-documentation/code-documentation.md "mention")

[api-documentation](authentication-service-technical-documentation/api-documentation/ "mention")

[monitoring](authentication-service-technical-documentation/monitoring/ "mention")

[configuration-guide.md](authentication-service-technical-documentation/configuration-guide.md "mention")
