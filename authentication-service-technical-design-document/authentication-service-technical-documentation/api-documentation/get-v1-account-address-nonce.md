# GET /v1/account/:address/nonce

Retrieve a nonce for the specified Ethereum address.

#### Request

* **Path Parameters**
  * `address` (string, required): The Ethereum address for which to retrieve the nonce.

#### Response

* HTTP Status Code
  * `200 OK` on success.
  * `400 Bad Request` if the provided address is not a valid Ethereum address.
* **Response Body** (JSON):
  * `nonce` (string): The nonce value associated with the specified address.

#### Example

#### Request

```
GET /api/as/v1/account/0x123abc456def/nonce HTTP/1.1
Host: aztechcorp.io
```

#### Response (200 OK):

```
{
  "nonce": "123456789"
}
```

#### Response (400 Bad Request):

```
{
  "error": "address used is not valid"
}
```
