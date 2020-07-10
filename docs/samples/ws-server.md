## Using the WebSocket Server sample bundle

The WebSocket-server sample bundle in `samples/websocket-server` shows how to setup a simple WebSocket server that will relay all incoming messages to all connected clients.

### Prerequisites

* Working NodeCG & nodcg-io installation

### Configure the websocket-server sample bundle

1. Start nodecg with nodecg-io installed. The websocket-server bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new ws-server service instance using the left upper menu.

5. Enter a port for the server. This has to be a number from 0 to 65535.

   The created instance should be automatically selected, if not select it in the upper left menu. Enter your port in monaco (the texteditor on the right) in this format:

   ```json
   {
       "port": 7777
   }
   ```

   After entering it, click save.

6. Set the created ws-server service instance to the service dependency of the ws-server bundle.

7. A websocket-server has been started at the specified port.
