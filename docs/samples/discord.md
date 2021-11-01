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

!!! Note

    If you don't have such a token yet, you can follow
    [this](https://discordjs.guide/preparations/setting-up-a-bot-application.html)
    guide.

### Configure the Discord sample bundle

1. In NodeCG, create a new discord service instance.
2. Enter your bot token:

    ```json
    {
        "botToken": "your-token-goes-here"
    }
    ```

    After entering it, click save.

3. Set the sample's (`discord-guild-chat`) dependency to be the newly created
   service instance (of type `discord`).
4. Check the NodeCG logs:

    You should see an error or a Login message.
