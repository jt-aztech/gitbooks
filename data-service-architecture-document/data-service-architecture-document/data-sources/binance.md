# 💲 Binance

The Data Service sets a limit on the number of data streams per web socket connection. When this limit is surpassed, a new web socket connections is established to accommodate additional streams. Unsubscribing from a stream removes the stream from the respective web socket, potentially closing the web socket connection if the only stream on the web socket was unsubscribed from.
