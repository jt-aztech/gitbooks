# GET /metrics

GET /metrics retrieves the prometheus metrics exposed by the service

#### Example

#### Request

```
GET /metrics HTTP/1.1
Host: localhost:8890
```

#### Response (200 OK

```
# HELP vertx_http_server_bytes_written_total Number of bytes sent by the server
# TYPE vertx_http_server_bytes_written_total counter
vertx_http_server_bytes_written_total 4.3242832E7
# HELP vertx_http_server_bytes_read_total Number of bytes received by the server
# TYPE vertx_http_server_bytes_read_total counter
vertx_http_server_bytes_read_total 1557.0
# HELP react_http_round_trip_time_seconds  
# TYPE react_http_round_trip_time_seconds summary
react_http_round_trip_time_seconds{code="404",route="/v1/strategy/:id",quantile="0.8",} 0.0069580078125
react_http_round_trip_time_seconds{code="404",route="/v1/strategy/:id",quantile="0.9",} 0.0069580078125
react_http_round_trip_time_seconds_count{code="404",route="/v1/strategy/:id",} 5.0
react_http_round_trip_time_seconds_sum{code="404",route="/v1/strategy/:id",} 0.028999999999999998
react_http_round_trip_time_seconds{code="200",route="/v1/strategy/:id",quantile="0.8",} 0.09375
react_http_round_trip_time_seconds{code="200",route="/v1/strategy/:id",quantile="0.9",} 0.09375
react_http_round_trip_time_seconds_count{code="200",route="/v1/strategy/:id",} 9.0
react_http_round_trip_time_seconds_sum{code="200",route="/v1/strategy/:id",} 0.929
react_http_round_trip_time_seconds{code="200",route="/v1/strategy",quantile="0.8",} 0.105224609375
react_http_round_trip_time_seconds{code="200",route="/v1/strategy",quantile="0.9",} 0.105224609375
react_http_round_trip_time_seconds_count{code="200",route="/v1/strategy",} 14.0
react_http_round_trip_time_seconds_sum{code="200",route="/v1/strategy",} 0.71
react_http_round_trip_time_seconds{code="500",route="/v1/strategy",quantile="0.8",} 0.0
react_http_round_trip_time_seconds{code="500",route="/v1/strategy",quantile="0.9",} 0.0
react_http_round_trip_time_seconds_count{code="500",route="/v1/strategy",} 4.0
react_http_round_trip_time_seconds_sum{code="500",route="/v1/strategy",} 0.033
# HELP react_http_round_trip_time_seconds_max  
# TYPE react_http_round_trip_time_seconds_max gauge
react_http_round_trip_time_seconds_max{code="404",route="/v1/strategy/:id",} 0.007
react_http_round_trip_time_seconds_max{code="200",route="/v1/strategy/:id",} 0.096
react_http_round_trip_time_seconds_max{code="200",route="/v1/strategy",} 0.102
react_http_round_trip_time_seconds_max{code="500",route="/v1/strategy",} 0.0
# HELP strategy_processing_time_milliseconds  
# TYPE strategy_processing_time_milliseconds summary
strategy_processing_time_milliseconds{interval="1h",name="Bitcoin TABI",source="binance",strategyId="66839abe9b75c606469eaa9d",ticker="btcusdt",quantile="0.8",} 0.0
strategy_processing_time_milliseconds{interval="1h",name="Bitcoin TABI",source="binance",strategyId="66839abe9b75c606469eaa9d",ticker="btcusdt",quantile="0.9",} 0.0
strategy_processing_time_milliseconds_count{interval="1h",name="Bitcoin TABI",source="binance",strategyId="66839abe9b75c606469eaa9d",ticker="btcusdt",} 1.0
strategy_processing_time_milliseconds_sum{interval="1h",name="Bitcoin TABI",source="binance",strategyId="66839abe9b75c606469eaa9d",ticker="btcusdt",} 288.0
strategy_processing_time_milliseconds{interval="1m",name="Bitcoin TABI",source="binance",strategyId="6685ee2bba1a0c3135e6754e",ticker="btcusdt",quantile="0.8",} 1088.0
strategy_processing_time_milliseconds{interval="1m",name="Bitcoin TABI",source="binance",strategyId="6685ee2bba1a0c3135e6754e",ticker="btcusdt",quantile="0.9",} 1088.0
strategy_processing_time_milliseconds_count{interval="1m",name="Bitcoin TABI",source="binance",strategyId="6685ee2bba1a0c3135e6754e",ticker="btcusdt",} 85.0
strategy_processing_time_milliseconds_sum{interval="1m",name="Bitcoin TABI",source="binance",strategyId="6685ee2bba1a0c3135e6754e",ticker="btcusdt",} 96794.0
# HELP strategy_processing_time_milliseconds_max  
# TYPE strategy_processing_time_milliseconds_max gauge
strategy_processing_time_milliseconds_max{interval="1h",name="Bitcoin TABI",source="binance",strategyId="66839abe9b75c606469eaa9d",ticker="btcusdt",} 0.0
strategy_processing_time_milliseconds_max{interval="1m",name="Bitcoin TABI",source="binance",strategyId="6685ee2bba1a0c3135e6754e",ticker="btcusdt",} 1181.0
# HELP vertx_pool_queue_pending Number of pending elements in queue
# TYPE vertx_pool_queue_pending gauge
vertx_pool_queue_pending{pool_type="worker",} 0.0
# HELP vertx_http_server_request_bytes_max Size of requests in bytes
# TYPE vertx_http_server_request_bytes_max gauge
vertx_http_server_request_bytes_max{method="GET",} 0.0
vertx_http_server_request_bytes_max{method="OPTIONS",} 0.0
vertx_http_server_request_bytes_max{method="PUT",} 51.0
# HELP vertx_http_server_request_bytes Size of requests in bytes
# TYPE vertx_http_server_request_bytes summary
vertx_http_server_request_bytes{method="GET",quantile="0.8",} 0.0
vertx_http_server_request_bytes{method="GET",quantile="0.9",} 0.0
vertx_http_server_request_bytes_count{method="GET",} 242.0
vertx_http_server_request_bytes_sum{method="GET",} 0.0
vertx_http_server_request_bytes{method="OPTIONS",quantile="0.8",} 0.0
vertx_http_server_request_bytes{method="OPTIONS",quantile="0.9",} 0.0
vertx_http_server_request_bytes_count{method="OPTIONS",} 39.0
vertx_http_server_request_bytes_sum{method="OPTIONS",} 0.0
vertx_http_server_request_bytes{method="PUT",quantile="0.8",} 50.0
vertx_http_server_request_bytes{method="PUT",quantile="0.9",} 50.0
vertx_http_server_request_bytes_count{method="PUT",} 32.0
vertx_http_server_request_bytes_sum{method="PUT",} 1557.0
# HELP vertx_pool_ratio Pool usage ratio, only present if maximum pool size could be determined
# TYPE vertx_pool_ratio gauge
vertx_pool_ratio{pool_type="worker",} 0.0
# HELP vertx_pool_in_use Number of resources used
# TYPE vertx_pool_in_use gauge
vertx_pool_in_use{pool_type="worker",} 0.0
# HELP vertx_pool_queue_time_seconds_max Time spent in queue before being processed
# TYPE vertx_pool_queue_time_seconds_max gauge
vertx_pool_queue_time_seconds_max{pool_type="worker",} 0.0
# HELP vertx_pool_queue_time_seconds Time spent in queue before being processed
# TYPE vertx_pool_queue_time_seconds summary
vertx_pool_queue_time_seconds{pool_type="worker",quantile="0.8",} 0.0
vertx_pool_queue_time_seconds{pool_type="worker",quantile="0.9",} 0.0
vertx_pool_queue_time_seconds_count{pool_type="worker",} 2.0
vertx_pool_queue_time_seconds_sum{pool_type="worker",} 0.012028692
# HELP vertx_http_server_requests_total Number of processed requests
# TYPE vertx_http_server_requests_total counter
vertx_http_server_requests_total{code="204",method="OPTIONS",route="",} 39.0
vertx_http_server_requests_total{code="200",method="GET",route="/metrics",} 210.0
vertx_http_server_requests_total{code="200",method="PUT",route="/metrics",} 32.0
vertx_http_server_requests_total{code="200",method="GET",route="/v1/strategy",} 14.0
vertx_http_server_requests_total{code="404",method="GET",route="/v1/strategy/:id",} 5.0
vertx_http_server_requests_total{code="500",method="GET",route="/v1/strategy",} 4.0
vertx_http_server_requests_total{code="200",method="GET",route="/v1/strategy/:id",} 9.0
# HELP vertx_pool_completed_total Number of elements done with the resource
# TYPE vertx_pool_completed_total counter
vertx_pool_completed_total{pool_type="worker",} 2.0
# HELP vertx_http_server_response_time_seconds_max Request processing time
# TYPE vertx_http_server_response_time_seconds_max gauge
vertx_http_server_response_time_seconds_max{code="204",method="OPTIONS",route="",} 2.40922E-4
vertx_http_server_response_time_seconds_max{code="200",method="GET",route="/metrics",} 0.001445173
vertx_http_server_response_time_seconds_max{code="200",method="PUT",route="/metrics",} 0.001104023
vertx_http_server_response_time_seconds_max{code="200",method="GET",route="/v1/strategy",} 0.002634862
vertx_http_server_response_time_seconds_max{code="404",method="GET",route="/v1/strategy/:id",} 7.56201E-4
vertx_http_server_response_time_seconds_max{code="500",method="GET",route="/v1/strategy",} 0.0
vertx_http_server_response_time_seconds_max{code="200",method="GET",route="/v1/strategy/:id",} 0.061677365
# HELP vertx_http_server_response_time_seconds Request processing time
# TYPE vertx_http_server_response_time_seconds summary
vertx_http_server_response_time_seconds{code="204",method="OPTIONS",route="",quantile="0.8",} 2.29376E-4
vertx_http_server_response_time_seconds{code="204",method="OPTIONS",route="",quantile="0.9",} 2.37568E-4
vertx_http_server_response_time_seconds_count{code="204",method="OPTIONS",route="",} 39.0
vertx_http_server_response_time_seconds_sum{code="204",method="OPTIONS",route="",} 0.010338088
vertx_http_server_response_time_seconds{code="200",method="GET",route="/metrics",quantile="0.8",} 8.84736E-4
vertx_http_server_response_time_seconds{code="200",method="GET",route="/metrics",quantile="0.9",} 0.00147456
vertx_http_server_response_time_seconds_count{code="200",method="GET",route="/metrics",} 210.0
vertx_http_server_response_time_seconds_sum{code="200",method="GET",route="/metrics",} 0.222481644
vertx_http_server_response_time_seconds{code="200",method="PUT",route="/metrics",quantile="0.8",} 8.35584E-4
vertx_http_server_response_time_seconds{code="200",method="PUT",route="/metrics",quantile="0.9",} 0.001097728
vertx_http_server_response_time_seconds_count{code="200",method="PUT",route="/metrics",} 32.0
vertx_http_server_response_time_seconds_sum{code="200",method="PUT",route="/metrics",} 0.029387288
vertx_http_server_response_time_seconds{code="200",method="GET",route="/v1/strategy",quantile="0.8",} 0.00262144
vertx_http_server_response_time_seconds{code="200",method="GET",route="/v1/strategy",quantile="0.9",} 0.00262144
vertx_http_server_response_time_seconds_count{code="200",method="GET",route="/v1/strategy",} 14.0
vertx_http_server_response_time_seconds_sum{code="200",method="GET",route="/v1/strategy",} 0.039759156
vertx_http_server_response_time_seconds{code="404",method="GET",route="/v1/strategy/:id",quantile="0.8",} 7.53664E-4
vertx_http_server_response_time_seconds{code="404",method="GET",route="/v1/strategy/:id",quantile="0.9",} 7.53664E-4
vertx_http_server_response_time_seconds_count{code="404",method="GET",route="/v1/strategy/:id",} 5.0
vertx_http_server_response_time_seconds_sum{code="404",method="GET",route="/v1/strategy/:id",} 0.003621611
vertx_http_server_response_time_seconds{code="500",method="GET",route="/v1/strategy",quantile="0.8",} 0.0
vertx_http_server_response_time_seconds{code="500",method="GET",route="/v1/strategy",quantile="0.9",} 0.0
vertx_http_server_response_time_seconds_count{code="500",method="GET",route="/v1/strategy",} 4.0
vertx_http_server_response_time_seconds_sum{code="500",method="GET",route="/v1/strategy",} 0.008717844
vertx_http_server_response_time_seconds{code="200",method="GET",route="/v1/strategy/:id",quantile="0.8",} 0.060817408
vertx_http_server_response_time_seconds{code="200",method="GET",route="/v1/strategy/:id",quantile="0.9",} 0.060817408
vertx_http_server_response_time_seconds_count{code="200",method="GET",route="/v1/strategy/:id",} 9.0
vertx_http_server_response_time_seconds_sum{code="200",method="GET",route="/v1/strategy/:id",} 0.833420453
# HELP vertx_pool_usage_seconds Time using a resource
# TYPE vertx_pool_usage_seconds summary
vertx_pool_usage_seconds{pool_type="worker",quantile="0.8",} 0.0
vertx_pool_usage_seconds{pool_type="worker",quantile="0.9",} 0.0
vertx_pool_usage_seconds_count{pool_type="worker",} 2.0
vertx_pool_usage_seconds_sum{pool_type="worker",} 0.039550932
# HELP vertx_pool_usage_seconds_max Time using a resource
# TYPE vertx_pool_usage_seconds_max gauge
vertx_pool_usage_seconds_max{pool_type="worker",} 0.0
# HELP vertx_http_server_response_bytes_max Size of responses in bytes
# TYPE vertx_http_server_response_bytes_max gauge
vertx_http_server_response_bytes_max{code="204",method="OPTIONS",route="",} 0.0
vertx_http_server_response_bytes_max{code="200",method="GET",route="/metrics",} 17766.0
vertx_http_server_response_bytes_max{code="200",method="PUT",route="/metrics",} 28.0
vertx_http_server_response_bytes_max{code="200",method="GET",route="/v1/strategy",} 1418.0
vertx_http_server_response_bytes_max{code="404",method="GET",route="/v1/strategy/:id",} 70.0
vertx_http_server_response_bytes_max{code="500",method="GET",route="/v1/strategy",} 0.0
vertx_http_server_response_bytes_max{code="200",method="GET",route="/v1/strategy/:id",} 3060438.0
# HELP vertx_http_server_response_bytes Size of responses in bytes
# TYPE vertx_http_server_response_bytes summary
vertx_http_server_response_bytes{code="204",method="OPTIONS",route="",quantile="0.8",} 0.0
vertx_http_server_response_bytes{code="204",method="OPTIONS",route="",quantile="0.9",} 0.0
vertx_http_server_response_bytes_count{code="204",method="OPTIONS",route="",} 39.0
vertx_http_server_response_bytes_sum{code="204",method="OPTIONS",route="",} 0.0
vertx_http_server_response_bytes{code="200",method="GET",route="/metrics",quantile="0.8",} 17408.0
vertx_http_server_response_bytes{code="200",method="GET",route="/metrics",quantile="0.9",} 17408.0
vertx_http_server_response_bytes_count{code="200",method="GET",route="/metrics",} 210.0
vertx_http_server_response_bytes_sum{code="200",method="GET",route="/metrics",} 3453653.0
vertx_http_server_response_bytes{code="200",method="PUT",route="/metrics",quantile="0.8",} 28.0
vertx_http_server_response_bytes{code="200",method="PUT",route="/metrics",quantile="0.9",} 28.0
vertx_http_server_response_bytes_count{code="200",method="PUT",route="/metrics",} 32.0
vertx_http_server_response_bytes_sum{code="200",method="PUT",route="/metrics",} 896.0
vertx_http_server_response_bytes{code="200",method="GET",route="/v1/strategy",quantile="0.8",} 1408.0
vertx_http_server_response_bytes{code="200",method="GET",route="/v1/strategy",quantile="0.9",} 1408.0
vertx_http_server_response_bytes_count{code="200",method="GET",route="/v1/strategy",} 14.0
vertx_http_server_response_bytes_sum{code="200",method="GET",route="/v1/strategy",} 19852.0
vertx_http_server_response_bytes{code="404",method="GET",route="/v1/strategy/:id",quantile="0.8",} 68.0
vertx_http_server_response_bytes{code="404",method="GET",route="/v1/strategy/:id",quantile="0.9",} 68.0
vertx_http_server_response_bytes_count{code="404",method="GET",route="/v1/strategy/:id",} 5.0
vertx_http_server_response_bytes_sum{code="404",method="GET",route="/v1/strategy/:id",} 350.0
vertx_http_server_response_bytes{code="500",method="GET",route="/v1/strategy",quantile="0.8",} 0.0
vertx_http_server_response_bytes{code="500",method="GET",route="/v1/strategy",quantile="0.9",} 0.0
vertx_http_server_response_bytes_count{code="500",method="GET",route="/v1/strategy",} 4.0
vertx_http_server_response_bytes_sum{code="500",method="GET",route="/v1/strategy",} 140.0
vertx_http_server_response_bytes{code="200",method="GET",route="/v1/strategy/:id",quantile="0.8",} 3014656.0
vertx_http_server_response_bytes{code="200",method="GET",route="/v1/strategy/:id",quantile="0.9",} 3014656.0
vertx_http_server_response_bytes_count{code="200",method="GET",route="/v1/strategy/:id",} 9.0
vertx_http_server_response_bytes_sum{code="200",method="GET",route="/v1/strategy/:id",} 3.9767941E7
# HELP vertx_http_server_active_requests Number of requests being processed
# TYPE vertx_http_server_active_requests gauge
vertx_http_server_active_requests{method="GET",} 1.0
vertx_http_server_active_requests{method="OPTIONS",} 0.0
vertx_http_server_active_requests{method="PUT",} 0.0
# HELP algo_processing_time_milliseconds  
# TYPE algo_processing_time_milliseconds summary
algo_processing_time_milliseconds{name="MAATR",strategyId="6685ee2bba1a0c3135e6754e",quantile="0.8",} 608.0
algo_processing_time_milliseconds{name="MAATR",strategyId="6685ee2bba1a0c3135e6754e",quantile="0.9",} 608.0
algo_processing_time_milliseconds_count{name="MAATR",strategyId="6685ee2bba1a0c3135e6754e",} 85.0
algo_processing_time_milliseconds_sum{name="MAATR",strategyId="6685ee2bba1a0c3135e6754e",} 52334.0
algo_processing_time_milliseconds{name="MAATR",strategyId="66839abe9b75c606469eaa9d",quantile="0.8",} 0.0
algo_processing_time_milliseconds{name="MAATR",strategyId="66839abe9b75c606469eaa9d",quantile="0.9",} 0.0
algo_processing_time_milliseconds_count{name="MAATR",strategyId="66839abe9b75c606469eaa9d",} 1.0
algo_processing_time_milliseconds_sum{name="MAATR",strategyId="66839abe9b75c606469eaa9d",} 168.0
algo_processing_time_milliseconds{name="RSI",strategyId="66839abe9b75c606469eaa9d",quantile="0.8",} 0.0
algo_processing_time_milliseconds{name="RSI",strategyId="66839abe9b75c606469eaa9d",quantile="0.9",} 0.0
algo_processing_time_milliseconds_count{name="RSI",strategyId="66839abe9b75c606469eaa9d",} 1.0
algo_processing_time_milliseconds_sum{name="RSI",strategyId="66839abe9b75c606469eaa9d",} 115.0
algo_processing_time_milliseconds{name="RSI",strategyId="6685ee2bba1a0c3135e6754e",quantile="0.8",} 480.0
algo_processing_time_milliseconds{name="RSI",strategyId="6685ee2bba1a0c3135e6754e",quantile="0.9",} 480.0
algo_processing_time_milliseconds_count{name="RSI",strategyId="6685ee2bba1a0c3135e6754e",} 85.0
algo_processing_time_milliseconds_sum{name="RSI",strategyId="6685ee2bba1a0c3135e6754e",} 41805.0
# HELP algo_processing_time_milliseconds_max  
# TYPE algo_processing_time_milliseconds_max gauge
algo_processing_time_milliseconds_max{name="MAATR",strategyId="6685ee2bba1a0c3135e6754e",} 656.0
algo_processing_time_milliseconds_max{name="MAATR",strategyId="66839abe9b75c606469eaa9d",} 0.0
algo_processing_time_milliseconds_max{name="RSI",strategyId="66839abe9b75c606469eaa9d",} 0.0
algo_processing_time_milliseconds_max{name="RSI",strategyId="6685ee2bba1a0c3135e6754e",} 495.0
# HELP vertx_http_server_active_connections Number of opened connections to the server
# TYPE vertx_http_server_active_connections gauge
vertx_http_server_active_connections 4.0


```
