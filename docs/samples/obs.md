## Using the OBS sample bundle

The OBS example bundle in `samples/obs-scenelist` demonstrates the ability to control a OBS instance by listing all available scenes. Here is a guide to how to get it working.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   OBS with obs-websocket installed

_Note:_ OBS is available [here](https://obsproject.com/de/download) and obs-websocket with install instructions is available [here](https://github.com/Palakis/obs-websocket/releases).

### Configure the OBS sample bundle

1. Start nodecg with nodecg-io installed. The obs-scenelist bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new obs service instance using the left upper menu.

5. Enter config for obs.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your obs-websocket connection information in monaco (the texteditor on the right) in this format:

    ```json
    {
        "host": "localhost",
        "port": 4444,
        "password": "mypassword12345678"
    }
    ```

    If you don't want to use a password you can just remove the password property from the config.

    After entering it, click save.

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created obs service instance to the service dependency of the obs-scenelist bundle.

    Select the obs-scenelist bundle and the OBS service in the left bottom menu and then select the service instance that should be used by the obs-scenelist bundle (in this case the name of the previously created OBS instance).

7. Check the nodecg logs

    You should see an error or a success message and the names of all you scenes that you have set in OBS.
