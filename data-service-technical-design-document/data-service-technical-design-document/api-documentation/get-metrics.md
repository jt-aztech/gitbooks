# GET /metrics

Retrieve the metrics exposed by the service.

#### Example

#### Request

```
GET /metrics HTTP/1.1
Host: aztechcorp.io
```

#### Response (200 OK):

```
# HELP vertx_http_server_response_bytes_max Size of responses in bytes
# TYPE vertx_http_server_response_bytes_max gauge
vertx_http_server_response_bytes_max{code="400",method="PUT",route="/v1/subscribe",} 2.0
vertx_http_server_response_bytes_max{code="200",method="DELETE",route="/v1/subscribe",} 15.0
vertx_http_server_response_bytes_max{code="200",method="GET",route="/metrics",} 9730.0
vertx_http_server_response_bytes_max{code="200",method="PUT",route="/v1/subscribe",} 0.0
# HELP vertx_http_server_response_bytes Size of responses in bytes
# TYPE vertx_http_server_response_bytes summary
vertx_http_server_response_bytes_count{code="400",method="PUT",route="/v1/subscribe",} 1.0
vertx_http_server_response_bytes_sum{code="400",method="PUT",route="/v1/subscribe",} 2.0
vertx_http_server_response_bytes_count{code="200",method="DELETE",route="/v1/subscribe",} 1.0
vertx_http_server_response_bytes_sum{code="200",method="DELETE",route="/v1/subscribe",} 15.0
vertx_http_server_response_bytes_count{code="200",method="GET",route="/metrics",} 20.0
vertx_http_server_response_bytes_sum{code="200",method="GET",route="/metrics",} 166974.0
vertx_http_server_response_bytes_count{code="200",method="PUT",route="/v1/subscribe",} 1.0
vertx_http_server_response_bytes_sum{code="200",method="PUT",route="/v1/subscribe",} 824846.0
# HELP vertx_http_server_active_connections Number of opened connections to the server
# TYPE vertx_http_server_active_connections gauge
vertx_http_server_active_connections 3.0
# HELP vertx_http_server_request_bytes_max Size of requests in bytes
# TYPE vertx_http_server_request_bytes_max gauge
vertx_http_server_request_bytes_max{method="DELETE",} 67.0
vertx_http_server_request_bytes_max{method="GET",} 0.0
vertx_http_server_request_bytes_max{method="PUT",} 45.0
# HELP vertx_http_server_request_bytes Size of requests in bytes
# TYPE vertx_http_server_request_bytes summary
vertx_http_server_request_bytes_count{method="DELETE",} 1.0
vertx_http_server_request_bytes_sum{method="DELETE",} 67.0
vertx_http_server_request_bytes_count{method="GET",} 20.0
vertx_http_server_request_bytes_sum{method="GET",} 0.0
vertx_http_server_request_bytes_count{method="PUT",} 2.0
vertx_http_server_request_bytes_sum{method="PUT",} 112.0
# HELP vertx_eventbus_sent_total Number of messages sent (point-to-point)
# TYPE vertx_eventbus_sent_total counter
vertx_eventbus_sent_total{side="local",} 4.0
# HELP vertx_http_client_requests_total Number of requests sent
# TYPE vertx_http_client_requests_total counter
vertx_http_client_requests_total{method="GET",} 6.0
# HELP vertx_http_client_request_bytes_max Size of requests in bytes
# TYPE vertx_http_client_request_bytes_max gauge
vertx_http_client_request_bytes_max{method="GET",} 0.0
# HELP vertx_http_client_request_bytes Size of requests in bytes
# TYPE vertx_http_client_request_bytes summary
vertx_http_client_request_bytes_count{method="GET",} 6.0
vertx_http_client_request_bytes_sum{method="GET",} 0.0
# HELP vertx_http_client_bytes_read_total Number of bytes received from the remote host
# TYPE vertx_http_client_bytes_read_total counter
vertx_http_client_bytes_read_total 423886.0
# HELP vertx_eventbus_pending Number of messages not processed yet
# TYPE vertx_eventbus_pending gauge
vertx_eventbus_pending{side="local",} 0.0
# HELP vertx_http_server_requests_total Number of processed requests
# TYPE vertx_http_server_requests_total counter
vertx_http_server_requests_total{code="400",method="PUT",route="/v1/subscribe",} 1.0
vertx_http_server_requests_total{code="200",method="DELETE",route="/v1/subscribe",} 1.0
vertx_http_server_requests_total{code="200",method="GET",route="/metrics",} 20.0
vertx_http_server_requests_total{code="200",method="PUT",route="/v1/subscribe",} 1.0
# HELP vertx_eventbus_handlers Number of event bus handlers in use
# TYPE vertx_eventbus_handlers gauge
vertx_eventbus_handlers 1.0
# HELP vertx_http_client_response_time_seconds_max Response time
# TYPE vertx_http_client_response_time_seconds_max gauge
vertx_http_client_response_time_seconds_max{code="301",method="GET",} 0.0
vertx_http_client_response_time_seconds_max{code="200",method="GET",} 0.0
# HELP vertx_http_client_response_time_seconds Response time
# TYPE vertx_http_client_response_time_seconds summary
vertx_http_client_response_time_seconds_count{code="301",method="GET",} 3.0
vertx_http_client_response_time_seconds_sum{code="301",method="GET",} 0.267190392
vertx_http_client_response_time_seconds_count{code="200",method="GET",} 3.0
vertx_http_client_response_time_seconds_sum{code="200",method="GET",} 1.134080773
# HELP vertx_eventbus_delivered_total Number of messages delivered to handlers
# TYPE vertx_eventbus_delivered_total counter
vertx_eventbus_delivered_total{side="local",} 4.0
# HELP vertx_http_client_queue_pending Number of pending elements in queue
# TYPE vertx_http_client_queue_pending gauge
vertx_http_client_queue_pending 0.0
# HELP vertx_http_server_bytes_read_total Number of bytes received by the server
# TYPE vertx_http_server_bytes_read_total counter
vertx_http_server_bytes_read_total 179.0
# HELP vertx_http_client_responses_total Response count with codes
# TYPE vertx_http_client_responses_total counter
vertx_http_client_responses_total{code="301",method="GET",} 3.0
vertx_http_client_responses_total{code="200",method="GET",} 3.0
# HELP vertx_eventbus_received_total Number of messages received
# TYPE vertx_eventbus_received_total counter
vertx_eventbus_received_total{side="local",} 4.0
# HELP vertx_http_client_active_ws_connections Number of websockets currently opened
# TYPE vertx_http_client_active_ws_connections gauge
vertx_http_client_active_ws_connections 0.0
# HELP vertx_http_server_bytes_written_total Number of bytes sent by the server
# TYPE vertx_http_server_bytes_written_total counter
vertx_http_server_bytes_written_total 991837.0
# HELP vertx_http_client_response_bytes_max Size of responses in bytes
# TYPE vertx_http_client_response_bytes_max gauge
vertx_http_client_response_bytes_max{code="301",method="GET",} 0.0
vertx_http_client_response_bytes_max{code="200",method="GET",} 0.0
# HELP vertx_http_client_response_bytes Size of responses in bytes
# TYPE vertx_http_client_response_bytes summary
vertx_http_client_response_bytes_count{code="301",method="GET",} 3.0
vertx_http_client_response_bytes_sum{code="301",method="GET",} 501.0
vertx_http_client_response_bytes_count{code="200",method="GET",} 3.0
vertx_http_client_response_bytes_sum{code="200",method="GET",} 416138.0
# HELP vertx_http_client_active_connections Number of connections to the remote host currently opened
# TYPE vertx_http_client_active_connections gauge
vertx_http_client_active_connections 0.0
# HELP vertx_http_client_bytes_written_total Number of bytes sent to the remote host
# TYPE vertx_http_client_bytes_written_total counter
vertx_http_client_bytes_written_total 791.0
# HELP vertx_eventbus_processed_total Number of processed messages
# TYPE vertx_eventbus_processed_total counter
vertx_eventbus_processed_total{side="local",} 4.0
# HELP vertx_http_server_response_time_seconds_max Request processing time
# TYPE vertx_http_server_response_time_seconds_max gauge
vertx_http_server_response_time_seconds_max{code="400",method="PUT",route="/v1/subscribe",} 0.001361507
vertx_http_server_response_time_seconds_max{code="200",method="DELETE",route="/v1/subscribe",} 0.014954022
vertx_http_server_response_time_seconds_max{code="200",method="GET",route="/metrics",} 9.74613E-4
vertx_http_server_response_time_seconds_max{code="200",method="PUT",route="/v1/subscribe",} 0.0
# HELP vertx_http_server_response_time_seconds Request processing time
# TYPE vertx_http_server_response_time_seconds summary
vertx_http_server_response_time_seconds_count{code="400",method="PUT",route="/v1/subscribe",} 1.0
vertx_http_server_response_time_seconds_sum{code="400",method="PUT",route="/v1/subscribe",} 0.001361507
vertx_http_server_response_time_seconds_count{code="200",method="DELETE",route="/v1/subscribe",} 1.0
vertx_http_server_response_time_seconds_sum{code="200",method="DELETE",route="/v1/subscribe",} 0.014954022
vertx_http_server_response_time_seconds_count{code="200",method="GET",route="/metrics",} 20.0
vertx_http_server_response_time_seconds_sum{code="200",method="GET",route="/metrics",} 0.023099157
vertx_http_server_response_time_seconds_count{code="200",method="PUT",route="/v1/subscribe",} 1.0
vertx_http_server_response_time_seconds_sum{code="200",method="PUT",route="/v1/subscribe",} 2.400563667
# HELP vertx_http_client_queue_time_seconds_max Time spent in queue before being processed
# TYPE vertx_http_client_queue_time_seconds_max gauge
vertx_http_client_queue_time_seconds_max 0.0
# HELP vertx_http_client_queue_time_seconds Time spent in queue before being processed
# TYPE vertx_http_client_queue_time_seconds summary
vertx_http_client_queue_time_seconds_count 6.0
vertx_http_client_queue_time_seconds_sum 0.880499826
# HELP vertx_data_service_klines_total Kline counter for data service
# TYPE vertx_data_service_klines_total counter
vertx_data_service_klines_total{interval="1m",origin="websocket",source="Binance",symbol="xrpbtc",} 4.0
vertx_data_service_klines_total{interval="1m",origin="genesis",source="Binance",symbol="xrpbtc",} 2879.0
# HELP vertx_http_client_active_requests Number of requests waiting for a response
# TYPE vertx_http_client_active_requests gauge
vertx_http_client_active_requests{method="GET",} 0.0
# HELP vertx_http_server_active_requests Number of requests being processed
# TYPE vertx_http_server_active_requests gauge
vertx_http_server_active_requests{method="DELETE",} 0.0
vertx_http_server_active_requests{method="GET",} 1.0
vertx_http_server_active_requests{method="PUT",} 0.0
```
