## Using the Twitch PubSub sample bundle

The twitch-pubsub example bundle in `samples/twitch-pubsub` demonstrates the ability to use the Twitch PubSub api. Here is a guide to how to get it working.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   a Twitch oAuth-Key

_Note:_ If you don't have such a key yet, you can generate it on https://twitchtokengenerator.com/, select custom scope token and select these scopes: `channel_subscriptions`, `bits:read` and `channel:read:redemptions`

### Configure the Twitch PubSub sample bundle

1. Start nodecg with nodecg-io installed. The twitch-pubsub sample bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new twitch-pubsub service instance using the left upper menu.

5. Enter credentials for twitch-pubsub.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your Twitch oauth Key in monaco (the text-editor on the right) in this format:

    ```json
    {
        "oauthKey": "oauth:abcdef...."
    }
    ```

    After entering it, click save.

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created twitch-pubsub service instance to the service dependency of the twitch-pubsub sample bundle.

    Select the twitch-pubsub sample bundle and the twitch-pubsub service in the left bottom menu and then select the service instance that should be used by the twitch-pubsub sample bundle (in this case the name of the previously created twitch-pubsub instance).

7. Check the nodecg logs

    You should see an error or a success message and a log entry for each subscription, bits, bits badge unlock and channel point redemption event.
