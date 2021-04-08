## Using the IRC sample bundle

The IRC example bundle in `samples/irc` demonstrates the ability to get access to an IRC chat. This sample is designed to log the twitch IRC chat of skate702.

### Prerequisites

-   Working NodeCG & nodecg-io installation

### Configure the IRC sample bundle

1. Start nodecg with nodecg-io installed. The irc sample bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new irc service instance using the left upper menu.

5. Enter credentials for irc.

    The created instance should be automatically selected, if not select it in the upper left menu. In this example we will anonymously connect to the twitch IRC chat. Enter the config in this format:

    ```json
    {
        "host": "irc.chat.twitch.tv",
        "port": 6667,
        "nick": "justinfan123456"
    }
    ```

    Here you may want to change the numbers of the nick to be unique to you.

    After entering it, click save.

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created irc service instance to the service dependency of the irc sample bundle.

    Select the irc sample bundle and the irc service in the left bottom menu and then select the service instance that should be used by the irc sample bundle (in this case the name of the previously created irc instance).

7. Check the nodecg logs

    You should see an error or a success message and all twitch messages that are written in the twitch channel that is hardcoded in `samples/irc/extension/index.ts`.
