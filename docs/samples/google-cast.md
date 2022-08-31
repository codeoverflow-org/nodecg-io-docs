## Using the Google Cast sample bundle

The google-cast example bundle in `samples/google-cast` demonstrates the ability
to cast a mp3 file to a Google Cast device. Here is a guide
to how to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   a Google Cast device inside your local network

### Configure the Google Cast sample bundle

1. In nodecg-io, create a new google-cast service instance.

2. Select a device inside the configuration preset list or add a device using a config like this:

    ```json
    {
        "host": "192.168.2.111",
        "friendlyName": "My Chromecast"
    }
    ```

    After entering it, click save.

3. Set the sample's (`google-cast`) dependency to be the newly created service
   instance (of type `google-cast`).

4. Listen to the beautiful music playing through your Google Cast device:
