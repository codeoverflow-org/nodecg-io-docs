## Using the AHK sample bundle

The AHK sample bundle in `samples/ahk-sendcommand` shows how to send a command to a HotkeylessAHK server.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   A running [HotkeylessAHK](https://github.com/sebinside/HotkeylessAHK) setup.

### Configure the ahk sample bundle

1. Start nodecg with nodecg-io installed. The ahk bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new ahk service instance using the left upper menu.

5. Enter the host and port of the HotkeylessAHK Server.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your host and port in monaco (the text-editor on the right) in this format:

    ```json
    {
        "host": "localhost",
        "port": 42800
    }
    ```

    After entering it, click save.

6. Set the created ahk service instance to the service dependency of the ahk bundle.

7. A small window with the text "Hello World" should have popped up.
