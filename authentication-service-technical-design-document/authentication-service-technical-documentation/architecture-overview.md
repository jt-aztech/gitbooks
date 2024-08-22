# 🏫 Architecture Overview

The architecture of the authentication service is centered around the Vert.x framework, chosen for its asynchronous and non-blocking event-driven model, which facilitates high concurrency and scalability. This lightweight runtime provides an efficient platform for building reactive applications.

#### Key Components:

1. **Vert.x Framework**:
   * **Asynchronous and Non-blocking**: Enables high concurrency and efficient resource utilization.
   * **Event-driven Model**: Supports building scalable and responsive applications.
2. **Web Interface**:
   * **React**: Utilized for its simplicity and effectiveness in constructing user interfaces. The component-based structure of React streamlines development and maintenance processes.
3. **Database**:
   * **PostgreSQL**: Selected for its reliability and robustness in managing structured data.
4. **API Gateway**:
   * **Nginx**: Used to route requests, providing load balancing, reverse proxying, and security features such as rate limiting and IP whitelisting. Nginx ensures efficient and secure communication between the client and backend services.
5. **Dynamic Scaling**:
   * Upon startup, the authentication service dynamically adjusts its scaling strategy based on server hardware resources, creating REST API services proportional to half the number of available CPU cores. This adaptive approach optimizes resource utilization and ensures effective request handling. As a microservice, it can also scale horizontally.
6. **Security**:
   * **MetaMask**: Utilized as a self-custodial wallet for user authentication.
   * **Vert.x JWT Auth Library**: Ensures secure interactions with Ethereum wallets and the application.
7. **Monitoring and Performance**:
   * **Prometheus**: Facilitates metrics collection for system health and performance monitoring.
   * **Grafana**: Visualizes these metrics through comprehensive dashboards, providing real-time insights and alerts.
