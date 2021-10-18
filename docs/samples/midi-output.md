## Using the midi-output sample bundle

The midi-output example bundle in `samples/midi-output` demonstrates the ability to send data to a midi device.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   A midi device that can be connected to your computer

### Configure the midi-output sample bundle

1. Start nodecg with nodecg-io installed. The midi-output bundle is currently part of it, so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new midi-output service instance using the left upper menu.

5. Enter your device information

    The created instance should be automatically selected, if not select it in the upper left menu. Enter the name of your device in monaco (the text-editor on the right) in this format:

    ```json
    {
        "device": "name"
    }
    ```

    After entering it, click save.
    **Note:** A script is provided to list all inputs and outputs. It can be run from the sample directory `samples/midi-output` using the command `npm run list`. The devices should be listed with their device names and some other stuff.
    Under Linux this looks for example like this:

    ```
    nanoKONTROL2:nanoKONTROL2 MIDI 1 28:0
    ```

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created midi-output service instance to the service dependency of the midi-output sample bundle.

    Select the midi-output bundle and the midi-output service in the left bottom menu and then select the service instance that should be used by the midi-output bundle (in this case the name of the previously created midi-output instance).

7. Check the nodecg logs

    You should see an error or a success message and random midi messages should be sent to the device that is configured. The messages are only `Noteon` messages and have a random note and velocity value ranging 0-127. The channels they are sent from are either channel 0 or 1, but the midi protocol supports up to 16 channels, so it could technically range from 0-15.

### Note

Only sending `Noteon` messages is sufficient for most midi, because most of them don't really care if you use proper `Noteoff` messages or simply send a `Noteon` with a velocity of 0. This is due to the early days of midi, when integrated circuits were expensive. Allowing a velocity of 0 as replacement for `Noteoff` made instruments featuring midi more affordable.
