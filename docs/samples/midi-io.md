## Using the midi-io sample bundle

The midi-io example bundle in `samples/midi-io` demonstrates the ability to send/receive data to/from a midi device.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   A midi device that can be connected to your computer

### Configure the midi-io sample bundle

1. Start nodecg with nodecg-io installed. The midi-io bundle is currently part of it, so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new midi-input service instance using the left upper menu.

5. Enter your device information

    The created instance should be automatically selected, if not select it in the upper left menu. Enter the name of your device in monaco (the text-editor on the right) in this format:

    ```json
    {
        "device": "name"
    }
    ```

    After entering it, click save.
    **Note:** A script is provided to list all inputs and outputs. It can be run from the sample directory `samples/midi-io` using the command `npm run list`. The devices should be listed with their device names and some other stuff.
    Under Linux this looks for example like this:

    ```
    nanoKONTROL2:nanoKONTROL2 MIDI 1 28:0
    ```

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Create a new midi-output service instance using the left upper menu.

7. Repeat step 5 for your midi-output service. In most cases you want to use the same device for input and output.

8. Set the created midi-output service instance to the service dependency of the midi-io sample bundle.

    Select the midi-io bundle and the midi-output service in the left bottom menu and then select the service instance that should be used by the midi-io bundle (in this case the name of the previously created midi-output instance).

9. Set the created midi-input service instance to the service dependency of the midi-io sample bundle.

    Select the midi-io bundle and the midi-input service in the left bottom menu and then select the service instance that should be used by the midi-io bundle (in this case the name of the previously created midi-input instance).

10. Check the nodecg logs

    You should see an error or a success message and midi messages that are received and echoed back to the device that is configured. The messages are only modified, if the received Message is a `Noteon` with a velocity of greater than zero or a control change message with a value of at least 64. `Noteoff` messages are always echoed unmodified.

### Note

A `Noteon` message with a velocity of 0 should be handled like a `Noteoff` message, so they are echoed unmodified. Otherwise, this would get annoying very fast.  
If a control change is assigned to the push-button values of 64 and up are interpreted as on and values lower than that are interpreted as off. Most somewhat modern Midi devices send 127 as on and 0 as off, but 63 and 64 should also be sufficient.
