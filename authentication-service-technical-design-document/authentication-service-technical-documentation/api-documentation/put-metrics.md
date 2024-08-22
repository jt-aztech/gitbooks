# PUT /metrics

Accepts metrics data and updates the metrics based on the provided information.

#### Request

* **Request Body** (JSON)
  * `code` (string, required): The code or identifier for the metric.
  * `route` (string, required): The route or URL path associated with the metric.
  * `rtt` (number, required): The round trip time (RTT) value for the metric in seconds.

#### Response

* **HTTP Status Code**
  * `200 OK` on successful update of metrics.
  * `400 Bad Request` if required fields are missing in the request or if the data types for fields are invalid.
  * `500 Internal Server Error` if there is a failure while updating the metrics.
* Response Body
  * "Metrics updated successfully" message on success.
  * Error message on failure.

#### Example

#### Request

```
PUT /api/as/metrics HTTP/1.1
Host: aztechcorp/io
Content-Type: application/json

{
  "code": "react_http_round_trip_time",
  "route": "/v1/account/:address/nonce",
  "rtt": 0.1
}
```

#### Response (200 OK)

```
{
  "message": "Metrics updated successfully"
}
```

#### Response (400 Bad Request)

```
{
  "error": "Missing required fields in the request"
}
```

#### Response (500 Internal Server Error)

```
{
  "error": "Failed to update metrics"
}
```
