## Using the Twitch sample bundle

The Twitch-chat example bundle in `samples/twitch-chat` demonstrates the ability
to get access to a twitch chat and printing all messages of it. Here is a guide
to how to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   a Twitch oAuth-Key

!!! NOTE

    If you don't have such a key yet, you can generate it on
    <https://twitchapps.com/tmi/>. Just log into your Twitch account and copy
    the token.

### Configure the Twitch sample bundle

1. In NodeCG, create a new twitch-chat service instance.

2. Enter your Twitch OAuth Key:

    ```json
    {
        "oauthKey": "oauth:abcdef...."
    }
    ```

    After entering it, click save.

3. Set the sample's (`twitch-chat`) dependency to be the newly created service
   instance (of type `twitch-chat`).

4. Check the NodeCG logs:

    You should see an error or a success message and all twitch messages that
    are written in the twitch channel that is hardcoded in
    `samples/twitch-chat/extension/index.ts`.
