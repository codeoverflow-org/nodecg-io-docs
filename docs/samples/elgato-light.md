## Using the elgato-light sample bundle

The elgato-light example bundle in `samples/elgato-light` demonstrates the ability to controll elgato keylights and elgato lightstrips. Here is a guide to how to get it working.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   at least one elgato keylight or lightstrip

### Configure the elgato-light sample bundle

1. Start nodecg with nodecg-io installed. The elgato-light sample bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new elgato-light service instance using the left upper menu.

5. Enter configuration:

    The created instance should be automatically selected, if not select it in the upper left menu. Enter the IP address to your light and the type (`KeyLight` or `LightStrip`) in monaco (the text-editor on the right) in this format:

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

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created elgato-light service instance to the service dependency of the elgato-light sample bundle.

    Select the elgato-light example bundle and the elgato-light service in the left bottom menu and then select the service instance that should be used by the elgato-light example bundle (in this case the name of the previously created elagto-light instance).

7. Check the nodecg logs

    Your lights should blink for three seconds and you should see the current brightness in the nodecg logs.
