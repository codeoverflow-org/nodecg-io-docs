## Using the Twitch-Addons sample bundle

The Twitch-Addons example bundle in `samples/twitch-addons` demonstrates the
ability to send requests to the APIs of [BetterTTV](https://betterttv.com/), and
[FrankerFaceZ](https://www.frankerfacez.com/).

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A Twitch oAuth-Key

_Note:_ If you don't have such a key yet, you can generate it on
<https://twitchapps.com/tmi/>. Just log into your Twitch account and copy the
token. You can also use any other token. There are no special scope requirements
as the token is only used to convert channel names to IDs.

### Configure the Twitch-Addons sample bundle

1. In NodeCG, create a new twitch-addons service instance using the left upper
   menu.

2. Enter credentials for twitch.

    The created instance should be automatically selected, if not select it in
    the upper left menu. Enter your Twitch OAuth Key in monaco (the text-editor
    on the right) in this format:

    ```json
    {
        "oauthKey": "oauth:abcdef...."
    }
    ```

    After entering it, click save.

3. Set the created twitch-addons service instance to the service dependency of
   the twitch-addons bundle.

    Select the twitch-addons bundle and the twitch-addons service in the left
    bottom menu. Then select the service instance that should be used by the
    bundle (in this case the name of the previously created twitch-addons
    instance).

4. Check the NodeCG logs

    You should see an error or a success message and all BetterTTV and FFZ
    emotes from the twitch channel `#derniklaas`
