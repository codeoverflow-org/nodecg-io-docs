## Using the Discord RPC sample bundle

The Discord Rich Presence example bundle in `samples/discord-rpc` demonstrates
the ability to access a locally running discord client. Here is a guide to how
to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A discord application with permissions `indentify` and `rpc`

_Note:_ If you don't have an application yet, you can create one
[here](https://discord.com/developers/applications)

### Configure the Discord RPC sample bundle

1. In NodeCG, create a new `discord-rpc` service instance using the left upper
   menu.
2. Enter required information.  
   The created instance should be automatically selected, if not select it in
   the upper left menu. Enter your information in monaco (the text-editor on the
   right) in this format:

    ```json
    {
        "clientId": "your client id",
        "clientSecret": "your client secret"
    }
    ```

    After entering it, click save.

3. Set the created `discord-rpc` service instance to the service dependency of
   the `discord-rpc` bundle.  
   Select the `discord-rpc` bundle and the `discord-rpc` service in the left
   bottom menu. Then select the service instance that should be used by the
   `discord-rpc` sample bundle (in this case the name of the previously created
   `discord-rpc` instance).
4. Check the NodeCG logs  
   You should see an error or a success message displaying your discord
   username.
