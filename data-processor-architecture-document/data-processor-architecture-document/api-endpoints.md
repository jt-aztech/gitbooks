# 📥 API Endpoints

The service's API exposes the following 2 end points.

* **PUT /v1/strategy**
* **GET /v1/strategy/:id**

**PUT /v1/strategy**

* Receives a JSON payload containing the data needed to execute a strategy.
* Example Request:

```
{
    "name":"Bitcoin TABI",
    "ticker":"btcusdt",
    "interval":"1h",
    "source":"binance", 
    "address":"all",
    "algorithms":[
        {
            "name":"MAATR",
            "parameters":{
                "smaPeriod":100,
                "atrPeriod":10 
            }
        },{
            "name":"RSI",
            "parameters":{
                "rsiPeriod":14 
            }
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
        "name": "Bitcoin TABI",
        "ticker": "btcusdt",
        "interval": "1h",
        "source": "binance",
        "address": "all",
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

    ```
