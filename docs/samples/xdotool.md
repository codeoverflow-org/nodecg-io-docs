## Using the Xdotool sample bundle

The Xdotool sample bundle in `samples/xdotool-windowminimize` shows how to use
the xdotool service to execute
[xdotool commands](http://manpages.ubuntu.com/manpages/trusty/man1/xdotool.1.html)
by minimizing the currently active window.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

-   Xdotool installed (Only works on Linux)

### Configure the Xdotool sample bundle

1. In NodeCG, create a new xdotool service instance using the left upper menu.

2. Enter settings port `-1` tells nodecg-io to use a locally installed xdotool.

    The created instance should be automatically selected, if not select it in
    the upper left menu. Configure local xdotool in monaco (the text-editor on
    the right) using this config:

    ```json
    {
        "host": "127.0.0.1",
        "port": -1
    }
    ```

    After entering it, click save.

3. Set the created xdotool service instance to the service dependency of the
   xdotool bundle.

4. Your browser window should get minimized.
