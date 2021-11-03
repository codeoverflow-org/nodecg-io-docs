## Using the AutoHotkey sample bundle

The AutoHotkey sample bundle in `samples/ahk-sendcommand` shows how to send a
command to a HotkeylessAHK server.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A running [HotkeylessAHK](https://github.com/sebinside/HotkeylessAHK) setup.

### Configure the AutoHotkey sample bundle

1. In NodeCG, create a new ahk service instance.
2. Enter the host and port of the HotkeylessAHK Server:

    ```json
    {
        "host": "localhost",
        "port": 42800
    }
    ```

    After entering it, click save.

3. Set the sample's (`ahk-sendcommand`) dependency to be the newly created
   service instance (of type `ahk`).
4. A small window with the text “Hello World” should have popped up.
