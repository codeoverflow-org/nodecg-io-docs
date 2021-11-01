## Using the Atem sample bundle

The Atem sample bundle in `samples/atem` shows how to listen to commands.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.


### Configure the AutoHotkey sample bundle

1. In NodeCG, create a new atem service instance.
2. Enter the address and optional a port of the Atem server:

    ```json
    {
        "address": "0.0.0.0"
    }
    or

    ```json
    {
        "address": "0.0.0.0",
        "port": 9910
    }
    ```

    After entering it, click save.

3. Set the sample's (`atem`) dependency to be the newly created
   service instance (of type `atem`).
4. Now all commands sended through the atem protocol should be logged in the console.
