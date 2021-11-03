## Using the elgato-light sample bundle

The elgato-light example bundle in `samples/elgato-light` demonstrates the ability to controll elgato keylights and elgato lightstrips. Here is a guide to how to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   at least one elgato keylight or lightstrip

### Configure the elgato-light sample bundle

1. In NodeCG, create a new elgato-light service instance.
2. Enter your IP address of your light and the type (`KeyLight` or `LightStrip`):

    ```json
    {
        "lights": [
            {
                "ipAddress": "xxx.xxx.xxx.xxx",
                "lightType": "KeyLight",
                "name": "MyLight1"
            }
        ]
    }
    ```

    You can add as many lights to this service as you wish by adding more objects inside the `lights` array.

    `name` is optional and can be used to identify lights in bundles. You can omit it if you don't use the name to get it in any bundle.

    After entering it, click save.

3. Set the sample's (`elgato-light`) dependency to be the newly created
   service instance (of type `elgato-light`).
4. Check the NodeCG logs:

    Your lights should blink for three seconds and you should see the current brightness in the NodeCG logs.
