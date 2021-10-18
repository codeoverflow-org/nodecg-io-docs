## Using the Twitch-Addons sample bundle

The Twitch-Addons example bundle in `samples/twitch-addons` demonstrates the ability to send requests to the APIs of [BetterTTV](https://betterttv.com/), and [FrankerFaceZ](https://www.frankerfacez.com/).

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   a Twitch OAuth Key

_Note:_ If you don't have such a key yet, you can generate it on <https://twitchapps.com/tmi/>. Just log into your Twitch account and copy the token. You can also use any other token. There are no special scope requirements as the token is only used to convert channel names to IDs.

### Configure the Twitch-Addons sample bundle

1. Start nodecg with nodecg-io installed. The Twitch-Addons bundle is currently part of it, so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new twitch-addons service instance using the left upper menu.

5. Enter credentials for twitch.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your Twitch OAuth Key in monaco (the text-editor on the right) in this format:

    ```json
    {
        "oauthKey": "oauth:abcdef...."
    }
    ```

    After entering it, click save.

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created twitch-addons service instance to the service dependency of the twitch-addons bundle.

    Select the twitch-addons bundle and the twitch-addons service in the left bottom menu and then select the service instance that should be used by the bundle (in this case the name of the previously created twitch-addons instance).

7. Check the nodecg logs

    You should see an error or a success message and all BetterTTV and FFZ emotes from the twitch channel `#derniklaas`
