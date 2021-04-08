## Using the StreamDeck rainbow sample bundle

The streamdeck-rainbow bundle paints your streamdeck with different colors. It is located in `samples/streamdeck-rainbow`.

Sadly you can't access the StreamDeck while another application accesses it. So you need to stop your StreamDeck Software before.

### Configure the Streamdeck Rainbow bundle

1. If you're on linux follow the instructions listed under Manual Installation [here](https://github.com/timothycrosley/streamdeck-ui/blob/master/README.md). Everything after the `sudo udevadm` command can be omitted.

2. Start nodecg with nodecg-io installed. The streamdeck-rainbow bundle is currently part of it so it should also be loaded.

3. Go to the `nodecg-io` tab in the nodecg dashboard.

4. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

5. Create a new StreamDeck service instance using the left upper menu.

6. Enter the configuration

    ```json
    {
        "device": "default"
    }
    ```

    `default` tells the bundle to automatically find a StreamDeck. If you've multiple StreamDecks you need to put in an id here.

7. Set the created StreamDeck service instance to the service dependency of the streamdeck-rainbow bundle.

8. Watch your streamdeck.
