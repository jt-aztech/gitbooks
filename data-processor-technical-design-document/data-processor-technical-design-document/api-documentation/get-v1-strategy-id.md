# GET /v1/strategy/:id

GET /v1/strategy/:id retrieves a strategy for a given ID

#### Request

* **Path Parameters**
  * `id`(string, required): The id of the strategy to retrieve

#### Response

* HTTP Status Code
  * `200 OK`on success.
  * `404 Not Found`if the strategy doesn't exist for the provided ID doesn't exist.
  * `401 Unauthorized`if the strategy found doesn't belong to the address of the user.
* **Response Body** (JSON):
  * (JSON): The JSON object associated with the specified id.

#### Example

#### Request

```
GET /v1/strategy/66839abe9b75c606469eaa9d HTTP/1.1
Host: aztechcorp.io\
```

#### Response (200 OK)

```
{
    "name": "Bitcoin TABI",
    "ticker": "btcusdt",
    "interval": "1h",
    "source": "binance",
    "address": "all",
    "active": true,
    "algorithms": [
        {
            "name": "MAATR",
            "parameters": {
                "smaPeriod": 100,
                "atrPeriod": 10,
                "rsiPeriod": 0
            },
            "data": [
                {
                    "time": 1693987199999,
                    "value": "NaN"
                }
            ]
        },
        {
            "name": "RSI",
            "parameters": {
                "smaPeriod": 0,
                "atrPeriod": 0,
                "rsiPeriod": 14
            },
            "data": [
                {
                    "time": 1693987199999,
                    "value": "NaN"
                }
            ]
        }
    ],
    "btcusdt_1h_binance": [
        {
            "_id": "66839ac5ee6080499779a880",
            "e": "kline",
            "E": 1719900869447,
            "s": "btcusdt",
            "k": {
                "t": 1693983600000,
                "T": 1693987199999,
                "s": "btcusdt",
                "i": "1h",
                "o": "25780.00000000",
                "c": "25728.93000000",
                "h": "25784.57000000",
                "l": "25723.65000000",
                "v": "912.61434000",
                "x": true
            },
            "S": "binance",
            "nek": 1693990799999,
            "o": "genesis",
            "status": "pending"
        }
    ]
}
```

#### Response (404 Not Found)

```
{
    "message": "Not found",
    "path": "/v1/strategy/66839abe9b75c606469eaa9d"
}
```

#### Response (401 Unauthorized)

```
{
    "message": "Not authorized"",
    "path": "/v1/strategy/66839abe9b75c606469eaa9d"
}
```
