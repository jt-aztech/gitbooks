# PUT /v1/account/:address/verifySignature

Verifies a signature provided by the user and issues a JWT token upon successful verification.

#### Request

* **Path Parameters**
  * `address` (string, required): The Ethereum address to be verified.
* **Request Body** (JSON)
  * `signature` (string, required): The signature provided by the user.

#### Response

* **HTTP Status Code**
  * `200 OK` on successful verification and token issuance.
  * `400 Bad Request` if the provided signature is incomplete or invalid.
  * `404 Not Found` if no account is found for the specified address.
* **Response Body** (JSON):
  * `jwt` (string): The JWT token issued upon successful verification.

#### Example

#### Request

```
PUT /api/as/v1/account/0x123abc456def/verifySignature HTTP/1.1
Host: aztechcorp.io
Content-Type: application/json

{
  "signature": "0x123abc..."
}

```

#### Response (200 OK)

```
{
  "jwt": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIwM...."
}
```

#### Response (400 Bad Request)

```
{
  "error": "Signature incomplete."
}
```

#### Response (404 Not Found)

```
{
  "error": "No account found for address."
}
```
