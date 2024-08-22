# GET /metrics

Retrieve the metrics exposed by the service.

#### Example

#### Request

```
GET /metrics HTTP/1.1
Host: localhost:8888
```

#### Response (200 OK)

```
# HELP react_http_round_trip_time_seconds  
# TYPE react_http_round_trip_time_seconds summary
react_http_round_trip_time_seconds{code="200",route="/v1/account/:address/verifySignature",quantile="0.8",} 0.0
react_http_round_trip_time_seconds{code="200",route="/v1/account/:address/verifySignature",quantile="0.9",} 0.0
react_http_round_trip_time_seconds_count{code="200",route="/v1/account/:address/verifySignature",} 21.0
react_http_round_trip_time_seconds_sum{code="200",route="/v1/account/:address/verifySignature",} 0.34200000000000014
react_http_round_trip_time_seconds{code="200",route="/v1/account/:address/nonce",quantile="0.8",} 0.0
react_http_round_trip_time_seconds{code="200",route="/v1/account/:address/nonce",quantile="0.9",} 0.0
react_http_round_trip_time_seconds_count{code="200",route="/v1/account/:address/nonce",} 21.0
react_http_round_trip_time_seconds_sum{code="200",route="/v1/account/:address/nonce",} 0.34200000000000014
# HELP react_http_round_trip_time_seconds_max  
# TYPE react_http_round_trip_time_seconds_max gauge
react_http_round_trip_time_seconds_max{code="200",route="/v1/account/:address/verifySignature",} 0.0
react_http_round_trip_time_seconds_max{code="200",route="/v1/account/:address/nonce",} 0.0
# HELP vertx_http_server_requests_total Number of processed requests
# TYPE vertx_http_server_requests_total counter
vertx_http_server_requests_total{code="204",method="OPTIONS",route="",} 45.0
vertx_http_server_requests_total{code="200",method="GET",route="/v1/account/:address/nonce",} 45.0
vertx_http_server_requests_total{code="200",method="GET",route="/metrics",} 114.0
vertx_http_server_requests_total{code="400",method="GET",route="/v1/account/:address/nonce",} 7.0
vertx_http_server_requests_total{code="200",method="PUT",route="/metrics",} 42.0
vertx_http_server_requests_total{code="200",method="PUT",route="/v1/account/:address/verifySignature",} 41.0
vertx_http_server_requests_total{code="404",method="PUT",route="/v1/account/:address/verifySignature",} 10.0
# HELP vertx_pool_in_use Number of resources used
# TYPE vertx_pool_in_use gauge
vertx_pool_in_use{pool_type="worker",} 0.0
# HELP vertx_http_server_response_time_seconds_max Request processing time
# TYPE vertx_http_server_response_time_seconds_max gauge
vertx_http_server_response_time_seconds_max{code="204",method="OPTIONS",route="",} 0.0
vertx_http_server_response_time_seconds_max{code="200",method="GET",route="/v1/account/:address/nonce",} 0.009164785
vertx_http_server_response_time_seconds_max{code="200",method="GET",route="/metrics",} 0.0013853
vertx_http_server_response_time_seconds_max{code="400",method="GET",route="/v1/account/:address/nonce",} 0.0
vertx_http_server_response_time_seconds_max{code="200",method="PUT",route="/metrics",} 0.0
vertx_http_server_response_time_seconds_max{code="200",method="PUT",route="/v1/account/:address/verifySignature",} 0.0
vertx_http_server_response_time_seconds_max{code="404",method="PUT",route="/v1/account/:address/verifySignature",} 0.00217402
# HELP vertx_http_server_response_time_seconds Request processing time
# TYPE vertx_http_server_response_time_seconds summary
vertx_http_server_response_time_seconds{code="204",method="OPTIONS",route="",quantile="0.8",} 0.0
vertx_http_server_response_time_seconds{code="204",method="OPTIONS",route="",quantile="0.9",} 0.0
vertx_http_server_response_time_seconds_count{code="204",method="OPTIONS",route="",} 45.0
vertx_http_server_response_time_seconds_sum{code="204",method="OPTIONS",route="",} 0.010021784
vertx_http_server_response_time_seconds{code="200",method="GET",route="/v1/account/:address/nonce",quantile="0.8",} 0.0
vertx_http_server_response_time_seconds{code="200",method="GET",route="/v1/account/:address/nonce",quantile="0.9",} 0.0
vertx_http_server_response_time_seconds_count{code="200",method="GET",route="/v1/account/:address/nonce",} 45.0
vertx_http_server_response_time_seconds_sum{code="200",method="GET",route="/v1/account/:address/nonce",} 0.417807889
vertx_http_server_response_time_seconds{code="200",method="GET",route="/metrics",quantile="0.8",} 6.88128E-4
vertx_http_server_response_time_seconds{code="200",method="GET",route="/metrics",quantile="0.9",} 6.88128E-4
vertx_http_server_response_time_seconds_count{code="200",method="GET",route="/metrics",} 114.0
vertx_http_server_response_time_seconds_sum{code="200",method="GET",route="/metrics",} 0.141260529
vertx_http_server_response_time_seconds{code="400",method="GET",route="/v1/account/:address/nonce",quantile="0.8",} 0.0
vertx_http_server_response_time_seconds{code="400",method="GET",route="/v1/account/:address/nonce",quantile="0.9",} 0.0
vertx_http_server_response_time_seconds_count{code="400",method="GET",route="/v1/account/:address/nonce",} 7.0
vertx_http_server_response_time_seconds_sum{code="400",method="GET",route="/v1/account/:address/nonce",} 0.004418919
vertx_http_server_response_time_seconds{code="200",method="PUT",route="/metrics",quantile="0.8",} 0.0
vertx_http_server_response_time_seconds{code="200",method="PUT",route="/metrics",quantile="0.9",} 0.0
vertx_http_server_response_time_seconds_count{code="200",method="PUT",route="/metrics",} 42.0
vertx_http_server_response_time_seconds_sum{code="200",method="PUT",route="/metrics",} 0.042716564
vertx_http_server_response_time_seconds{code="200",method="PUT",route="/v1/account/:address/verifySignature",quantile="0.8",} 0.0
vertx_http_server_response_time_seconds{code="200",method="PUT",route="/v1/account/:address/verifySignature",quantile="0.9",} 0.0
vertx_http_server_response_time_seconds_count{code="200",method="PUT",route="/v1/account/:address/verifySignature",} 41.0
vertx_http_server_response_time_seconds_sum{code="200",method="PUT",route="/v1/account/:address/verifySignature",} 0.27521765
vertx_http_server_response_time_seconds{code="404",method="PUT",route="/v1/account/:address/verifySignature",quantile="0.8",} 0.0
vertx_http_server_response_time_seconds{code="404",method="PUT",route="/v1/account/:address/verifySignature",quantile="0.9",} 0.0
vertx_http_server_response_time_seconds_count{code="404",method="PUT",route="/v1/account/:address/verifySignature",} 10.0
vertx_http_server_response_time_seconds_sum{code="404",method="PUT",route="/v1/account/:address/verifySignature",} 0.049844191
# HELP vertx_pool_completed_total Number of elements done with the resource
# TYPE vertx_pool_completed_total counter
vertx_pool_completed_total{pool_type="worker",} 1.0
# HELP vertx_pool_ratio Pool usage ratio, only present if maximum pool size could be determined
# TYPE vertx_pool_ratio gauge
vertx_pool_ratio{pool_type="worker",} 0.0
# HELP vertx_http_server_response_bytes_max Size of responses in bytes
# TYPE vertx_http_server_response_bytes_max gauge
vertx_http_server_response_bytes_max{code="204",method="OPTIONS",route="",} 0.0
vertx_http_server_response_bytes_max{code="200",method="GET",route="/v1/account/:address/nonce",} 51.0
vertx_http_server_response_bytes_max{code="200",method="GET",route="/metrics",} 14449.0
vertx_http_server_response_bytes_max{code="400",method="GET",route="/v1/account/:address/nonce",} 0.0
vertx_http_server_response_bytes_max{code="200",method="PUT",route="/metrics",} 0.0
vertx_http_server_response_bytes_max{code="200",method="PUT",route="/v1/account/:address/verifySignature",} 0.0
vertx_http_server_response_bytes_max{code="404",method="PUT",route="/v1/account/:address/verifySignature",} 145.0
# HELP vertx_http_server_response_bytes Size of responses in bytes
# TYPE vertx_http_server_response_bytes summary
vertx_http_server_response_bytes{code="204",method="OPTIONS",route="",quantile="0.8",} 0.0
vertx_http_server_response_bytes{code="204",method="OPTIONS",route="",quantile="0.9",} 0.0
vertx_http_server_response_bytes_count{code="204",method="OPTIONS",route="",} 45.0
vertx_http_server_response_bytes_sum{code="204",method="OPTIONS",route="",} 0.0
vertx_http_server_response_bytes{code="200",method="GET",route="/v1/account/:address/nonce",quantile="0.8",} 0.0
vertx_http_server_response_bytes{code="200",method="GET",route="/v1/account/:address/nonce",quantile="0.9",} 0.0
vertx_http_server_response_bytes_count{code="200",method="GET",route="/v1/account/:address/nonce",} 45.0
vertx_http_server_response_bytes_sum{code="200",method="GET",route="/v1/account/:address/nonce",} 2283.0
vertx_http_server_response_bytes{code="200",method="GET",route="/metrics",quantile="0.8",} 14336.0
vertx_http_server_response_bytes{code="200",method="GET",route="/metrics",quantile="0.9",} 14336.0
vertx_http_server_response_bytes_count{code="200",method="GET",route="/metrics",} 114.0
vertx_http_server_response_bytes_sum{code="200",method="GET",route="/metrics",} 1544965.0
vertx_http_server_response_bytes{code="400",method="GET",route="/v1/account/:address/nonce",quantile="0.8",} 0.0
vertx_http_server_response_bytes{code="400",method="GET",route="/v1/account/:address/nonce",quantile="0.9",} 0.0
vertx_http_server_response_bytes_count{code="400",method="GET",route="/v1/account/:address/nonce",} 7.0
vertx_http_server_response_bytes_sum{code="400",method="GET",route="/v1/account/:address/nonce",} 777.0
vertx_http_server_response_bytes{code="200",method="PUT",route="/metrics",quantile="0.8",} 0.0
vertx_http_server_response_bytes{code="200",method="PUT",route="/metrics",quantile="0.9",} 0.0
vertx_http_server_response_bytes_count{code="200",method="PUT",route="/metrics",} 42.0
vertx_http_server_response_bytes_sum{code="200",method="PUT",route="/metrics",} 1176.0
vertx_http_server_response_bytes{code="200",method="PUT",route="/v1/account/:address/verifySignature",quantile="0.8",} 0.0
vertx_http_server_response_bytes{code="200",method="PUT",route="/v1/account/:address/verifySignature",quantile="0.9",} 0.0
vertx_http_server_response_bytes_count{code="200",method="PUT",route="/v1/account/:address/verifySignature",} 41.0
vertx_http_server_response_bytes_sum{code="200",method="PUT",route="/v1/account/:address/verifySignature",} 15498.0
vertx_http_server_response_bytes{code="404",method="PUT",route="/v1/account/:address/verifySignature",quantile="0.8",} 0.0
vertx_http_server_response_bytes{code="404",method="PUT",route="/v1/account/:address/verifySignature",quantile="0.9",} 0.0
vertx_http_server_response_bytes_count{code="404",method="PUT",route="/v1/account/:address/verifySignature",} 10.0
vertx_http_server_response_bytes_sum{code="404",method="PUT",route="/v1/account/:address/verifySignature",} 1428.0
# HELP vertx_http_server_active_requests Number of requests being processed
# TYPE vertx_http_server_active_requests gauge
vertx_http_server_active_requests{method="GET",} 1.0
vertx_http_server_active_requests{method="OPTIONS",} 0.0
vertx_http_server_active_requests{method="PUT",} 0.0
# HELP vertx_pool_queue_pending Number of pending elements in queue
# TYPE vertx_pool_queue_pending gauge
vertx_pool_queue_pending{pool_type="worker",} 0.0
# HELP vertx_pool_usage_seconds Time using a resource
# TYPE vertx_pool_usage_seconds summary
vertx_pool_usage_seconds{pool_type="worker",quantile="0.8",} 0.0
vertx_pool_usage_seconds{pool_type="worker",quantile="0.9",} 0.0
vertx_pool_usage_seconds_count{pool_type="worker",} 1.0
vertx_pool_usage_seconds_sum{pool_type="worker",} 0.221972422
# HELP vertx_pool_usage_seconds_max Time using a resource
# TYPE vertx_pool_usage_seconds_max gauge
vertx_pool_usage_seconds_max{pool_type="worker",} 0.0
# HELP vertx_sql_processing_pending Number of elements being processed
# TYPE vertx_sql_processing_pending gauge
vertx_sql_processing_pending 0.0
# HELP vertx_sql_processing_time_seconds Processing time, from request start to response end
# TYPE vertx_sql_processing_time_seconds summary
vertx_sql_processing_time_seconds{quantile="0.8",} 0.0
vertx_sql_processing_time_seconds{quantile="0.9",} 0.0
vertx_sql_processing_time_seconds_count 141.0
vertx_sql_processing_time_seconds_sum 0.340885833
# HELP vertx_sql_processing_time_seconds_max Processing time, from request start to response end
# TYPE vertx_sql_processing_time_seconds_max gauge
vertx_sql_processing_time_seconds_max 0.006968054
# HELP vertx_http_server_active_connections Number of opened connections to the server
# TYPE vertx_http_server_active_connections gauge
vertx_http_server_active_connections 3.0
# HELP vertx_http_server_request_bytes_max Size of requests in bytes
# TYPE vertx_http_server_request_bytes_max gauge
vertx_http_server_request_bytes_max{method="GET",} 0.0
vertx_http_server_request_bytes_max{method="OPTIONS",} 0.0
vertx_http_server_request_bytes_max{method="PUT",} 154.0
# HELP vertx_http_server_request_bytes Size of requests in bytes
# TYPE vertx_http_server_request_bytes summary
vertx_http_server_request_bytes{method="GET",quantile="0.8",} 0.0
vertx_http_server_request_bytes{method="GET",quantile="0.9",} 0.0
vertx_http_server_request_bytes_count{method="GET",} 166.0
vertx_http_server_request_bytes_sum{method="GET",} 0.0
vertx_http_server_request_bytes{method="OPTIONS",quantile="0.8",} 0.0
vertx_http_server_request_bytes{method="OPTIONS",quantile="0.9",} 0.0
vertx_http_server_request_bytes_count{method="OPTIONS",} 45.0
vertx_http_server_request_bytes_sum{method="OPTIONS",} 0.0
vertx_http_server_request_bytes{method="PUT",quantile="0.8",} 0.0
vertx_http_server_request_bytes{method="PUT",quantile="0.9",} 0.0
vertx_http_server_request_bytes_count{method="PUT",} 93.0
vertx_http_server_request_bytes_sum{method="PUT",} 10497.0
# HELP vertx_http_server_bytes_read_total Number of bytes received by the server
# TYPE vertx_http_server_bytes_read_total counter
vertx_http_server_bytes_read_total 10497.0
# HELP vertx_http_server_bytes_written_total Number of bytes sent by the server
# TYPE vertx_http_server_bytes_written_total counter
vertx_http_server_bytes_written_total 1566127.0
# HELP vertx_pool_queue_time_seconds_max Time spent in queue before being processed
# TYPE vertx_pool_queue_time_seconds_max gauge
vertx_pool_queue_time_seconds_max{pool_type="worker",} 0.0
# HELP vertx_pool_queue_time_seconds Time spent in queue before being processed
# TYPE vertx_pool_queue_time_seconds summary
vertx_pool_queue_time_seconds{pool_type="worker",quantile="0.8",} 0.0
vertx_pool_queue_time_seconds{pool_type="worker",quantile="0.9",} 0.0
vertx_pool_queue_time_seconds_count{pool_type="worker",} 1.0
vertx_pool_queue_time_seconds_sum{pool_type="worker",} 0.01261245
```
