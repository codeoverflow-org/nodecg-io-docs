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

1. In NodeCG, create a new midi-input service instance using the left upper
   menu.

2. Enter your device information

    The created instance should be automatically selected, if not select it in
    the upper left menu. Enter the name of your device in monaco (the
    text-editor on the right) in this format:

    ```json
    {
        "device": "name"
    }
    ```

    After entering it, click save. **Note:** A script is provided to list all
    inputs and outputs. It can be run from the sample directory
    `samples/midi-input` using the command `npm run list`. The devices should be
    listed with their device names and some other stuff. Under Linux this looks
    for example like this:

    ```
    nanoKONTROL2:nanoKONTROL2 MIDI 1 28:0
    ```

3. Set the created midi-input service instance to the service dependency of the
   midi-input sample bundle.

    Select the midi-input bundle and the midi-input service in the left bottom
    menu. Then select the service instance that should be used by the midi-input
    bundle (in this case the name of the previously created midi-input
    instance).

4. Check the NodeCG logs

    You should see an error or a success message and all midi messages that are
    sent by the device that is configured.
