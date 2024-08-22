# 💲 Binance

1. **Initial Subscription:**&#x20;
   1. When the first data stream is subscribed to, a new web socket connection is created, and this connection subscribes to the new data stream.
2. **Subsequent Subscriptions**:
   1. As additional data streams are subscribed to, they are added to the existing web socket connection's subscriptions.
   2. If a web socket reaches its configured maximum number of streams, any new data stream subscription will trigger the creation of a new web socket, which will then subscribe to the new data stream.
3. **Unsubscribing from Data Streams**:
   1. When a data stream is unsubscribed from, the web socket connection subscribed to that stream will unsubscribe from that stream.
   2. This may cause a web socket that was previously at its maximum capacity to move below the configured limit.
4. **Managing Multiple Web Socket Connections**:
   1. When there are multiple web socket connections and a new data stream is subscribed to, the system will check the existing connections.
   2. The first web socket that is below the configured maximum number of streams will be instructed to subscribe to the new stream.
   3. If all existing web socket connections are at capacity, a new web socket will be created to handle the new data stream subscription.
