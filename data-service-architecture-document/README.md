# ℹ️ Data Service Architecture Document

### Overview

The data service is a micro service designed to gather data from various different data sources. This application follows an event-driven architecture emphasizing speed, scalability and adaptability. The service expose one endpoints in total supporting two HTTP methods, one to subscribe to a data stream and one to unsubscribe from a data stream. It publishes new data via a queue mechanism. It has no user interface.

### Contents

* [endpoints.md](data-service-architecture-document/endpoints.md "mention")
* [data-sources](data-service-architecture-document/data-sources/ "mention")
* [service-level-objectives-slos.md](data-service-architecture-document/service-level-objectives-slos.md "mention")
* [technology-stack.md](data-service-architecture-document/technology-stack.md "mention")
* [deployment-considerations.md](data-service-architecture-document/deployment-considerations.md "mention")
* [functional-requirement-diagram.md](data-service-architecture-document/functional-requirement-diagram.md "mention")
