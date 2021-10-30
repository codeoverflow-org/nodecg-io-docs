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

1. In NodeCG, create a new `discord-rpc` service instance.
2. Enter the `clientId` and `clientSecret` for the service:

    ```json
    {
        "clientId": "your client id",
        "clientSecret": "your client secret"
    }
    ```

    After entering it, click save.

3. Set the sample's (`discord-rpc`) dependency to be the newly created service
   instance (of type `discord-rpc`).
4. Check the NodeCG logs:

    You should see an error or a success message displaying your discord
    username.
