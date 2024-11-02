# PUT /v1/strategy

PUT /v1/strategy adds a new strategy.

**Request Body** (JSON)

* `name`  (string, required): The name of the strategy.
* `address`(string required): The Ethereum address that owns and can see this strategy i.e. 0x79655530BD5D6B507AA4bd9bA158f20E569d50C2 or "all" if it is a public strategy.
* `sources` (array, required): This list of sources the strategy use.
  * `source`(string, required): The source of the ticker i.e. Binance.
  * `ticker` (string, required(for primary)): The ticker that the strategy uses i.e. BTCUSDT(Bitcoin USD)
  * `interval`(string, required(for primary)): The interval that the ticker uses i.e 1h, 4h, 1d(1 hour, 4 hours, 1 day)
  * `primary`(boolean, required): Is this the source that is used for the chart.
  * `algorithms` (array, required): The list of algorithms that this strategy use.
    * `name`(string, required): The name of the algorithm i.e. MAATR or RSI
    * `parameters`(array, required): The parameters used by the strategy.
      * `smaPeriod`(int, optional): The moving average period of the algorithm.
      * `atrPeriod`(int, optional): The average true range period of the algorithm.
      * `rsiPeriod`(int, optional): The relative strength index period of the algorithm.

#### Response

* HTTP Status Code
  * `200 OK`on success.
  * `404 Bad Request` the provided request doesn't have the correct format.

#### Example

#### Request

```
PUT /v1/strategy HTTP/1.1
Host: aztechcorp.io
Content-Type: application/json
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

#### Response (200 OK)

```
{
}
```

#### Response (400 Bad Request)

```
{
    "message": "Bad request",
    "path": "/v1/strategy"
}
```

#### Response (404 Unauthorized)

```
{
    "message": "Not authorized"",
    "path": "/v1/strategy"
}
```
