## Using the WebSocket-client sample bundle

The WebSocket-client sample bundle in `samples/websocket-client` shows how to setup a simple WebSocket client that will ping a server every second.

### Prerequisites

-   Working NodeCG & nodecg-io installation

For simplicity sake this sample will rely upon the websocket-server sample.

### Configure the WebSocket-client sample bundle

Please setup the WebSocket-server bundle first and then follow these steps:

1. Start nodecg with nodecg-io installed. The websocket-client bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new ws-client service instance using the left upper menu.

5. Enter the address of the sample server. This has to be a url following the pattern `ws://localhost:<port>`.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your port in monaco (the texteditor on the right) in this format:

    ```json
    {
        "address": "ws://localhost:7777"
    }
    ```

    After entering it, click save.

6. Set the created ws-client service instance to the service dependency of the ws-client bundle.

7. A websocket-client has been connected and the console should display if a ping is sent or a pong is recieved.
