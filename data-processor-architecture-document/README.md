# ✒️ Data Processor Architecture Document

### Overview

The data processor service is designed to handle incoming data from a queue by storing it, identifying applicable strategies for incoming data points, executing all associated algorithms for the applicable strategies, normalizing the resulting data, and updating the cache for each strategy as new data is coming in as well as when algorithms are executed. This updated cache can then be queried through the web component to display the results of the strategies in real-time.

### Contents

* [api-endpoints.md](data-processor-architecture-document/api-endpoints.md "mention")
* [algorithms](data-processor-architecture-document/algorithms/ "mention")
* [service-level-objectives-slos.md](data-processor-architecture-document/service-level-objectives-slos.md "mention")
* [technology-stack.md](data-processor-architecture-document/technology-stack.md "mention")
* [deployment-considerations.md](data-processor-architecture-document/deployment-considerations.md "mention")
* [functional-requirement-diagram.md](data-processor-architecture-document/functional-requirement-diagram.md "mention")
