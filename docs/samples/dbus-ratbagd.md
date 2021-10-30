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

1. In NodeCG, create a new D-Bus service instance.
2. Configure the D-Bus service  
   There should not be any additional configuration needed for the D-Bus
   service.

3. Set the sample's (`dbus-ratbagd`) dependency to be the newly created service
   instance (of type `dbus`).

4. Check the NodeCG logs:

    You should see an error or a success message and a list of connected device
    names.
