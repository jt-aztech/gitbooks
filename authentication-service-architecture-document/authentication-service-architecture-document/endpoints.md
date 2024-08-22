# Endpoints

* **GET /v1/account/:address/nonce**
  * Returns a JSON payload containing a nonce for the specified address.
  * Example Response:

```
{
    "nonce": 1234
}
```

* **POST /v1/account/:address/verifySignature**
  * Receives a JSON payload containing the user's signature of a static message concatenated with a nonce and returns a JWT secret upon successful verification.
  * Example Request:

```
{
    "signature": "abcd"
}
```

* Example Response:

```
{
    "jwtsecret": "xyz..."
}
```

* **GET /metrics**
  * Exposes metrics for monitoring and performance analysis.
* #### PUT /metrics
  * Accepts metrics for round trip time
  * Example Request:

```
{
    "code": "metric-name",
    "rtt": 0.1,
    "route":"/v1/account/:address/nonce"
}
```
