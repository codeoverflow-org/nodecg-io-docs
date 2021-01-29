## Using the Twitch Api sample bundle

The twitch-api example bundle in `samples/twitch-api` demonstrates the ability to access the twitch api (kraken/helix). Here is a guide to how to get it working.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   a Twitch oAuth-Key

_Note:_ If you don't have such a key yet you can generate it on https://twitchtokengenerator.com/, select custom scope token and select the scopes you need. For this sample you don't need any additional scopes so you can leave everything off.

### Configure the Twitch Api sample bundle

1. Start nodecg with nodecg-io installed. The twitch-api bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new twitch-api service instance using the left upper menu.

5. Enter credentials for the twitch api.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your Twitch oauth Key in monaco (the texteditor on the right) in this format:

    ```json
    {
        "oauthKey": "oauth:abcdef...."
    }
    ```

    After entering it, click save.

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created twitch-api service instance to the service dependency of the twitch-api bundle.

    Select the twitch-api bundle and the twitch-api service in the left bottom menu and then select the service instance that should be used by the twitch-api sample bundle (in this case the name of the previously created twitch-api instance).

7. Check the nodecg logs

    You should see an error or a success message and you current username, how many people you follow and if you are currently streaming.
