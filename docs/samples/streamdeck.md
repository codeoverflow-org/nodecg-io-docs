## Using the StreamDeck rainbow sample bundle

The streamdeck-rainbow bundle paints your streamdeck with different colours. It
is located in `samples/streamdeck-rainbow`.

Sadly you can't access the StreamDeck while another application accesses it. So
you need to stop your StreamDeck Software before.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:** (If you're on Linux)

Follow the instructions listed under Manual Installation
[here](https://github.com/timothycrosley/streamdeck-ui/blob/master/README.md).
Everything after the `sudo udevadm` command can be omitted.

### Configure the StreamDeck Rainbow bundle

1.  In NodeCG, create a new StreamDeck service instance.

2.  Enter the configuration:

    ```json
    {
        "device": "default"
    }
    ```

    !!! INFO

        `default` tells the bundle to automatically find a StreamDeck. If you use
        multiple StreamDecks, you need to put in an ID here.

3.  Set the sample's (`streamdeck-rainbow`) dependency to be the newly created
    service instance (of type `streamdeck`).

4.  Watch your streamdeck.
