## Using the sACN sender sample bundle

The sacn-sender example bundle in `samples/sacn-sender` demonstrates the ability send data via sACN to e.g. open lighting architecture or professional lighting equipment. Here is a guide to how to get it working.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   A working sACN receiver in the current network

### Configure the sACN sample bundle

1. Start nodecg with nodecg-io installed. The sacn-receiver-sample bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new sacn-sender service instance using the left upper menu.

5. Enter the needed options.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your universe in monaco (the text-editor on the right) in this format:

    **Universes**

    The universes to use. Must be an array with numbers within 1-63999

    ```json
    {
        "universe": 1
    }
    ```

    **Port**

    Optional. The multicast port to use. All professional consoles broadcast to the default port 5568.

    ```json
    {
        "universes": 1,
        "port": 5568
    }
    ```

    **ReuseAddr**
    Optional. Allow multiple programs on your computer to listen to the same sACN universe.

    ```json
    {
        "universes": 1,
        "reuseAddr": true
    }
    ```

    After entering it/them, click save.

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created sacn-sender service instance to the service dependency of the sacn-sender bundle.

    Select the sacn-sender bundle and the sacn-sender service in the left bottom menu and then select the service instance that should be used by the sacn-sender bundle (in this case the name of the previously created sACN instance).

7. Check the nodecg logs

    You should see data logged.
