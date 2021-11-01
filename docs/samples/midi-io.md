## Using the midi-io sample bundle

The midi-io example bundle in `samples/midi-io` demonstrates the ability to
send/receive data to/from a midi device.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A midi device that can be connected to your computer

### Configure the midi-io sample bundle

1.  In NodeCG, create a new midi-input service instance.

2.  Enter your device information:

    ```json
    {
        "device": "name"
    }
    ```

    After entering it, click save.

    !!! NOTE

        A script is provided to list all inputs and outputs. It can be run
        from the sample directory `samples/midi-input` using the command
        `npm run list`. The devices should be listed with their device names
        and some other stuff.

        Under Linux this looks for example like this:

        ```plain
        nanoKONTROL2:nanoKONTROL2 MIDI 1 28:0
        ```

3.  Create a new midi-output service instance using the left upper menu.

4.  Set the sample's (`midi-io`) dependencies to be the newly created service
    instances (of type `midi-input` & `midi-output`).

5.  Check the NodeCG logs:

    You should see an error or a success message and midi messages that are
    received and echoed back to the device that is configured. The messages are
    only modified, if the received Message is a `Noteon` with a velocity of
    greater than zero or a control change message with a value of at least 64.
    `Noteoff` messages are always echoed unmodified.

### Note

A `Noteon` message with a velocity of 0 should be handled like a `Noteoff`
message, so they are echoed unmodified. Otherwise, this would get annoying very
fast.  
If a control change is assigned to the push-button values of 64 and up are
interpreted as on and values lower than that are interpreted as off. Most
somewhat modern Midi devices send 127 as on and 0 as off, but 63 and 64 should
also be sufficient.
