## Using the D-Bus ratbagd sample bundle

The `dbus-ratbagd` example bundle in `samples/dbus-ratbagd` demonstrates how to
access all devices supported by ratbagd. Here is a guide to how to get it
working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   [ratbagd](https://github.com/libratbag/libratbag)

### Configure the DBus ratbagd sample bundle

1. In NodeCG, create a new D-Bus service instance using the left upper menu.
2. Configure the D-Bus service  
   There should not be any additional configuration needed for the D-Bus
   service. Just enter an empty JSON object like this:

    ```json
    {}
    ```

    After entering it, click save.

3. Set the created D-Bus service instance to the service dependency of the
   `dbus-ratbagd` bundle.  
   Select the `dbus-ratbagd` bundle and the D-Bus service in the left bottom
   menu. Then select the service instance that should be used by the
   `dbus-ratbagd` sample bundle (in this case the name of the previously created
   D-Bus instance).
4. Check the NodeCG logs  
   You should see an error or a success message and a list of connected device
   names.
