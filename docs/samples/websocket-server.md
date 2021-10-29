## Using the WebSocket Server sample bundle

The WebSocket-server sample bundle in `samples/websocket-server` shows how to
set up a simple WebSocket server that will relay all incoming messages to all
connected clients.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

### Configure the websocket-server sample bundle

1. In NodeCG, create a new ws-server service instance.
2. Enter a port for the server. This has to be a number from 0 to 65535:

    ```json
    {
        "port": 7777
    }
    ```

    After entering it, click save.

3. Set the sample's (`websocket-server`) dependency to be the newly created
   service instance (of type `websocket-server`).

4. A websocket-server has been started at the specified port.
