## Using the midi-output sample bundle

The midi-output example bundle in `samples/midi-output` demonstrates the ability
to send data to a midi device.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A midi device that can be connected to your computer

### Configure the midi-output sample bundle

1. In NodeCG, create a new midi-output service instance.

2. Enter your device information:

    ```json
    {
        "device": "name"
    }
    ```

    After entering it, click save.  
    **Note:** A script is provided to list all inputs and outputs. It can be run
    from the sample directory `samples/midi-output` using the command
    `npm run list`. The devices should be listed with their device names and
    some other stuff.  
    Under Linux this looks for example like this:

    ```
    nanoKONTROL2:nanoKONTROL2 MIDI 1 28:0
    ```

3. Set the sample's (`midi-output`) dependency to be the newly created service
   instance (of type `midi-output`).

4. Check the NodeCG logs:

    You should see an error or a success message and random midi messages should
    be sent to the device that is configured. The messages are only `Noteon`
    messages and have a random note and velocity value ranging 0-127. The
    channels they are sent from are either channel 0 or 1, but the midi protocol
    supports up to 16 channels, so it could technically range from 0-15.

### Note

Only sending `Noteon` messages is sufficient for most midi, because most of them
don't really care if you use proper `Noteoff` messages or simply send a `Noteon`
with a velocity of 0. This is due to the early days of midi, when integrated
circuits were expensive. Allowing a velocity of 0 as replacement for `Noteoff`
made instruments featuring midi more affordable.
