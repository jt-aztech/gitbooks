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
GET /v1/strategy/671cd64bba7d04639a2e3e79 HTTP/1.1
Host: aztechcorp.io\
```

#### Response (200 OK)

```
{
        "_id": "671cd64bba7d04639a2e3e79",
        "name": "Bitcoin TABI",
        "address": "all",
        "active": false,
        "sources": [
            {
                "ticker": "btcusdt",
                "interval": "1d",
                "source": "binance",
                "primary": true,
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
                                "time": 1729944299999,
                                "value": 87.74293402714711
                            },
                            {
                                "time": 1729944599999,
                                "value": 65.64196037542223
                            }
                        ]
                    }
                ]
            },
            {
                "ticker": null,
                "interval": null,
                "source": "alternative_me",
                "primary": false,
                "algorithms": [
                    {
                        "name": "FNG",
                        "parameters": {
                            "smaPeriod": 0,
                            "atrPeriod": 0,
                            "rsiPeriod": 0
                        },
                        "data": [
                            {
                                "time": 1729944299999,
                                "value": 47.61904761904761
                            },
                            {
                                "time": 1729944599999,
                                "value": 41.66666666666667
                            }
                        ]
                    }
                ]
            }
        ],
        "btcusdt_5m_binance": [
            {
                "_id": "671cdaec5f3a6b7e90c1714f",
                "e": "kline",
                "E": 1729944300009,
                "s": "btcusdt",
                "k": {
                    "t": 1729944000000,
                    "T": 1729944299999,
                    "s": "btcusdt",
                    "i": "5m",
                    "f": 3966428729,
                    "L": 3966436284,
                    "o": "67138.00000000",
                    "c": "67166.00000000",
                    "h": "67180.00000000",
                    "l": "67110.00000000",
                    "v": "26.16012000",
                    "n": 7556,
                    "x": true,
                    "q": "1756463.63504640",
                    "V": "15.48908000",
                    "Q": "1040003.57650320",
                    "B": "0"
                },
                "S": "binance",
                "nek": 1729944599999,
                "o": "websocket",
                "status": "pending"
            },
            {
                "_id": "671cdc185f3a6b7e90c17150",
                "e": "kline",
                "E": 1729944600009,
                "s": "btcusdt",
                "k": {
                    "t": 1729944300000,
                    "T": 1729944599999,
                    "s": "btcusdt",
                    "i": "5m",
                    "f": 3966436285,
                    "L": 3966439737,
                    "o": "67166.00000000",
                    "c": "67104.45000000",
                    "h": "67166.01000000",
                    "l": "67104.44000000",
                    "v": "14.58766000",
                    "n": 3453,
                    "x": true,
                    "q": "979351.44335330",
                    "V": "4.75439000",
                    "Q": "319196.52499270",
                    "B": "0"
                },
                "S": "binance",
                "nek": 1729944899999,
                "o": "websocket",
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
