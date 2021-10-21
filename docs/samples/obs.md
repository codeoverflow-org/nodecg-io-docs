## Using the OBS sample bundle

The OBS example bundle in `samples/obs-scenelist` demonstrates the ability to
control an OBS instance by listing all available scenes. Here is a guide to how
to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   OBS with obs-websocket installed

_Note:_ OBS is available [here](https://obsproject.com/de/download) and
obs-websocket with install instructions is available
[here](https://github.com/Palakis/obs-websocket/releases).

### Configure the OBS sample bundle

1. In NodeCG, create a new obs service instance using the left upper menu.

2. Enter configuration for obs.

    The created instance should be automatically selected, if not select it in
    the upper left menu. Enter your obs-websocket connection information in
    monaco (the text-editor on the right) in this format:

    ```json
    {
        "host": "localhost",
        "port": 4444,
        "password": "mypassword12345678"
    }
    ```

    If you don't want to use a password, you can just remove the password
    property from the config.

    After entering it, click save.

3. Set the created obs service instance to the service dependency of the
   obs-scenelist bundle.

    Select the obs-scenelist bundle and the OBS service in the left bottom menu.
    Then select the service instance that should be used by the obs-scenelist
    bundle (in this case the name of the previously created OBS instance).

4. Check the NodeCG logs

    You should see an error or a success message and the names of all you scenes
    that you have set in OBS.
