## Using the RCON sample bundle

The RCON sample bundle in `samples/rcon-minecraft` shows how to send a command
to a Minecraft server.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A working [Minecraft](https://minecraft.net) server.

### Configure the RCON sample bundle

1. In NodeCG, create a new RCON service instance.

2. Enter the host, port, and password of the RCON connection. This can be found
   in the `server.properties` file (`rcon.port`, `rcon.password`):

    ```json
    {
        "host": "localhost",
        "port": 25575,
        "password:": "ThisIsAVeryGoodPassword"
    }
    ```

    After entering it, click save.

3. Set the sample's (`rcon-minecraft`) dependency to be the newly created
   service instance (of type `rcon`).

4. In the NodeCG console you will see a list with all online players. It will
   also send a /say command to the Minecraft server.
