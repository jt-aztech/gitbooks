# 📥 API Endpoints

The service's API exposes the following 2 end points.

* **PUT /v1/strategy**
* **GET /v1/strategy/:id**

**PUT /v1/strategy**

* Receives a JSON payload containing the data needed to execute a strategy.
* Example Request:

```
{
  "name": "Bitcoin TABI",
  "address": "all",
  "sources": [
    {
      "source": "binance",
      "ticker": "btcusdt",
      "interval": "1d",
      "primary":true,
      "algorithms": [
        {
          "name": "MAATR",
          "parameters": {
            "smaPeriod": 100,
            "atrPeriod": 10
          }
        },
        {
          "name": "RSI",
          "parameters": {
            "rsiPeriod": 14
          }
        }
      ]
    },{
      "source": "alternative_me",
      "algorithms": [
        {
          "name": "FNG",
          "parameters": {
          }
        }
      ]
    }
  ]
}

```

* Example Response:

```
HTTP Code: 200
{}
```

*   **GET /v1/strategy/:id**

    * Returns strategy data for a strategy identifier
    * Example Response:

    ```
    HTTP Code: 200
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
