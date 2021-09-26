## Using the Nanoleaf sample bundle

The Nanoleaf example bundle in `samples/nanoleaf` demonstrates the ability to control your nanoleaf lights. This example code sets all panels to an orange color. Here is a guide to how to get it working.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   IP address of your nanoleaf controller

### Configure the nanoleaf sample bundle

1. Start nodecg with nodecg-io installed. The nanoleaf sample bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new nanoleaf service instance using the left upper menu.

5. Enter configuration.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your nanoleaf controller IP address in this format (change the IP accordingly):

    ```json
    {
        "ipAddress": "xxx.xxx.xxx.xxx"
    }
    ```

    Before clicking save put your nanoleaf controller into pairing mode by holding the on-off button for 5-7 seconds till the LED starts flashing.

    After entering your config and entering pairing mode, click save.

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created nanoleaf service instance to the service dependency of the nanoleaf sample bundle.

    Select the nanoleaf sample bundle and the nanoleaf service in the left bottom menu and then select the service instance that should be used by the nanoleaf sample bundle (in this case the name of the previously created nanoleaf instance).

7. If everything worked your nanoleafs should now shine orange.

    If not you should check the nodecg logs for any errors.
