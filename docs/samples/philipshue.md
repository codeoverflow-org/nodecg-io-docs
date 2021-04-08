## Using the Philips Hue sample bundle

The philipshue-lights example bundle in `samples/philipshue-lights` demonstrates the ability to connect to the Philips Hue bridge and control philips hue accessories.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   A Philips Hue bridge with some connected accessories

### Configure the Philips Hue sample bundle

1. Start nodecg with nodecg-io installed. The philipshue-lights sample bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new philipshue service instance using the left upper menu.

5. Enter configuration for hue.

    The created instance should be automatically selected, if not select it in the upper left menu. If you want the bridge to be automatically discovered just set `discover` to true like this:

    ```json
    {
        "discover": true
    }
    ```

    If you want to provide the ip address manually you can provide them like this:

    ```json
    {
        "discover": false,
        "ipAddr": "x.x.x.x"
    }
    ```

    After entering it, press the big link button on your bridge and then click save.

    After the first time you connect to your bridge it will create a user and an API key which will be saved so that you only need to press the link button when you connect it for the first time.

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created philipshue service instance to the service dependency of the philipshue-lights sample bundle.

    Select the philipshue-lights sample bundle and the philipshue service in the left bottom menu and then select the service instance that should be used by the philipshue-lights sample bundle (in this case the name of the previously created philipshue instance).

7. Check the nodecg logs

    You should see an error or a success message and the number of lights that the bridge knows of.
