# 🏫 Architecture Overview

The architecture of the data service is centered around the Vert.x framework, chosen for its asynchronous and non-blocking event-driven model, facilitating high concurrency and scalability. This lightweight runtime provides an efficient platform for building reactive applications.

#### Key Components:

1. **Vert.x Framework**:
   * **Asynchronous and Non-blocking**: Enables high concurrency and efficient resource utilization.
   * **Event-driven Model**: Supports building scalable and responsive applications.
2. **Database**:
   * **MongoDB**: Selected for its schema-less storage capabilities, allowing flexible and dynamic data management without predefined schemas.
3. **Data Collection and Delivery**:
   * Upon startup, the data service loads the current subscriptions for which it is collecting data. It checks for missing data points and collects those to ensure data completeness after a system outage. Any new data points are sent to the RabbitMQ message broker for efficient and reliable delivery to other services.
4. **Security**:
   * **Vert.x JWT Auth Library**: Ensures secure communication by allowing only authorized entities to interact with the service.
5. **Monitoring and Performance**:
   * **Prometheus**: Facilitates metrics collection for system health and performance monitoring.
   * **Grafana**: Visualizes these metrics through comprehensive dashboards, providing real-time insights and alerts.
