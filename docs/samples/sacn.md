## Using the sACN sample bundle

The sacn-sample example bundle in `samples/sacn-sample` demonstrates the ability receive data send via sACN from e.g professional lighting consoles. Here is a guide to how to get it working.

### Prerequisites

- Working NodeCG & nodecg-io installation
- A working sACN sender in the current network

### Configure the Discord sample bundle

1. Start nodecg with nodecg-io installed. The sacn-sample bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new sacn-receiver service instance using the left upper menu.

5. Enter the needed options.

   The created instance should be automatically selected, if not select it in the upper left menu. Enter your Bot token in monaco (the texteditor on the right) in this format:

   **Universes**

   The universes to use. Must be an array with numbers within 1-63999

   ```json
   {
     "universes": [1, 2, 3]
   }
   ```

   **Port**

   Optional. The multicast port to use. All professional consoles broadcast to the default port 5568.

   ```json
   {
     "universes": [1, 2, 3],
     "port": 5568
   }
   ```

   **Iface**
   Optional. If the computer is connected to multiple networks, specify which network adaptor to use by using this computer's local IP address.

   ```json
   {
     "universes": [1, 2, 3],
     "iface": "Network Adapter"
   }
   ```

   **ReuseAddr**
   Optional. Allow multiple programs on your computer to listen to the same sACN universe.

    ```json
   {
     "universes": [1, 2, 3],
     "reuseAddr": true
   }
   ```

   After entering it/them, click save.

   _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created dsacn-receiver service instance to the service dependency of the sacn-sample bundle.

   Select the sacn-sample bundle and the sacn-receiver service in the left bottom menu and then select the service instance that should be used by the sacn-sample bundle (in this case the name of the previously created sACN instance).

7. Check the nodecg logs

   You should see data logged.
