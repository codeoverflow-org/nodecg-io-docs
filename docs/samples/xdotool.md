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

1. In NodeCG, create a new xdotool service instance.

2. Enter settings port `-1` tells nodecg-io to use a locally installed xdotool:

    ```json
    {
        "host": "127.0.0.1",
        "port": -1
    }
    ```

    After entering it, click save.

3. Set the sample's (`xdotool-windowminimize`) dependency to be the newly
   created service instance (of type `xdotool`).

4. Your browser window should get minimized.
