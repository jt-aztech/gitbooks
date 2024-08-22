# DELETE /v1/subscribe

Removes an existing subscription stream from a WebSocket

**Request Body** (JSON)

* `source` (string, required): The source of the data stream requested by another service i.e. Binance.
* `interval` (string, required): The interval requested by another service i.e. "1d" for one day.
* `symbol` (string, required): The symbol requested by another service i.e. "btcusd" for the bitcoin $USD price..

#### Response

* HTTP Status Code
  * `200 OK` on success.
  * `400 Bad Request` if the provided request doesn't have the correct format.

#### Example

#### Request

```
DELETE /v1/subscribe HTTP/1.1
Host: aztechcorp.io
Content-Type: application/json

{
   "source":"Binance",
   "interval":"1d",
   "symbol":"btcusd"
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
}
```
