## Using the Discord sample bundle

The Discord-guild-chat example bundle in `samples/discord-guild-chat`
demonstrates the ability to reply with `pong` to messages which are equal to
`!ping` or `ping`. Here is a guide to how to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A Discord Bot token

_Note:_ If you don't have such a token yet, you can follow
[this](https://discordjs.guide/preparations/setting-up-a-bot-application.html)
guide.

### Configure the Discord sample bundle

1. In NodeCG, create a new discord service instance using the left upper menu.
2. Enter your bot token.  
   The created instance should be automatically selected, if not select it in
   the upper left menu. Enter your Bot token in monaco (the text-editor on the
   right) in this format:

    ```json
    {
        "botToken": "your-token-goes-here"
    }
    ```

    After entering it, click save.

3. Set the created discord service instance to the service dependency of the
   Discord-guild-chat bundle.  
   Select the Discord-guild-chat bundle and the Discord service in the left
   bottom menu. Then select the service instance that should be used by the
   Discord-guild-chat bundle (in this case the name of the previously created
   discord instance).
4. Check the NodeCG logs.  
   You should see an error or a Login message.
