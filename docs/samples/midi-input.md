## Using the midi-input sample bundle

The midi-input example bundle in `samples/midi-input` demonstrates the ability
to read data from a midi device.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A midi device that can be connected to your computer

### Configure the midi-input sample bundle

1. In NodeCG, create a new midi-input service instance.

2. Enter your device information:

    ```json
    {
        "device": "name"
    }
    ```

    After entering it, click save.  
    **Note:** A script is provided to list all inputs and outputs. It can be run
    from the sample directory `samples/midi-input` using the command
    `npm run list`. The devices should be listed with their device names and
    some other stuff.  
    Under Linux this looks for example like this:

    ```
    nanoKONTROL2:nanoKONTROL2 MIDI 1 28:0
    ```

3. Set the sample's (`midi-input`) dependency to be the newly created service
   instance (of type `midi-input`).
4. Check the NodeCG logs:

    You should see an error or a success message and all midi messages that are
    sent by the device that is configured.
