## Using the RCON sample bundle

The rcon sample bundle in `samples/rcon-minecraft` shows how to send a command to a minecraft server.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   A working [Minecraft](https://minecraft.net) server.

### Configure the rcon sample bundle

1. Start nodecg with nodecg-io installed. The rcon bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new rcon service instance using the left upper menu.

5. Enter the host, port and password of the rcon connection. This can be found in the ``server.properties`` file (rcon.port, rcon.password)

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your host and port in monaco (the text-editor on the right) in this format:

    ```json
    {
        "host": "localhost",
        "port": 25575,
        "password:": "ThisIsAVeryGoodPassword"
    }
    ```

    After entering it, click save.

6. Set the created rcon service instance to the service dependency of the rcon-minecraft bundle.

7. In the nodecg console you will see a list with all online players. It will also send a /say command to the minecraft server.
