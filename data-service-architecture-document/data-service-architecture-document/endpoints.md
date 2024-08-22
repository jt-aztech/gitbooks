# 📥 Endpoints

The Data service's API consists of two end points - PUT /v1/subscribe & Delete /v1/subscribe.

*   PUT /v1/subscribe

    * Receives a JSON payload containing the data needed to subscribe to a data source.
    * Example Request:

    ```
    {
       "source":"binance",
       "interval":"1d",
       "symbol":"btcusd"
    }
    ```

    * Example Response:



    ```
    HTTP Code: 200
    {
        "success":true
    }
    ```
*   &#x20;Delete /v1/subscribe

    * Receives a JSON payload containing the data needed to unsubscribe to a data stream.
    * Example Request:

    ```
    {
       "source":"binance",
       "interval":"1d",
       "symbol":"btcusd"
    }
    ```

    * Example Response:

    ```
    HTTP Code: 200
    {
        "success":true

    ```
