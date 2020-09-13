## Using the midi-input sample bundle

The midi-input example bundle in `samples/midi-input` demonstrates the the ability to read data from a midi device. 

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   A midi device that can be connected to your computer

### Configure the midi-input sample bundle

1. Start nodecg with nodecg-io installed. The Twitch-chat bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new midi-input service instance using the left upper menu.

5. Enter your device information

    The created instance should be automatically selected, if not select it in the upper left menu. Enter the name of your device in monaco (the texteditor on the right) in this format:

    ```json
    {
        "device": "name"
    }
    ```

    After entering it, click save.
    __Note:__ A script is provided to list all inputs and outputs. It can be run from the sample directory `samples/midi-input` using the command `npm run list`. The devices should be listed with there device names and some other stuff.
    under linux this looks for example like this:
    
    ```
    nanoKONTROL2:nanoKONTROL2 MIDI 1 28:0
    ```

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created midi-input service instance to the service dependency of the Twitch-chat bundle.

    Select the midi-input bundle and the midi-input service in the left bottom menu and then select the service instance that should be used by the Twitch-chat bundle (in this case the name of the previously created midi-input instance).

7. Check the nodecg logs

    You should see an error or a success message and all midi messages that are sent by the device that is configured.
