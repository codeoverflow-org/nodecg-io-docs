## Using the WebSocket-client sample bundle

The WebSocket-client sample bundle in `samples/websocket-client` shows how to
set up a simple WebSocket client that will ping a server every second.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

For simplicity's sake this sample will rely upon the websocket-server sample.

### Configure the WebSocket-client sample bundle

Please set up the [WebSocket-server bundle](./websocket-server.md) first and
then follow these steps:

1. In NodeCG, create a new ws-client service instance.

2. Enter the address of the sample server. This has to be a URL following the
   pattern `ws://localhost:<port>`.

    ```json
    {
        "address": "ws://localhost:7777"
    }
    ```

    After entering it, click save.

3. Set the sample's (`websocket-client`) dependency to be the newly created
   service instance (of type `websocket-client`).

4. A websocket-client has been connected and the console should display if a
   ping is sent or a pong is received.
